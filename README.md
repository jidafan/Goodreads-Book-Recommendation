# Goodreads Book Recommendation

## Table of Contents
* [Introduction](#introduction)
* [Data Overview](#data-overview)
* [Methods](#methods)
* [Results](#results)
* [Conclusion](#conclusion)

## Introduction

Books have been published and read for thousands of years and span various subjects ranging from cooking to fantasy. Many readers have a dilemma regarding books, deciding the next one they will commit to. Sometimes the vastness of material can overwhelm a person, and leave them feeling that there is nothing to read. This project focuses on various techniques to create recommendations for users using their liked books as a basis.

## Data Overview

The data we used to perform this analysis was obtained from **[this](https://sites.google.com/eng.ucsd.edu/ucsdbookgraph/home)** dataset from UCSD which was obtained via scraping user's public shelves. 
It includes data from three files **goodreads_books.json.gz**, which includes the metadata of tens of thousands of books. This includes the Goodreads URL of the book, the cover image of the book, and other details of the book. The file **goodreads_interactions.csv** includes userid,bookid and the rating of the book from the user. The last file **book_id_map.csv** is used to map the books to the bookid listed on the Goodreads website.

| Variable      | Description           | 
| ------------- |:---------------------| 
| `userid`     | The number that uniquely identifies a user from the Goodreads website    |
| `bookid`     | The number that uniquely identifies a book from the Goodreads website           |   
| `rating` | The rating of a book assigned from a user on the Goodreads website                                         |

## Methods

The methods that we used in this project are:
1. TFIDF Matrices
2. Cosine Similarity
3. Collaborative Filtering


In this project, we used a TFIDF matrix to create a function that allows users to search for books, so we are able to create a list of books that are liked by the user. In conjunction with the TFIDF matrix, we use cosine similarity to find the exact book a user is looking for. As some books have the same names as others. Afterwards, we use coo matrices and cosine similarity to implement collaborative filtering to recommend books to the user, based on the likes of other users with similar tastes to us.

## Results 

After we input our list of liked books, we see that the reviews are heavily skewed towards fantasy novels, more specifically towards the "Harry Potter" series. 

![image](https://github.com/jidafan/Goodreads-Book-Recommendation/assets/141703009/16975728-a190-43e4-ac59-d24d8d260a53)

## Conclusion

To conclude, the program did well in recommending books for us to read for the most part. It could be improved with a more extensive list of books to scan through. In addition we could improve the program, by asking for specific recommendations based on genre of the book.
