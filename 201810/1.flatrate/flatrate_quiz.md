Q) 사용자별 이용권 시작일 ~ 종료일 정보를 이용하여 다음과 같은 차트를 그려주세요...!  

```{r, message=FALSE, warning=FALSE}
library(dplyr)
library(ggplot2)

set.seed(7)

df <-
  data.frame(
    id = 1:10, 
    from = as.Date(Sys.Date()) + sample(1:20, 10, TRUE)) %>% 
  mutate(
    to = from + sample(3:10, 10, TRUE))
```

![target!](flatrate_result.PNG)
