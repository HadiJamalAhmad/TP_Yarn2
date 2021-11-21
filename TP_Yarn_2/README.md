# TP Yarn 2
```s
Hadi Jamal Ahmad

```

# 1.6.1

```s

[hadi.jamal-ahmad@hadoop-edge01 ~]$ ls
]
davinci.txt
dog
emptyfile.txt
hadoop-examples-mapreduce-1.0-SNAPSHOT.jar
hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar
mapper.py
message.txt
reducer.py
secret-of-the-universe.txt
sudoku.dta
The_Notebooks_of_Leonardo_Da_Vinci.txt
The_Outline_of_Science_Volume_1.txt
trees.csv
trees.csv.1
TreesMapper.java
TreesReducer.java
Ulysses.txt
[hadi.jamal-ahmad@hadoop-edge01 ~]$

```


# 1.6.3

```s

[hadi.jamal-ahmad@hadoop-edge01 ~]$ yarn jar hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar wordcount davinci.txt user/hadi.jamal-ahmad


[hadi.jamal-ahmad@hadoop-edge01 ~]$ hdfs dfs -cat user/hadi.jamal-ahmad/part-r-000                                                         00
"";     2
"Load   1
"en";   1
"http://www.gutenberg.org/ebooks/66579";        1
"screen";       1
&amp;   2
(This   1
(no     2
(with   2
-       1
-->     4
--><html        1
.icon   1
.qrcode 1
//</script>     1
0       4
15,     1
1884    1
20,     1
2021</td>       1
30      1
320)"   2
46,     1
640,    2
:William        1
<!--    5
<!--<div        1
<!DOCTYPE       1
</a>    8
</body> 1
</colgroup>     2
</div>  24
</div>-->       1
</form> 2
</head> 1
</html> 1
</li>   13
</nav>  1
</span> 2
</span></h2>    1
</span></th>    4
</style>        2
</table>        2
</td>   21
</tr>   12
</tr><tr        5
</tr><tr>       2
</ul>   7
<a      34
<body>  1
<col    5
<col>   4
<colgroup>      2
<div    25
<div>   1
<form   2
<h1     1
<h2     1
<h2>Bibliographic       1
<h2>Download    1
<head>  1
<img    3
<input  9
<label  4
<li     3
<li>    10
<li><a  23
<link   9
<meta   19
<nav>   1
<p><a   1
<script 1
<script>//      1
<span   14
<span>  2
<style> 2
<table  2
<td     47
<td>    3
<td>66579</td>  1
<td></td>       1
<td><span       7
<td>English</td>        1
<th     5
<th></th>       1
<th>Author</th> 1
<th>Category</th>       1
<th>Copyright   1
<th>Credits</th>        1
<th>Downloads</th>      1
<th>EBook-No.</th>      1
<th>Format      1
<th>Language</th>       1
<th>Original    1
<th>Release     1
<th>Title</th>  1
<title>Chambers's       1
<tr     5

the counting continues but i have shorterned it for convinience...

```

...

# 1.8.1  Districts containing trees (very easy)


[hadi.jamal-ahmad@hadoop-edge01 ~]$ yarn jar hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar Districts tree/tree.csv user/hadi.jamal-ahmad/181

[hadi.jamal-ahmad@hadoop-edge01 ~]$ hdfs dfs -cat user/hadi.jamal-ahmad/181/part-r-00000
3       1
4       1
5       2
6       1
7       2
8       5
9       1
11      1
12      29
13      2
14      3
15      1
16      36
17      1
18      1
19      6
20      3


# 1.8.2 Show all existing species (very easy)

 yarn jar hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar treeSpecies  tree/tree.csv user/hadi.jamal-ahmad/182

[hadi.jamal-ahmad@hadoop-edge01 ~]$ hdfs dfs -cat user/hadi.jamal-ahmad/182/part-r-00000
araucana
atlantica
australis
baccata
bignonioides
biloba
bungeana
cappadocicum
carpinifolia
colurna
coulteri
decurrens
dioicus
distichum
excelsior
fraxinifolia
giganteum
giraldii
glutinosa
grandiflora
hippocastanum
ilex
involucrata
japonicum
kaki
libanii
monspessulanum
nigra
nigra laricio
opalus
orientalis
papyrifera
petraea
pseudoacacia
sempervirens
serrata
stenoptera
suber
sylvatica
tomentosa
tulipifera
ulmoides
virginiana
x acerifolia


# 1.8.3 Number of trees by kinds (easy)

[hadi.jamal-ahmad@hadoop-edge01 ~]$ yarn jar hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar treeSpeciesCount  tree/tree.csv user/hadi.jamal-ahmad/183

[hadi.jamal-ahmad@hadoop-edge01 ~]$ hdfs dfs -cat user/hadi.jamal-ahmad/183/part-r-00000
araucana        1
atlantica       2
australis       1
baccata 2
bignonioides    1
biloba  5
bungeana        1
cappadocicum    1
carpinifolia    4
colurna 3
coulteri        1
decurrens       1
dioicus 1
distichum       3
excelsior       1
fraxinifolia    2
giganteum       5
giraldii        1
glutinosa       1
grandiflora     1
hippocastanum   3
ilex    1
involucrata     1
japonicum       1
kaki    2
libanii 2
monspessulanum  1
nigra   3
nigra laricio   1
opalus  1
orientalis      8
papyrifera      1
petraea 2
pseudoacacia    1
sempervirens    1
serrata 1
stenoptera      1
suber   1
sylvatica       8
tomentosa       2
tulipifera      2
ulmoides        1
virginiana      2
x acerifolia    11


# 1.8.4 Maximum height per kind of tree using the average

[hadi.jamal-ahmad@hadoop-edge01 ~]$ yarn jar hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar maxHeightSpecies  tree/tree.csv user/hadi.jamal-ahmad/184

[hadi.jamal-ahmad@hadoop-edge01 ~]$ hdfs dfs -cat user/hadi.jamal-ahmad/184/part-r-00000
araucana        9.0
atlantica       25.0
australis       16.0
baccata 13.0
bignonioides    15.0
biloba  33.0
bungeana        10.0
cappadocicum    16.0
carpinifolia    30.0
colurna 20.0
coulteri        14.0
decurrens       20.0
dioicus 10.0
distichum       35.0
excelsior       30.0
fraxinifolia    27.0
giganteum       35.0
giraldii        35.0
glutinosa       16.0
grandiflora     12.0
hippocastanum   30.0
ilex    15.0
involucrata     12.0
japonicum       10.0
kaki    14.0
libanii 30.0
monspessulanum  12.0
nigra   30.0
nigra laricio   30.0
opalus  15.0
orientalis      34.0
papyrifera      12.0
petraea 31.0
pseudoacacia    11.0
sempervirens    30.0
serrata 18.0
stenoptera      30.0
suber   10.0
sylvatica       30.0
tomentosa       20.0
tulipifera      35.0
ulmoides        12.0
virginiana      14.0
x acerifolia    45.0


# 1.8.5 Sort the trees height from smallest to largest : using average

[hadi.jamal-ahmad@hadoop-edge01 ~]$ yarn jar hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar treesSortedByHeight  tree/tree.csv user/hadi.jamal-ahmad/185

[hadi.jamal-ahmad@hadoop-edge01 ~]$ hdfs dfs -cat user/hadi.jamal-ahmad/185/part-r-00000
3 - Fagus sylvatica (Fagaceae)  2.0
89 - Taxus baccata (Taxaceae)   5.0
62 - Cedrus atlantica (Pinaceae)        6.0
39 - Araucaria araucana (Araucariaceae) 9.0
44 - Styphnolobium japonicum (Fabaceae) 10.0
32 - Quercus suber (Fagaceae)   10.0
95 - Pinus bungeana (Pinaceae)  10.0
61 - Gymnocladus dioicus (Fabaceae)     10.0
63 - Fagus sylvatica (Fagaceae) 10.0
4 - Robinia pseudoacacia (Fabaceae)     11.0
93 - Diospyros virginiana (Ebenaceae)   12.0
66 - Magnolia grandiflora (Magnoliaceae)        12.0
50 - Zelkova carpinifolia (Ulmaceae)    12.0
7 - Eucommia ulmoides (Eucomiaceae)     12.0
48 - Acer monspessulanum (Sapindacaees) 12.0
58 - Diospyros kaki (Ebenaceae) 12.0
33 - Broussonetia papyrifera (Moraceae) 12.0
71 - Davidia involucrata (Cornaceae)    12.0
36 - Taxus baccata (Taxaceae)   13.0
96 - Pinus coulteri (Pinaceae)  14.0
94 - Diospyros virginiana (Ebenaceae)   14.0
68 - Diospyros kaki (Ebenaceae) 14.0
91 - Acer opalus (Sapindaceae)  15.0
5 - Catalpa bignonioides (Bignoniaceae) 15.0
70 - Fagus sylvatica (Fagaceae) 15.0
2 - Ulmus carpinifolia (Ulmaceae)       15.0
98 - Quercus ilex (Fagaceae)    15.0
78 - Acer cappadocicum (Sapindaceae)    16.0
16 - Celtis australis (Cannabaceae)     16.0
28 - Alnus glutinosa (Betulaceae)       16.0
75 - Zelkova carpinifolia (Ulmaceae)    16.0
83 - Zelkova serrata (Ulmaceae) 18.0
23 - Aesculus hippocastanum (Sapindaceae)       18.0
64 - Ginkgo biloba (Ginkgoaceae)        18.0
60 - Fagus sylvatica (Fagaceae) 18.0
8 - Platanus orientalis (Platanaceae)   20.0
20 - Fagus sylvatica (Fagaceae) 20.0
87 - Taxodium distichum (Taxodiaceae)   20.0
12 - Sequoiadendron giganteum (Taxodiaceae)     20.0
51 - Platanus x acerifolia (Platanaceae)        20.0
43 - Tilia tomentosa (Malvaceae)        20.0
35 - Paulownia tomentosa (Paulowniaceae)        20.0
34 - Corylus colurna (Betulaceae)       20.0
15 - Corylus colurna (Betulaceae)       20.0
1 - Corylus colurna (Betulaceae)        20.0
13 - Platanus orientalis (Platanaceae)  20.0
11 - Calocedrus decurrens (Cupressaceae)        20.0
86 - Platanus orientalis (Platanaceae)  22.0
47 - Aesculus hippocastanum (Sapindaceae)       22.0
14 - Pterocarya fraxinifolia (Juglandaceae)     22.0
88 - Liriodendron tulipifera (Magnoliaceae)     22.0
10 - Ginkgo biloba (Ginkgoaceae)        22.0
18 - Fagus sylvatica (Fagaceae) 23.0
31 - Ginkgo biloba (Ginkgoaceae)        25.0
24 - Cedrus atlantica (Pinaceae)        25.0
84 - Ginkgo biloba (Ginkgoaceae)        25.0
92 - Platanus x acerifolia (Platanaceae)        25.0
49 - Platanus orientalis (Platanaceae)  25.0
97 - Pinus nigra (Pinaceae)     25.0
73 - Platanus orientalis (Platanaceae)  26.0
42 - Platanus orientalis (Platanaceae)  27.0
65 - Pterocarya fraxinifolia (Juglandaceae)     27.0
85 - Juglans nigra (Juglandaceae)       28.0
52 - Fraxinus excelsior (Oleaceae)      30.0
29 - Zelkova carpinifolia (Ulmaceae)    30.0
37 - Cedrus libanii (Pinaceae)  30.0
27 - Sequoia sempervirens (Taxodiaceae) 30.0
25 - Fagus sylvatica (Fagaceae) 30.0
54 - Pterocarya stenoptera (Juglandaceae)       30.0
69 - Pinus nigra (Pinaceae)     30.0
41 - Platanus x acerifolia (Platanaceae)        30.0
77 - Taxodium distichum (Taxodiaceae)   30.0
30 - Aesculus hippocastanum (Sapindaceae)       30.0
55 - Platanus x acerifolia (Platanaceae)        30.0
38 - Fagus sylvatica (Fagaceae) 30.0
76 - Pinus nigra laricio (Pinaceae)     30.0
19 - Quercus petraea (Fagaceae) 30.0
72 - Sequoiadendron giganteum (Taxodiaceae)     30.0
59 - Sequoiadendron giganteum (Taxodiaceae)     30.0
22 - Cedrus libanii (Pinaceae)  30.0
9 - Platanus orientalis (Platanaceae)   31.0
80 - Quercus petraea (Fagaceae) 31.0
82 - Platanus x acerifolia (Platanaceae)        32.0
46 - Ginkgo biloba (Ginkgoaceae)        33.0
45 - Platanus orientalis (Platanaceae)  34.0
53 - Ailanthus giraldii (Simaroubaceae) 35.0
17 - Platanus x acerifolia (Platanaceae)        35.0
56 - Taxodium distichum (Taxodiaceae)   35.0
81 - Liriodendron tulipifera (Magnoliaceae)     35.0
57 - Sequoiadendron giganteum (Taxodiaceae)     35.0
40 - Platanus x acerifolia (Platanaceae)        40.0
26 - Platanus x acerifolia (Platanaceae)        40.0
74 - Platanus x acerifolia (Platanaceae)        40.0
90 - Platanus x acerifolia (Platanaceae)        42.0
21 - Platanus x acerifolia (Platanaceae)        45.0


# 1.8.6 District containing the oldest tree (difficult)

[hadi.jamal-ahmad@hadoop-edge01 ~]$ yarn jar hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar oldestTreeDistrictReduce  tree/tree.csv user/hadi.jamal-ahmad/186

[hadi.jamal-ahmad@hadoop-edge01 ~]$ hdfs dfs -cat user/hadi.jamal-ahmad/186/part-r-00000
1601    5

# 1.8.7 District containing the most trees (very difficult)

[hadi.jamal-ahmad@hadoop-edge01 ~]$ yarn jar hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar maxTreesDistrict  tree/tree.csv user/hadi.jamal-ahmad/187

[hadi.jamal-ahmad@hadoop-edge01 ~]$ hdfs dfs -cat user/hadi.jamal-ahmad/187/part-r-00000

16      36

