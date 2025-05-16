# Usage

## Basic Usage

The main entry point is the `plot()` function:

```python
import prettymaps
prettymaps.plot("Porto Alegre")
```

This will generate a map for the given location using default layers and styles.

## Customizing Layers and Styles

You can customize which OpenStreetMap layers are shown and how they are styled:

```python
layers = {
    "perimeter": {},
    "streets": {"width": 8},
    "buildings": {},
}
style = {
    "perimeter": {"fc": "#f2efe9"},
    "streets": {"fc": "#cccccc", "ec": "#333333"},
    "buildings": {"fc": "#bdbdbd"},
}
prettymaps.plot("Porto Alegre", layers=layers, style=style)
```

## Using Presets

Presets are reusable configurations for layers and styles. You can load, save, or update presets:

```python
prettymaps.plot("Porto Alegre", preset="default")
```

You can also create your own presets and save them for later use.

## Highlighting Keypoints

You can highlight specific keypoints (e.g., landmarks) on the map:

```python
keypoints = {
    "tags": {"tourism": "attraction"},
    "kwargs": {"bbox": {"fc": "yellow"}},
}
prettymaps.plot("Porto Alegre", keypoints=keypoints)
```

## Saving Maps

You can save the generated map to a file:

```python
prettymaps.plot("Porto Alegre", save_as="map.png")
```

---

See the [API Reference](api.md) for details on all functions and parameters. 