# Top 10 Movie Performance History
## Introduction
Movies are a popular form of entertainment, and understanding the characteristics that make a movie successful can greatly benefit the film industry. In this project, we explore the traits of the most successful movies of each year to identify key factors that contribute to box office success. Our goal is to assist directors and production studios in making informed decisions for future movie productions based on historical movie revenue and perceived success.

## Data
The primary dataset for this project is sourced from Blockbuster (_https://data.world/crowdflower/blockbuster-database/workspace/file?filename=blockbuster-top_ten_movies_per_year_DFE.csv_). 
It consists of the top 10 movies per year from 1975 to 2014, containing details on movie characteristics, revenue insights, and various rating criteria such as Rotten Tomatoes and IMDb scores. This dataset has eben condensed to include attributes relevant to movie production, such as release date, genre, maturity rating, runtime, production studio, budget, and performance. 
Movie performance is measured through viewer ratings (Rotten Tomatoes, IMDb), and gross revenue (_https://www.boxofficemojo.com/year/?grossesOption=totalGrosses_).

## Data Dictionary
- **MovieID**	(Text):	Unique number assigned to each movie
- **Title**	(Text):	Name of the movie
- **StudioID**	(Text):	Unique number assigned to each studio
- **Studio**	(Text):	Name of the studio that produced the film
- **Year**  (Numeric):	Year in which the movie was released
- **Release** Date	(Date):	Day the movie was released in theaters
- **rt_freshness**	(Numeric):	Rotten Tomatoes rating from critics
- **rt_audience**	(Numeric): Rotten Tomatoes rating from the audience
- **rt_score**	(Numeric):	Overall Rotten Tomatoes rating
- **IMDb rating**	(Numeric):	IMDb rating
- **Maturity Rating**	(Text):	Maturity rating given by experts (G, PG, PG-13, R)
- **Length**	(Numeric):	Total runtime of the film
- **Genre ID**	(Text):	Unique identifier for each genre
- **Genre(s)**	(Text):	Genre(s) that the film falls into
- **Worldwide Gross**:	(Numeric)	Total worldwide gross revenue
- **Total Gross**	(Numeric):	Total gross revenue of all films released in each year
- **Total Releases**	(Numeric):	Number of movies released in each year

## Entity Relationship Diagram (ERD)
The primary entity in our database is **MOVIE**, identified by **MovieID**. The Movie entity includes Studio and Genre, both being multivalued attributes. Year is derived from the movie release date. We have normalized our data and created a relational schema diagram with 6 tables.

## Database Implementation
We have implemented the database in APEX using CREATE TABLE commands for each table in the schema. The tables created are MOVIE, YEAR, STUDIO, GENRE, MOVIE_GENRE, and MOVIE_STUDIO.

## Analysis
Our analysis aims to provide production studios and directors with insights into successful movies. By analyzing historical box office success, we identify the best studios, genres, and runtimes for profitable movie productions.

## Website
Feel free to explore this project's web application at **https://apex.oracle.com/pls/apex/r/db_group_project/historical-movie-performance/home?session=732598589482**
