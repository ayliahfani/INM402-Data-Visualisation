---
id: litvis

narrative-schemas:
  - ../../narrative-schemas/teaching.yml

elm:
  dependencies:
    gicentre/elm-vegalite: latest
    gicentre/tidy: latest
---

@import "../../css/datavis.less"

```elm {l=hidden}
import Tidy exposing (..)
import VegaLite exposing (..)
```

<!-- Everything above this line should probably be left untouched. -->

# Session 1: Practical Exercises

{(task|}

Use this document as a place to add your answers to the week's practical exercises.

{|task)}

## Q.3 Datavis Evaluation

_Rich School, Poor School: Austrailia's Great Education Divide_

The visual shows the income and spending of each school on a map. Showing the data on a map with circles of varying sizes showing the location of schools and their spending is an ideal method of conveying the data. Other methods would likely not be as concise in conveying meaning. It connects and compares data from various school types (religious, state, private) and their location in communities. Since the data includes over 8500 schools interactivity via scaling and movement of the map is in place. This encourages users to engage with the visual all while converying the data in a meaningful and concise manner.

## Q.4 Bicycle Hires Visualization

```elm {l v}
bikehireBarchart : Spec
bikehireBarchart =
    let
        data =
            dataFromUrl "https://gicentre.github.io/data/bicycleHiresLondon.csv"

        enc =
            encoding
                << position X [ pName "Month", pTemporal ]
                << position Y [ pName "NumberOfHires", pQuant ]
    in
    toVegaLite [ width 640, data [], enc [], bar [] ]
```

The visualisation is intened to show the number of bike hires during a given month of a year. Hires spike in the summer when weather is nicer. hires have also spiked in response to COVID.

## Q.5 Creating a Scatterplot

```elm{l v}
bikehirescatterchart : Spec
bikehirescatterchart =
    let
        data =
            dataFromUrl "https://gicentre.github.io/data/bicycleHiresLondon.csv"

        enc =
            encoding
                << position X [ pName "Month", pTemporal ]
                << position Y [ pName "AvHireTime", pQuant ]
    in
    toVegaLite [ width 640, data [], enc [], circle [] ]
```

## Q.6 Data Challenge

```elm{l v}
uk : Spec
uk =
    let
        data =
            dataFromUrl "https://gicentre.github.io/data/euPolls.json"

        enc =
            encoding
                << position X [ pName "Date", pTemporal ]
                << position Y [ pName "Percent", pQuant ]
                << color [ mName "Answer", mQuant]
    in
    toVegaLite [ width 640, data [], enc [], line [] ]
```

## Q.7 Design Challenge

_Add a link to a photo of your design sketch._
