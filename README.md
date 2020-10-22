# imdb-api
non-official IMDb API client (sort of)

## how to

```
usage: imdb-api [-h] [-p] [imdb_id]

positional arguments:
  imdb_id               IMDb ID.

optional arguments:
  -h, --help            show this help message and exit
  -p, --only-poster-url
                        GET just the Movie Poster URL.
```

### Get a movie JSON 
```
$ imdb-api tt0093779
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
$ imdb-api -p tt0093779
https://m.media-amazon.com/images/M/MV5BMGM4M2Q5N2MtNThkZS00NTc1LTk1NTItNWEyZjJjNDRmNDk5XkEyXkFqcGdeQXVyMjA0MDQ0Mjc@._V1_.jpg
```

### Or an Actor JSON
```
$ imdb-api nm0005260
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
