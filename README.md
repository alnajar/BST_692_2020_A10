# Assignment 10 - Build your first Shiny App

First Name - Last Name

## **Problem statement**

You've explored your data and built your models. Your collaborators want to see your work. They are clinicians, not R programmers. You cannot just send them a static PDF file, they need to be able to visualize interaction between variables and select between subgroups of women.

## Files to work on

* app.R

### Running tests

* N/A

## Tasks

### Build app.R within the "predict_breast" subdirectory

- Build Shiny Web App
  - Open a new r script
  - Load the shiny and tidyverse libraries
  - Start a shiny app using the shiny app snippet
    - Start typing 'shiny' in your script and RStudio will offer autocomplete suggestions
- Integrate either tab
  - tabs: EDA, Models, Map
- Give your app a title
- Include an input widget to select a city in EDA tab
  - SelectInput
- Include a render/output pair
  - EDA plots from Assignment 4

### Notes
You want to have a reactive dataset in the server to be able to subset the women based on city. We will cover this more on 06/17, but a good place to start is to first create the skeleton of the app, with title and tabs, and then get your EDA plots to display for all women. Then, add the filtering for city that listens to the city dropdown.

#### Hint

```{r}
#store the unique values of city into a vector
cities <- unique(myData$city)

#then pass that vector into the `choices` argument of selectInput
```
