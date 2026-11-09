# Box Model Task

**Files:** `index.html`, `style.css`

## What I did
I made a `div` and changed its content width, padding and border to see how the total size changes. Then I did the same with height.

## Code used
```css
div {
    width: 400px;
    height: 300px;
    padding: 50px;
    border: 15px dotted red;
    border-radius: 10px;
}
```

## Width (content-box)
| Width | Padding | Border | Total width |
|-------|---------|--------|-------------|
| 200px | 0 | 0 | 200px |
| 200px | 20px | 0 | 240px |
| 200px | 20px | 10px | 260px |
| 200px | 40px | 5px | 290px |
| 400px | 50px | 15px | 530px |

## Height (content-box)
| Height | Padding | Border | Total height |
|--------|---------|--------|--------------|
| 100px | 0 | 0 | 100px |
| 100px | 20px | 0 | 140px |
| 100px | 20px | 10px | 160px |
| 100px | 40px | 5px | 190px |
| 300px | 50px | 15px | 430px |

## Observation
- Padding and border are added on top of width and height, so the box gets bigger.
- Width uses left + right values. Height uses top + bottom values.
- With `box-sizing: border-box` the box stays 400px x 300px and the content area shrinks instead.