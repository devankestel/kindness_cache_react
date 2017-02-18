# App Models

## Static Content
* ### Getting Started?

## User
  * Relations:
    * has many Acts
    * has many Completions through Acts
  * Attributes:
    * e-mail (string)
    * password (digest 2 strings)
    * forgot password (bool)
    * name (string)

## Act
  * Relations:
    * belongs to Category
    * belongs to User
    * has many Completions
  * Attributes:
    * description (string)

## Completion
  * Relations:
    * belongs to Act
  * Attributes:
    * timestamp (datetime)

## Category
  * Relations:
    * has many Acts
    * has many Users through Acts
  * Attributes:  
    * title [stranger | friend | family | self]

## User Stats
  * Act Completions by Category (100% bar format)
    * act completions in category / total act completions
  * Current Streak
    * number of days in a row from present day with at least one completion
  * Act Completions by Day (calendar format, heat style)
    * find act completions for specific date
  * Frequently Completed Acts
    * Acts ordered from greatest to least number of completions
    * Filterable by category
