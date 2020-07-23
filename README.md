# SysFor

Implementation of the decision forest algorithm SysFor, which was published in:

*Md Zahidul Islam and Helen Giggins: Knowledge Discovery through SysFor - a Systematically Developed Forest of Multiple Decision Trees In: Ninth Australasian Data Mining Conference, 195-204, 2011.*

This decision forest algorithm is designed to build a forest consisting of high accuracy decision trees. It uses gain ratio as the selection criteria. The general structure of "SysFor.java" is taken from "MetaCost.java".  The default parameter settings are the ones used in the SysFor paper.

## Changes
* This implementation uses the J48 implementation of C4.5. Since J48 does not require a setting for minimum gain ratio, this SysFor implementation also does not require it. 
* The original SysFor paper contained some voting techniques for classification that are not implemented here. Instead, majority voting is used.

## BibTeX
```
@inproceedings{Islam:2011:KDT:2483628.2483650,
 author = {Islam, Zahidul and Giggins, Helen},
 title = {Knowledge Discovery Through SysFor: A Systematically Developed Forest of Multiple Decision Trees},
 booktitle = {Proceedings of the Ninth Australasian Data Mining Conference - Volume 121},
 series = {AusDM '11},
 year = {2011},
 isbn = {978-1-921770-02-9},
 location = {Ballarat, Australia},
 pages = {195--204},
 numpages = {10},
 url = {http://dl.acm.org/citation.cfm?id=2483628.2483650},
 acmid = {2483650},
 publisher = {Australian Computer Society, Inc.},
 address = {Darlinghurst, Australia, Australia},
 keywords = {classification algorithm, data mining, multiple decision tree, prediction accuracy},
}
```

## Installation

Either download SysFor from the Weka package manager, or download the latest release from the "Releases" section on the sidebar of Github. A video of how to install and use the package can be found [here](https://www.youtube.com/watch?v=DQKKdAahDgE&t=1s).

## Compilation / Development

Set up a project in your IDE of choice, including weka.jar as a compile-time library.

## Valid options are:
`-L <minimum records in leaf>`
Set minimum number of records for a leaf. (default 10)

-N <no. trees>` 
Set number of trees to build. (default 60)

-G <goodness threshold>` 
Set goodness threshold for attribute selection. (default 0.3)

-S <separation threshold>` 
Set separation threshold for split point selection. (default 0.3)

-C <confidence factor>` 
Set confidence for pruning. (default 0.25)

