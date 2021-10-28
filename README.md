# Consistency Maintenance Clone Dataset
## 1. Content
```
├── basic_info.csv
├── consistent.csv
├── inconsistent.csv
├── json
│   ├── project1
│   └── project2
│   └── ...
└── web
    ├── CloneCoChange.html
    ├── js
    │   ├── d3.v3.js
    │   ├── jquery-3.3.1.js
    │   └── main.js
    ├── ...
    └── res
```

## 2. Basic Information

​		The resource in this repository is a dataset which contains 24,672 piars of consistently changed clone instances and 38,041 non-consistently changed clone instances.

​		The dataset was collected from 51 popular open-source Java projects. Detail information of these projects was shown at the end of this file. `basic_info.csv` contains detail information of these projects.

​		`consistent.csv`and `inconsistent.csv` contains consistently changed and inconsistently changed data seperately.

​		`json` folder contains the resource file of each project.

​		`web` folder contains a web project which could be used to show the genealogy of the clone pair.

### 2.1 Consistently and non-consistently changed clone instances
​		File ```consistent.csv```(or ```inconsistent.csv```) constain all the consistently(or inconsistently) changed clone pair. The meanings of the header was listed below:
+ project: which project does the data comes
+ groupId: the group id of the clone pair from which the data extracted
+ clone type: the type of the clone pair before changed
+ consistId: incremental id of the dataset
+ consistGroup: ids of the consistently changed clone instances. In one certain clone pair genealogy, the entity of the clone instance in each revision was given an unique number. Suppose a consisGroup like 3#4, if it is a consistently changed pair, it means that instance marked as 3 and instantce marked as 4 both experienced the same change, if it is a inconsistently changed pair, it means that instance marked as 3 changed while instance marked as 4 experenced a different change or no changed.
+ fileNum: 1 means the clone pair located in the same file, 2 means the clone pairs located in diffrerent files.
### 2.2 Resouce of the dataset
​		The genealogy of each clone pair was stored in json file, which could be visualized in the web page. Here gives an instruction of the usage of these resource.

[![5LOvPP.png](https://z3.ax1x.com/2021/10/28/5LOvPP.png)](https://imgtu.com/i/5LOvPP)

​		Figure above show a consistently changed clone pair from dbeaver. It was extracted from the genealogy of clone pair 10585. Before changed, the clone pair was a type2 clone and the two instances were located in the same source file.
Then, we open the web page CloneCoChange.html, select dbeaver and input 10585, the web show a page as the picture below.

[![5LX2QS.png](https://z3.ax1x.com/2021/10/28/5LX2QS.png)](https://imgtu.com/i/5LX2QS)

​		The picture above shows a clone genealogy of clone pair 10585. Each column presents a evolution timeline of the one clone instance, each row presents the source code of the two clone instance at the relavent revision. 

​		As shown in the figure, the ids of the consistently changed instances was marked by blue circle, meaning that these two codes was changed consistently.

