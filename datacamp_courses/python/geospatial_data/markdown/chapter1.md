\title{
Geospatial Data
}

WORKING WITH GEOSPATIAL DATA IN PYTHON

Instructors \(\square\)

Joris Van den Bossche \& Dani Arribas-

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-01.jpg?height=331&width=342&top_left_y=1202&top_left_x=1956)
Bel

\section*{What is Geospatial Data?}

Geospatial data are data with location information

\section*{What is Geospatial Data?}

Geospatial data are data with location information

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-04.jpg?height=2046&width=2708&top_left_y=73&top_left_x=757)

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-05.jpg?height=320&width=309&top_left_y=285&top_left_x=822)

\(12: 54\) PM on Sunday, Oclober 2, 2016

Lunch Ride

Add a description

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-05.jpg?height=157&width=141&top_left_y=562&top_left_x=1156)

\(40.3 \mathrm{~km} \quad 1: 44: 53 \quad 223 \mathrm{~m}\)

Distance Moving Time Elevation

\(173 w \quad 1,088 \mathrm{~kJ}\)

Estimated Ai

Avg Max

Snow More

Speed 3.1 kmh 2:08:22

View Flybys

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-05.jpg?height=1026&width=2742&top_left_y=1066&top_left_x=767)

\section*{How we record the real world}

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-06.jpg?height=1574&width=1606&top_left_y=423&top_left_x=1297)

\section*{Raster versus vector data}

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-07.jpg?height=1281&width=1877&top_left_y=396&top_left_x=217)

Raster

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-07.jpg?height=1291&width=1824&top_left_y=396&top_left_x=2170)

Vector

\section*{Vector features}

"Discrete" representations that turn the world into:

Point(2, 10)

\section*{Vector features}

"Discrete" representations that turn the world into:

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-09.jpg?height=820&width=1280&top_left_y=697&top_left_x=505)

Point(2, 10)

LineString \(([(1,2),(1,5), \ldots])\)

\section*{Vector features}

"Discrete" representations that turn the world into:

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-10.jpg?height=917&width=1405&top_left_y=703&top_left_x=502)

Point(2, 10)

LineString \(([(1,2),(1,5), \ldots])\)

Polygon([(13, 1), (14, 4), ...])

Feature consisting of multiple geometries: eg MultiPolygon

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-11.jpg?height=1541&width=3174&top_left_y=434&top_left_x=638)

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-12.jpg?height=1541&width=3174&top_left_y=434&top_left_x=638)

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-13.jpg?height=1547&width=3174&top_left_y=431&top_left_x=638)

\section*{Vector attribute data}

Vector features can have information associated that describe them: attributes

Tabular vector data:

\begin{tabular}{|c|c|c|c|c|}
\hline & name & capltal & population & geometry \\
\hline 0 & Afghanistan & Kabul & 34124811.0 & POLYGON ((61.21081709172574 35.65007233330923,... \\
\hline 1 & Angola & Luanda & 29310273.0 & (POLYGON ((23.90415368011818 -11.7222815894063... \\
\hline 2 & Albania & Tirana & 3047987.0 & POLYGON ((21.0200403174764 40.84272695572588, ... \\
\hline\(\cdots\) & \(\cdots\) & \(\cdots\) & \(\cdots\) & \(\cdots\) \\
\hline 174 & South Africa & Cape Town & 54841552.0 & POLYGON ([19.89576785653443 -24.76779021576059... \\
\hline 175 & Zambia & Lusaka & 15972000.0 & POLYGON ( (23.21504845550606 -17.52311614346598... \\
\hline 176 & Zimbabwe & Harare & 13805084.0 & POLYGON ((29.43218834810904 -22.09131275806759... \\
\hline
\end{tabular}

\section*{Let's practice!}

WORKING WITH GEOSPATIAL DATA IN PYTHON

\section*{Introduction to GeoPandas}

WORKING WITH GEOSPATIAL DATA IN PYTHON

Joris Van den Bossche

Open source software developer and

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-16.jpg?height=353&width=347&top_left_y=1321&top_left_x=1948)
teacher, GeoPandas maintainer

\section*{Spatial specific data formats}

restaurants = pd.read_csv("datasets/paris_restaurants.csv")

restaurants.head()

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-17.jpg?height=749&width=4005&top_left_y=646&top_left_x=119)

In the rest of the course:
- spatial file formats (Shapefiles, GeoJSON, GeoPackage, ...)
- GeoPandas: pandas dataframes with support for spatial data

\section*{Importing geospatial data with GeoPandas}

import geopandas

countries = geopandas.read_file("countries.geojson")

countries.head()

\begin{tabular}{|c|c|c|c|c|}
\hline & name & continent & gdp & geometry \\
\hline 0 & Afghanistan & Asia & 64080.0 & POLYGON ((61.21 35.65, 62.23 35... \\
\hline 1 & Angola & Africa & 189000.0 & MULTIPOLYGON (((23.90 -11.72, 2. \\
\hline 2 & Albania & Europe & 33900.0 & POLYGON ((21.02 40.84, \(21.0040 \ldots\) \\
\hline 4 & Argentina & South America & 879400.0 & MULTIPOLYGON ((C-66.96 -54.90, \\
\hline 5 & Armenia & Asia & \(26300.0 \quad\) & POLYGON ((43.58 41.09, 44.9741. \\
\hline
\end{tabular}

\section*{Quickly visualizing spatial data with GeoPandas}

countries.plot()

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-19.jpg?height=1042&width=2089&top_left_y=917&top_left_x=1039)

\section*{The GeoDataFrame}

countries.head()

\begin{tabular}{|rrrrrr}
\hline & name & continent & gdp & geometry \\
0 & Afghanistan & Asia & 64080.0 & POLYGON ( \(61.2135 .65,62.2335 \ldots\) \\
1 & Angola & Africa & 189000.0 & MULTIPOLYGON ( ( \(23.90-11.72,2 \ldots\) \\
2 & Albania & Europe & 33900.0 & POLYGON ( \(21.0240 .84,21.0040 \ldots\) \\
\(\ldots\) & & & & \\
\hline
\end{tabular}

type(countries)

geopandas.geodataframe.GeoDataFrame

\section*{The GeoDataFrame}

countries.head()

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-21.jpg?height=809&width=4010&top_left_y=583&top_left_x=122)

A GeoDataFrame represents a tabular, geospatial vector dataset:

- a 'geometry' column: that holds the geometry information

- other columns: attributes describe each of the geometries

\section*{The 'geometry' attribute}

countries.geometry

```
0 POLYGON ((61.21 35.65, 62.23 35...
1 MULTIPOLYGON (()23.90 -11.72, 2...
175 POLYGON ((23.22 -17.52, 22.56 -...
176 POLYGON ((29.43 -22.09, 28.79 -...
Name: geometry, Length: 176, dtype: object
```

type(countries.geometry)

geopandas.geoseries.GeoSeries

\section*{Spatial aware DataFrame}

countries.geometry.area

```
0 63.593500
1 103.599439
2 3.185163
174 112.718524
175 62.789498
176 32.280371
Length: 177, dtype: float64
```

\section*{Summary}

A GeoDataFrame is like a pandas DataFrame:

- all features of normal pandas DataFrames still work

but supercharged with spatial functionality:

- plot() method

- geometry attribute (GeoSeries)

- spatial-specific attributes and methods (e.g. area )

\section*{Let's practice!}

WORKING WITH GEOSPATIAL DATA IN PYTHON

\section*{Exploring and visualizing spatial data and its \\ attributes}

WORKING WITH GEOSPATIAL DATA IN PYTHON

Joris Van den Bossche

Open source software developer and teacher, GeoPandas maintainer

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-26.jpg?height=321&width=336&top_left_y=1565&top_left_x=1959)

\section*{Filtering data}

countries.head()

\begin{tabular}{|rrrrr}
\hline & name & continent & gdp & geometry \\
0 & Afghanistan & Asia & 64080.0 & POLYGON ( \(61.21 \quad 35.65,62.23 \quad 35 \ldots\) \\
1 & Angola & Africa & 189000.0 & MULTIPOLYGON ( ( \(23.90-11.72,2 \ldots\) \\
\(\ldots\) & & & \\
\hline
\end{tabular}

countries['continent'] == 'Africa'

\(\begin{array}{ll}0 & \text { False } \\ 1 & \text { True } \\ & \cdots \\ 175 & \text { True } \\ 176 & \text { True } \\ \text { Name: continent, Length: 177, dtype: bool }\end{array}\)

\section*{Filtering data}

countries_africa = countries[countries['continent'] == 'Africa']

countries_africa.plot()

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-28.jpg?height=922&width=923&top_left_y=988&top_left_x=1633)

\section*{Visualizing spatial data}

countries.plot()

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-29.jpg?height=1042&width=2089&top_left_y=917&top_left_x=1039)

\section*{Adjusting the color: uniform color}

countries.plot(color="red")

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-30.jpg?height=1047&width=2094&top_left_y=909&top_left_x=1031)

\section*{Adjusting the color: based on attribute values}

```
countries.plot(column='gdp_per_cap')
```

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-31.jpg?height=1118&width=2778&top_left_y=613&top_left_x=733)

\section*{Multi-layered plot}

```
fig, ax = plt.subplots(figsize=(12, 6))
countries.plot(ax=ax)
cities.plot(ax=ax, color='red', markersize=10)
ax.set_axis_off()
```

![](https://cdn.mathpix.com/cropped/2024_07_18_52c5ea38e2de6f551988g-32.jpg?height=977&width=2437&top_left_y=955&top_left_x=952)

\section*{Let's practice!}

WORKING WITH GEOSPATIAL DATA IN PYTHON