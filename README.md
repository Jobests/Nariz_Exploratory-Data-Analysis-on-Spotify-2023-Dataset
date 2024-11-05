# Nariz_2ECE-A_Incentives

## Description
#### The project aims to perform Exploratory Data Analysis(EDA) on a dataset of the most streamed songs on spotify in 2023.

## Libraries Needed
* Pandas
* Matplotlib
* Seaborn

## Loading the Dataset

#### The code reads the spotify_2023.csv file using the `pd.read_csv` function into a Pandas DataFrame named `spotify`, using ISO-8859-1 encoding to handle special characters.

```python
spotify = pd.read_csv('spotify_2023.csv', encoding='ISO-8859-1')
spotify
```

## Output
![Screenshot 2024-11-05 191913](https://github.com/user-attachments/assets/c021a06d-e396-4b68-a5e3-80035a7905d8)

## OVERVIEW OF THE DATASET

## Identifying the number of rows and column

#### This code retrieves the dimensions of the `spotify` DataFrame using the `spotify.shape` attribute, which returns a tuple containing the number of rows and columns; it unpacks this tuple into the variables rows and columns. The subsequent print statements then output the total number of rows and columns in the DataFrame, providing a quick overview of its size.

```python
rows, columns = spotify.shape
print('The number of rows are:', rows)
print('The number of columns are:', columns)
```
## Output

#### The output indicates that the `spotify` DataFrame has 953 rows and 24 columns, meaning there are 953 records in the dataset, each with 24 attributes or features. This provides a summary of the dataset's size and structure, showing the number of entries and the various pieces of information available for each entry.

```output
The number of rows are: 953
The number of columns are: 24
```

## Identifying the data types of each column

#### This code retrieves the data types of each column in the `spotify` DataFrame using `spotify.dtypes` and assigns them to the variable `data_types`. It then prints a message followed by the `data_types` Series, providing a quick overview of the type of data stored in each column, such as integers, floats, or strings.

```python
data_types = spotify.dtypes
print('Data types of each columns are:')
data_types
```
## Output

#### This is the output showing the data types of each column in the `spotify` DataFrame, indicating a mix of `object` and `int64` types. This summary provides insight into the nature of the data in the dataset.

```output
Data types of each column are:
track_name              object
artist(s)_name          object
artist_count             int64
released_year            int64
released_month           int64
released_day             int64
in_spotify_playlists     int64
in_spotify_charts        int64
streams                 object
in_apple_playlists       int64
in_apple_charts          int64
in_deezer_playlists     object
in_deezer_charts         int64
in_shazam_charts        object
bpm                      int64
key                     object
mode                    object
danceability_%           int64
valence_%                int64
energy_%                 int64
acousticness_%           int64
instrumentalness_%       int64
liveness_%               int64
speechiness_%            int64
dtype: object
```
## Cleaning the Data
* Hnadling missing values
* Removing duplicate values
* Correcting data types
