# imdb-api
non-official IMDb API client (sort of)

## how to

```
usage: imdb-api [-h] [--search [SEARCH]] [--imdb-id [IMDB_ID]] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --search [SEARCH]     Search IMDb by string.
  --imdb-id [IMDB_ID]   Get IMDb Object by ID.
  -p, --only-poster-url
                        GET just the Movie Poster URL.
```

### Search by title

```
$ imdb-api --search alucarda
{
  "v": 1,
  "q": "alucarda",
  "d": [
    {
      "l": "Alucarda",
      "id": "tt0075666",
      "s": "Claudio Brook, David Silva",
      "y": 1977,
      "q": "feature",
      "i": [
        "https://m.media-amazon.com/images/M/MV5BNzZmZTg3NjUtYTVmYi00Njg3LTlhYmUtNDhmYWM4NjM2ZjY1XkEyXkFqcGdeQXVyMTk0MjQ3Nzk@._V1_.jpg",
        465,
        691
      ]
    },
    {
      "l": "Azra Medea",
      "id": "nm2910194",
      "s": "Composer, 5 Dark Souls (1996)"
    },
    {
      "l": "Docion",
      "id": "nm2910746",
      "s": "Composer, 5 Dark Souls (1996)"
    },
    {
      "l": "Olivia Luccardi",
      "id": "nm3459140",
      "s": "Actress, It Follows (2014)",
      "i": [
        "https://m.media-amazon.com/images/M/MV5BZGI3YzVmZDktNzRiYi00ZTg1LTljMzctZDNjZmMzOTc2MzFhXkEyXkFqcGdeQXVyMjQwMDg0Ng@@._V1_.jpg",
        2647,
        3308
      ]
    },
    {
      "l": "Alucard",
      "id": "tt1414352",
      "s": "Jay Barber, William G. Smith",
      "y": 2008,
      "q": "video",
      "i": [
        "https://m.media-amazon.com/images/M/MV5BMjM1NzkzNTc5NV5BMl5BanBnXkFtZTgwMDE1MzA2MDE@._V1_.jpg",
        350,
        500
      ]
    },
    {
      "l": "AFI Life Achievement Award: A Tribute to George Lucas",
      "id": "tt0466641",
      "s": "Melissa Disney, Carole Bayer Sager",
      "y": 2005,
      "q": "TV special",
      "i": [
        "https://m.media-amazon.com/images/M/MV5BYzljNzVkYmYtMjg5My00MmI2LTg4ZDQtOTlmMTRmYmYwNWZmXkEyXkFqcGdeQXVyMTY4MjQ0NzU@._V1_.jpg",
        979,
        731
      ]
    },
    {
      "l": "La Lucarne d'Amilcar",
      "id": "tt10351186",
      "s": "Karen Chéryl, Eric Galliano",
      "y": 1987,
      "yr": "1987-1989",
      "q": "TV series"
    },
    {
      "l": "La lucarne des rêves",
      "id": "tt7826264",
      "s": "Michel Chion, Beatriz Ferreyra",
      "y": 2017,
      "q": "feature",
      "i": [
        "https://m.media-amazon.com/images/M/MV5BODE2ZDMzNDMtMzgwNC00N2RkLWJiYTItMmFmYzZlMWNkYzdlXkEyXkFqcGdeQXVyNzE5MzE4ODU@._V1_.jpg",
        2480,
        3507
      ]
    }
  ]
}
```

### Get a movie JSON 
```
$ imdb-api --imdb-id tt0093779
{                               
  "@context": "http://schema.org",
  "@type": "Movie",
  "url": "/title/tt0093779/",
  "name": "The Princess Bride",
  "image": "https://m.media-amazon.com/images/M/MV5BMGM4M2Q5N2MtNThkZS00NTc1LTk1NTItNWEyZjJjNDRmNDk5XkEyXkFqcGdeQXVyMjA0MDQ0Mjc@._V1_.jpg",
  "genre": [                                      
    "Adventure",                           
    "Family",                 
    "Fantasy",                    
    "Romance"                                                                                                                                                                                                        
  ],  
  "contentRating": "PG",               
  [...]
}
```

### Get the movie poster

```
$ imdb-api -p --imdb-id tt0093779
https://m.media-amazon.com/images/M/MV5BMGM4M2Q5N2MtNThkZS00NTc1LTk1NTItNWEyZjJjNDRmNDk5XkEyXkFqcGdeQXVyMjA0MDQ0Mjc@._V1_.jpg
```

### Or an Actor JSON
```
$ imdb-api --imdb-id nm0005260
{
  "@context": "http://schema.org",
  "@type": "Person",
  "url": "/name/nm0005260/",
  "name": "Frankie Muniz",
  "image": "https://m.media-amazon.com/images/M/MV5BMTkxNTU1Njk5MV5BMl5BanBnXkFtZTcwODUzNjQ0Nw@@._V1_.jpg",
  "jobTitle": [
    "Actor",
    "Soundtrack",
    "Producer"
  ],
  "description": "Frankie was born in Wood-Ridge, New Jersey, to Denise, a nurse, and Francisco Muniz III, a restaurateur. His father is of Puerto Rican heritage and his mother is of Irish and Italian descent. Frankie was home-schooled since Grade Six. He started his acting career performing the role of Tiny Tim in \"A Christmas Carol\" for three years. Nominations ...",
  "birthDate": "1985-12-05"
}
```

## license

See [LICENSE](LICENSE)
