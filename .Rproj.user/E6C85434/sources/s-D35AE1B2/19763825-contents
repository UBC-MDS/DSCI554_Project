# This version is to be run on an Amazon EC2 + S3 for DSCI 525 Lab 3, Ex 3

suppressPackageStartupMessages(library("readr"))
suppressPackageStartupMessages(library("dplyr"))
suppressPackageStartupMessages(library("haven"))
suppressPackageStartupMessages(library("ggplot2"))
suppressPackageStartupMessages(library("stringr"))
library("RCurl")

# 1.0 Clean data 


# Read data
data <- read.table(textConnection(getURL(
  "https://s3-us-west-2.amazonaws.com/dsci525-lab3-bucket/data/data.csv"
)), sep=",", header=FALSE)

# Select data 
data <-  
  data %>% 
  select(18:22)

# Rename columns 
names(data) <- c("sex", "math_skill", "friend_with_prog", "prog_exp", "difficulty")

# factorize variable in the data
clean_data <- 
  data %>%
  mutate(sex = as_factor(sex),
         math_skill = as_factor(math_skill,
                                levels=c("Below Average",
                                         "Average",
                                         "Above Average"), ordered=TRUE),
         friend_with_prog = as_factor(friend_with_prog),
         prog_exp = as_factor(prog_exp,
                              levels=c("None",
                                       "Less than 100 hours",
                                       "Less than 1000 hours",
                                       "More than 1000 hours"), ordered=TRUE),
         difficulty = as_factor(difficulty,
                                levels=c("Easier than average",
                                         "Average",
                                         "More difficult than average"),
                                ordered=TRUE)
  )

# Get the size of the data
dim(clean_data)


# Get the strcture of the data
str(clean_data)


# 2.0 EDA

## 2.1 EDA-1


clean_data %>%
  ggplot() + 
  theme_bw() +
  labs(x = "Self-preceived Diffculty",
       # y = "y",
       title = "Self-preceived diffculty of DSCI 512") +
  theme(plot.title = element_text(size = 13, face = "bold", hjust = 0.5)) + 
  geom_bar(aes(difficulty)) 



## 2.1 EDA-2


clean_data %>%
  ggplot() + 
  theme_bw() +
  labs(x = "Programming experience prior to the program",
       # y = "y",
       title = "Level of programming experience prior to the program") +
  theme(plot.title = element_text(size = 13, face = "bold", hjust = 0.5)) + 
  geom_bar(aes(prog_exp)) 



## 2.1 EDA-3


clean_data %>%
  ggplot() + 
  theme_bw() +
  labs(x = "Self-preceived difficulty",
       # y = "y",
       title = "Self-perceived difficulty vs. Sex") +
  theme(plot.title = element_text(size = 13, face = "bold", hjust = 0.5)) + 
  geom_bar(aes(x = difficulty, fill = sex), position = "dodge") 



## 2.1 EDA-4


clean_data %>% ggplot(aes(difficulty, prog_exp)) +
  geom_bin2d() +
  theme_bw() +
  labs(x = "Difficulty", y = "Programming Experience",
       title = "Heatmap of Programming Experience vs. Difficulty") +
  theme(plot.title = element_text(size = 13, face = "bold", hjust = 0.5)) +
  coord_fixed() +
  scale_x_discrete(
    labels = function(difficulty)
      str_wrap(difficulty, width = 14)
  ) +
  scale_fill_continuous(breaks = c(1, 5, 9))


