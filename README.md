# VU ISI Blockchain course's hashing function ranking
Hashrank is a tool designed to help rank VU ISI hashing algorithms. This benchmark will determine how fast and reliable your algorithm works.

![](https://media.giphy.com/media/6Z3D5t31ZdoNW/giphy.gif)  

### The idea behind the benchmark
This benchmark is designed based on [Blockchain Group's practical task analysys](https://github.com/blockchain-group/Blockchain-technologijos/blob/master/pratybos/1uzduotis-Hashavimas.md) but with a few key changes:
1) The size of random strings is 1000 characters. This size was chosen because the most difficult part of hashing algorithm is the compression of the input and 5 character long string is too short to require any compression (most of the time only padding will be made).
2) Benchmark is not only calculating average of the similarity of pair of strings but also calculating the number of collisions it found.

### Requirements for the hashing algorithm
* It must accept string as `Console Argument`
* It must accept strings as long as 10000 characters
* It has to have CMake or Makefile to be able to easily build the executable

### What does this benchmark do?
It runs in three steps:
1) Calculates the average time of hashing every line of "Konstitucija.txt" file.
2) Calculates similarity score, time and collision number of pair of random strings that differ with one char
3) Calculates similarity score, time and collision number of pair of random strings

### How to run the benchmark
There are two main ways to do it:
1) The easy one: contact me at: `dom.seputis@gmail.com` and request me to run the benchmark for you in my machine (must submit the link to yours repository). Keep in mind that if there will be a lot of request I might not be able to run benchmark because of the shortage of time.
2) The longer, but more pleasant one (for me :D):  
* You need to setup `Python3` in your machine.
* Need to install progress bar module by running `$ pip / pip3 install tqdm`
* Build your executable by running `$ sh build.sh` and `clean.sh` to clean the directory.
* Run `$ python3 rank.py <name of the executable>`
* Add your results to the table below

To submit your results just make PR with your entry in the table below:

**Legend**
`A` - Average hashing time of "Konstitucija.txt"  
`B` - Letter collision test time  
`C` - Letter collision similarity average  
`D` - Number of collisions found in Letter test  
`E` - Word collision test time  
`F` - Word collision similarity average  
`G` - Number of collisions found in Word test  

| Github nick | Link to the repo | A      | B         | C      | D    | E          | F      | G |
|-------------|------------------|--------|-----------|--------|------|------------|--------|---|
| dqmis       | dqmis/vuhash     | 0.0052 | 1417.6514 | 0.1108 | 9917 | 1497.0956s | 0.0056 | 0 |
|             |                  |        |           |        |      |            |        |   |
|             |                  |        |           |        |      |            |        |   |
