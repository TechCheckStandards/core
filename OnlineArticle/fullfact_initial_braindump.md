# Initial Brain Dump

We had a discussion within the technical team about what we would want from an open monitoring standard.
We couched the discussion thinking about the following two use cases:

1. What we would need from shared media to correctly integrate it with out current media monitoring, pattern based solution. 
We thought of this as the **minimum** set of fields to be useful.
2. What we thought would be useful for know future feature work. These are the **future feature** set of fields.
3. What we would need from a more research and development perspective, which we termed the **research** set of fields.

We decided to base out discussion on the schema.org [NewsArticle]() schema of schema.org. 
This is because that, with a couple of exceptions, it covers most things we need for the minimum solution and  has a lot of scope for interesting things to be shared for research purposes.

## The minimal set of fields

The following fields are the on NewsArticle schema and would expect to be filled in for our purposes. 
Note: this includes some fields that our monitoring solution does not extract or make use of. 
It is a slightly aspirational minimum.

|  What we want                     |  Path in schema.org NewsArticle  |
| --------------------------------- | -------------------------------- |
|  Headline                         |  headline                        |
|  Text of the body of the article. |  articleBody                     |
|  Image Captions                   |  headline in associatedMedia     |
|  Quotes in boxes                  |  citation                        |
|  Publication name                 |  name in publisher               |
|  Section of the website           |  articleSection                  |
|  Publication date                 |  datePublished                   |
|  Author                           |  name on author                  |
|  URL (unshortened)                |  url                             |
|  Modified date                    |  dateModified                    |

## Some obviously missing fields for future feature work

There are a couple of fields that are not present that we would need to add, possibly by extending NewsArticle, or adding out own type inheriting from it.

NewsArticle does not include a **corrections** field. 
These are the notes added to the end of the articles that indicate that a correction has occurred. 

It also does not include a **dateRetrieved** field. 
This is required for detecting changes to an article that are made without an explicit correction. 

## Fields on the schema that would be useful in future

Please see [this](https://docs.google.com/spreadsheets/d/1v6GNpSKzF5NuKfUXMwd9Hlb_1B_VGp9qrdxIshNYF98/edit?usp=sharing) spreadsheet for a rundown of what fields we think might be useful in future.