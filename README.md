# Philippine volcanoes :philippines: :volcano:

The entire dataset is available under the [data](./data) directory, classified into active, potentially active, and
inactive volcanoes.

Data sourced from [Wikipedia](https://en.wikipedia.org/wiki/List_of_active_volcanoes_in_the_Philippines) and
the [PHIVOLCS](https://www.phivolcs.dost.gov.ph/index.php/volcano-hazard/volcanoes-of-the-philippines) website.

## Visualization

- Interactive map at [bulkan.vercel.app](https://bulkan.vercel.app) (source code at
  this [repo](https://github.com/j4ckofalltrades/bulkan))
- View the rendered [geojson](data/_index.geojson) and [topojson](data/_index.topojson) directly in GitHub
- View the GeoJSON files at [geojson.io](https://geojson.io)

## Classification

Follows the Philippine Institute of Volcanology and Seismology (PHIVOLCS) classification according to a volcano's
eruptive history:

<dl>
  <dt>Active volcanoes</dt>
  <dd>Erupted within historical times (within the last 600 years), accounts of these eruptions were documented by man erupted within the last 10,000 years based on the analyses of material from young volcanic deposits.</dd>

  <dt>Potentially active volcanoes</dt>
  <dd>Morphologically young-looking but with no historical or analytical records of eruption.</dd>

  <dt>Inactive volcanoes</dt>
  <dd>No recorded eruptions, physical form has been intensively weathered and eroded, bearing deep and long gullies.</dd>
</dl>

## Metadata

Metadata for each mountain can be parsed from the `properties` field.

| field            | description                                                             | required |
|------------------|-------------------------------------------------------------------------|----------|
| `name`           | Name of the volcano                                                     | required |
| `classification` | One of the following values: `active`, `potentially_active`, `inactive` | required |
| `elev`           | Height in meters above sea level                                        | required |
| `coord`          | Formatted coordinates                                                   | required |
| `prov`           | One or more provinces where the mountain is located                     | required |
| `region`         | One or more regions where the mountain is located                       | required |
| `isl_grp`        | Island group where the mountain is located                              | required |
| `alt_names`      | Alternative names or spelling                                           | optional |

## Sample

GeoJSON and TopoJSON data for Mount Kanlaon.

- GeoJSON

```json
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [123.132, 10.412]
  },
  "properties": {
    "name": "Mount Kanlaon",
    "classification": "active",
    "elev": 2465,
    "coord": "10°24′43″N 123°07′55″E",
    "prov": ["Negros Occidental", "Negros Oriental"],
    "region": ["Region VI", "Region VII"],
    "isl_grp": "Visayas",
    "alt_names": [""],
    "marker-symbol": "volcano"
  }
}
```

```geojson
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [123.132, 10.412]
  },
  "properties": {
    "name": "Mount Kanlaon",
    "classification": "active",
    "elev": 2465,
    "coord": "10°24′43″N 123°07′55″E",
    "prov": ["Negros Occidental", "Negros Oriental"],
    "region": ["Region VI", "Region VII"],
    "isl_grp": "Visayas",
    "alt_names": [""],
    "marker-symbol": "volcano"
  }
}
```

- TopoJSON

```json
{
  "type": "Topology",
  "objects": {
    "active": {
      "type": "GeometryCollection",
      "geometries": [
        {
          "type": "Point",
          "coordinates": [123.132, 10.412],
          "properties": {
            "name": "Mount Kanlaon",
            "classification": "active",
            "elev": 2465,
            "coord": "10°24′43″N 123°07′55″E",
            "prov": ["Negros Occidental", "Negros Oriental"],
            "region": ["Region VI", "Region VII"],
            "isl_grp": "Visayas",
            "alt_names": [""],
            "marker-symbol": "volcano"
          }
        }
      ]
    }
  },
  "arcs": [],
  "bbox": [
    125.227721,
    6.541396,
    125.409816,
    7.36793
  ]
}
```

```topojson
{
  "type": "Topology",
  "objects": {
    "active": {
      "type": "GeometryCollection",
      "geometries": [
        {
          "type": "Point",
          "coordinates": [123.132, 10.412],
          "properties": {
            "name": "Mount Kanlaon",
            "classification": "active",
            "elev": 2465,
            "coord": "10°24′43″N 123°07′55″E",
            "prov": ["Negros Occidental", "Negros Oriental"],
            "region": ["Region VI", "Region VII"],
            "isl_grp": "Visayas",
            "alt_names": [""],
            "marker-symbol": "volcano"
          }
        }
      ]
    }
  },
  "arcs": [],
  "bbox": [
    125.227721,
    6.541396,
    125.409816,
    7.36793
  ]
}
```

## Contributing

This is by no means an exhaustive list, so contributions are more than welcome.
Please read and follow the [contribution guidelines](CONTRIBUTING.md).
