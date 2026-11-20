# How to Calculate the Volume of a Horizontal Cylindrical Tank

A horizontal cylindrical tank is the same shape as a standing cylinder, turned on its side. Fuel tanks, water bowsers, LPG bullets and many farm tanks are built this way, so knowing how much one holds matters before you buy, fill or size a pump for it.

The good news is that a full horizontal tank uses the same formula as any cylinder. The tricky part is only a partly filled tank, where the liquid surface cuts a circular segment instead of a full circle.

## The formula

For a cylinder of radius r and length L (the length plays the role of height here):

**V = pi x r^2 x L**

If you measured the diameter d instead of the radius, use this form:

**V = (pi x d^2 x L) / 4**

Keep radius and length in the same unit before you start. Mixing cm and metres is the most common mistake, and it throws the answer out by a factor of 100 or more.

## Worked example 1: a 2-metre fuel tank

Take a horizontal tank with radius 0.6 m and length 2.0 m.

1. Square the radius: 0.6^2 = 0.36
2. Multiply by pi: 0.36 x 3.14159 = 1.131 m^2 (the area of the circular end)
3. Multiply by the length: 1.131 x 2.0 = **2.262 m^3**

That is **2,261.9 litres**, or about **597.5 US gallons** when full.

## Worked example 2: a drum lying on its side

A drum has radius 30 cm and length 120 cm.

1. Base area: pi x 30^2 = pi x 900 = 2,827.43 cm^2
2. Volume: 2,827.43 x 120 = **339,292 cm^3**
3. That is **339.29 litres**, or about **89.6 US gallons**.

## Doing it in code

The same formula is three lines in Python, handy if you are sizing several tanks at once:

```python
import math

def cylinder_volume(radius, length):
    return math.pi * radius ** 2 * length

print(cylinder_volume(0.6, 2.0))   # 2.2619 cubic metres
print(cylinder_volume(0.6, 2.0) * 1000)  # 2261.9 litres
```

Keep the units consistent in the inputs and the output follows in the matching cubic unit.

## What changes when the tank is only partly full

A full tank is simple, but a partly filled horizontal tank is not half full at half depth. The liquid surface forms a circular segment, so the volume grows slowly at first, faster in the middle, then slowly again near the top. As a guide, a tank filled to a quarter of its depth holds only about 19.6 percent of its full volume, not 25 percent. If you need exact part-fill figures, work through the [volume of a horizontal cylinder](https://www.cylindervolume-calculator.com/horizontal/) page, which covers the segment calculation step by step.

For a quick full-tank check without doing the arithmetic by hand, use a free [cylinder volume calculator](https://www.cylindervolume-calculator.com/) and enter the radius and length. It shows the step-by-step working and converts the result to litres, gallons, cubic feet and more.

## FAQ

**Does a horizontal cylinder hold the same volume as a vertical one?**
Yes, when both are full and have the same radius and length. Turning a cylinder on its side changes the orientation, not the volume.

**Why is my tank's rated capacity lower than this calculation?**
Rated capacity often leaves headspace for expansion, vents and fittings, and the stated size may be nominal rather than exact. Measure the inside dimensions for the true volume.

**How do I convert cubic metres to litres?**
Multiply by 1,000. One cubic metre is 1,000 litres, so 2.262 m^3 is 2,262 litres (2,261.9 litres exact).
