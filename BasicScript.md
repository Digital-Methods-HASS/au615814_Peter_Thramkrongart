W4: Start with R
================
Peter
4/10/2020

``` r
pacman::p_load(pacman,tidyverse)


#Create the vector
rooms <- c(1, 2, 1, 3, 1, NA, 3, 1, 3, 2, 1, NA, 1, 8, 3, 1, 4, NA, 1, 3, 1, 2, 1, 7, 1, NA) 

#remove missing values
rooms <- na.omit(rooms)
#how many values are above 2

rooms %>% .[.>2] %>% length()
```

    ## [1] 8

``` r
#This is the result of runing the median() function
rooms %>% median()
```

    ## [1] 1.5

``` r
interviews = read_csv("https://ndownloader.figshare.com/files/11492171")
```

    ## Parsed with column specification:
    ## cols(
    ##   key_ID = col_double(),
    ##   village = col_character(),
    ##   interview_date = col_datetime(format = ""),
    ##   no_membrs = col_double(),
    ##   years_liv = col_double(),
    ##   respondent_wall_type = col_character(),
    ##   rooms = col_double(),
    ##   memb_assoc = col_character(),
    ##   affect_conflicts = col_character(),
    ##   liv_count = col_double(),
    ##   items_owned = col_character(),
    ##   no_meals = col_double(),
    ##   months_lack_food = col_character(),
    ##   instanceID = col_character()
    ## )
