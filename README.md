# Advent of code 2022

## About
OK, here we go again!

https://adventofcode.com/2022

## Quickstart
```
python3 -m venv venv
. ./venv/bin/activate
pip install -r requirements.txt
python aoc.py --day "01"
```

## Convenience tools
### Running the aoc solutions
```
# run today's solution
python aoc.py  

# run today's solution against the test input
python aoc.py --test 

# run day 01 against the test input
python aoc.py --day "01" --test  

# run day 05 against the file toto.txt contained in the test input folder
python aoc.py --day "05" --test --filename toto.txt 
```
### Create the base files for a new day
```
make prepare day=03
```


## Tricks I learnt this year
### Iterate through chunks
```
l = [1, 2, 3, 4, 5, 6]
for a, b, c in zip(*(iter(l),) * 3):
    print(a, b, c)
```
```
1 2 3
4 5 6
```
### Pandas intervals
```
from pandas import Interval
a = Interval(1, 4, closed="both")
b = Interval(2, 3, closed="both")
print(a in b)
print(b in a)
print(a.overlaps(b))
```
### Reversed
```
for x in reversed(range(6)):
    print(x)
    
5
4
3
2
1
0
```
### Matplotlib
- See day 14 for animation
- https://github.com/tomsembl/AdventOfCode/blob/main/2022/14.3.py could be a source of inspiration too or https://www.reddit.com/r/adventofcode/comments/zlmwb4/2022_day_14_how_does_everyone_do_visualisations/

### Numpy for dummies
```
grid = np.zeros((10, 5))  # 10 on the y-axis, 5 on the x-axis
x = 4
y = 9
grid[y][x] = 7
print(grid)
```
