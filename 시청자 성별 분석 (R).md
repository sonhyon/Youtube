# 시청자 성별 분석 (R)

```r

library(dplyr) ; library(ggplot2)

getwd()
setwd('C:/Users/User/유튜브_sonhyon86/데이터')

library('readxl')

# 시청자 성별별 조회수
viewer_gender <- read_excel('시청자 성별.xlsx')
head(viewer_gender)

ggplot(viewer_gender, aes(x = `시청자 성별`, y = `조회수 (%)`, fill = `시청자 성별`)) +
  geom_col() +
  scale_fill_manual(values = c(
    "남성" = "#4C72B0",
    "여성" = "#DD8452"
  ))

# 시청자 성별별 평균시청 지속시간

# 시청자 성별별 평균조회율
ggplot(viewer_gender, aes(x = `시청자 성별`, y = `평균 조회율 (%)`, fill = `시청자 성별`)) +
  geom_col() +
  scale_fill_manual(values = c(
    "남성" = "#4C72B0",
    "여성" = "#DD8452"
  ))

# 시청자 성별별 시청시간
ggplot(viewer_gender, aes(x = `시청자 성별`, y = `시청 시간(단위: 시간) (%)`, fill = `시청자 성별`)) +
  geom_col() +
  scale_fill_manual(values = c(
    "남성" = "#4C72B0",

```
