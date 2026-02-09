# API Query Building Assignment
---

## USGS Earthquake Queries

### Query 1: What were the top ten strongest earthquakes in January?
**URL:**
```
https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&starttime=2024-01-01&endtime=2024-01-31&orderby=magnitude&limit=10
```

**Parameters used:**
- `format`: GeoJSON
- `parameter2`: First month of the year
- `parameter3`: Top ten magnitudes (ordered)

**Result:** It showed 10, because without the limit, the output was so much that it had to be reduced. It was ordered to only output those from January.

---

### Query 2: What are the top 5 least strong earthquakes between 30 lat and 50 lat
**URL:**
```
https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&minlatitude=30&maxlatitude=50&orderby=magnitude-asc&limit=5
```

**Parameters used:**
- `format`: GeoJSON
- `parameter2`: minlatitude=30
- `parameter3`: maxlatitude=50

**Result:** A list of 5 earthquakes that had negative or null magnitudes from that certain area.

---

### Query 3: Earthquakes in the US
**URL:**
```
https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&minlatitude=35&maxlatitude=50&minlongitude=70&maxlongitude=125
```

**Parameters used:**
- `format`: GeoJSON
- `parameter2`: min and max latitude to be between 35 and 50
- `parameter3`: min and max longitude between 70 and 125

**Result:** Some earthquakes from areas that weren't from Ohio...

---

## Open Library Queries

### Query 4: Titles of Books by Stephen King
**URL:**
```

```

**Parameters used:**
- `parameter1`: author=stephen+king
- `parameter2`: fields=title limited the results to titles

**Result:** A list of a ton of titles created by Stephen King


### Query 5: English History books with "America" in the title
**URL:**
```
https://openlibrary.org/search.json?language=eng&subject=history&title=america
```

**Parameters used:**
- `parameter1`: language=eng
- `parameter2`: subject=history
**Result:** Shows a long list of different English history books, many of which start with the word "America."

### Query 6: Books about quantum computing written in English, only displaying title, author, and year published
**URL:**
```
https://openlibrary.org/search.json?q=quantum-computing&language=eng&fields=title,author_name,first_publish_year
```

**Parameters used:**
- `parameter1`: q=quantum-computing
- `parameter2`: language=eng

**Result:** The result was larger than expected, and showed multiple English-written books that were about quantum computing. The filtering allows it to be easier to find the basic attributes of the book without having to filter through all the data yourself.