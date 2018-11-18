[![GoDoc Reference](http://img.shields.io/badge/godoc-reference-5272B4.svg?style=flat-square)](http://godoc.org/github.com/FATHOM5/haversine)
[![Build Status](https://travis-ci.org/FATHOM5/haversine.svg?branch=master)](https://travis-ci.org/FATHOM5/haversine)
[![Go Report Card](https://goreportcard.com/badge/github.com/FATHOM5/haversine?style=flat-square)](https://goreportcard.com/report/github.com/FATHOM5/haversine)
[![Coverage Status](https://coveralls.io/repos/github/FATHOM5/haversine/badge.svg?branch=master)](https://coveralls.io/github/FATHOM5/haversine?branch=master)

## Haversine

Package haversine provides the great circle distance between two points on the surface of the earth.  Points are identified by latitude and longitude, and distance results can be returned in nautical miles, statute miles, or kilometers.  
![Earth great circle](https://i.imgur.com/iD3X3Ax.png)

The curvature of the earth means that shortest distance between two points cannot be a straight line between the points.  The Haversine formula provides an approximation for the shortest great circle route over the surface of earth that connects the two points.  In this figure the dotted yellow line is the arc of a great circle. *Image courtesy USGS.*

## Installation

`go get github.com/FATHOM5/haversine`

## Usage

The example below shows how far I'd have to walk in my boots to go visit my
co-founder.

    package main

    import (
        "fmt"

        "github.com/FATHOM5/haversine"
    )

    func main() {
        austin := haversine.Coord{ // Austin, Texas
            Lat: 30.2672,
            Lon: -97.7431,
        }
        paloAlto := haversine.Coord{ // Palo Alto, California
            Lat: 37.4419,
            Lon: 122.1430,
        }

        nm := haversine.Distance(austin, paloAlto)

        fmt.Printf("%.1f miles is a long walk to Silicon Valley.\n", nm)
    }

## Documenation

* http://godoc.org/github.com/FATHOM5/haversine

## References

* Many thanks to the original author, [umahmood](https://github.com/umahmood/haversine), for a great package to begin this fork.
* https://plus.maths.org/content/lost-lovely-haversine
* https://en.wikipedia.org/wiki/Haversine_formula

## License

See [LICENSE](LICENSE.md) for rights and limitations (MIT).
