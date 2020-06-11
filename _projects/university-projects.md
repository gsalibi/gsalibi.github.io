---
layout: project
title: University Projects
description: Projects developed in several disciplines
year: 2016/2017/2018/2019/2020
thumbnail: /assets/img/projects/unicamp.png
---

<img class="img-project" src="/assets/img/projects/unicamp.png" alt="Unicamp" />

<br>
<br>

Here I share projects that I have done for some subjects in the computer science course.

<br>
<ul>
    <li><a href="#artificial-intelligence-2019">Artificial Intelligence (2019)</a>
        <ul>
            <li><a href="#project-1---graph-search-algorithms">Project 1 - Graph Search Algorithms</a></li>
            <li><a href="#project-2---genetic-algorithms-in-optimization-of-rfid-antenna-readings">Project 2 - Genetic Algorithms in Optimization of RFID Antenna Readings</a></li>
            <li><a href="#project-3---control-algorithm-for-autonomous-robot-using-fuzzy-systems">Project 3 - Control Algorithm for Autonomous Robot Using Fuzzy Systems</a></li>
            <li><a href="#project-4---face-recognition">Project 4 - Face Recognition</a></li>
        </ul>
    </li>
    <li><a href="#introduction-to-digital-image-processing-2019">Introduction to Digital Image Processing (2019)</a></li>
    <li><a href="#databases-2018">Databases (2018)</a></li>
    <li><a href="#software-engineering-2018">Software Engineering (2018)</a></li>
    <li><a href="#computer-organization-and-assembly-2018">Computer Organization and Assembly (2018)</a></li>
    <li><a href="#design-and-analysis-of-algorithms-2017">Design and Analysis of Algorithms (2017)</a></li>
    <li><a href="#data-structures-2016">Data Structures (2016)</a></li>
</ul>
<br>

## Artificial Intelligence (2019)

<p class="right"> *Used languages: Python and C#* </p>

This course was taken in the first semestre of 2019 at Unicamp. You can find the complete project in <a
    href="https://github.com/gsalibi/artificial-intelligence-course" target="_blank">this repository</a>.
Introductory study of the fundamentals and applications of Artificial Intelligence. History and principles of AI.
Problem solving. Knowledge representation. Applications. The following topics have been covered:

- AI history and principles
- Smart agents
- Search without information, search with information and competitive search.
- Genetic algorithms
- Constraint satisfaction problem
- Evolutionary computing
- Planning
- Fuzzy systems
- Uncertainty and Bayesian Networks
- Machine learning
- Learning models (supervised, unsupervised and semi-supervised)
- Decision trees
- Neural networks
- Markov Models and Reinforcement Learning
- AI topics

As a complement to the course, we had to implement 4 projects that are described below.


##### Project 1 - Graph Search Algorithms

There are several algorithms that can be used to automate the process of finding a minimum path between two points.
Thus, this work aims to compare some of these possibilities (Breadth First Search, Uniform Cost Search, A * and
Greedy) using different heuristics through maps generated randomly where a point A (red) must reach a point B (blue).
<a href="https://github.com/gsalibi/artificial-intelligence-course/tree/master/Project%201" target="_blank">You can find
    the codes used in this project here</a>.

<img class="img-project" src="/assets/img/projects/p1-a.png" alt="Graph Search A*" style="max-width: 600px" />
<br>
<img class="img-project" src="/assets/img/projects/p1-b.png" alt="Graph Search Greedy" style="max-width: 600px" />
<br>

##### Project 2 - Genetic Algorithms in Optimization of RFID Antenna Readings

For RFID antennas to work properly, the parameter settings of the modules must be well selected.
However, given the nature of the problem, this is not feasible to do by testing all possibilities.
In the search for brute force, an algorithm with an order of complexity **O(101<sup>n</sup>)** would be necessary, with
n = 31, in the simulation used in this project.
Thus, genetic algorithms were used in search of the ideal configuration result.
Different parameters were used in the algorithm, producing different solutions.
The results obtained solve the problem in different ways and are, in general, quite satisfactory.
**Our best algorithm achieved the ideal result in just 21s:38ms.** <a
    href="https://github.com/gsalibi/artificial-intelligence-course/tree/master/Project%202" target="_blank">You can
    find the codes used in this project here</a>.
<br>

##### Project 3 - Control Algorithm for Autonomous Robot Using Fuzzy Systems

Robots, sensors and scenarios were simulated using the V-REP software. Different scenarios were created so that the
robot could achieve objectives by avoiding obstacles. <a
    href="https://github.com/gsalibi/artificial-intelligence-course/tree/master/Project%203" target="_blank">You can
    find
    the codes used in this project here</a>.

<img class="img-project" src="/assets/img/projects/p3.jpg" alt="Control Algorithm for Autonomous Robot Using Fuzzy Systems" style="max-width: 600px" />
<br>

##### Project 4 - Face Recognition

This work addresses the problem of face recognition in images through a regression tree algorithm using landmarks.
This project shows how the model was trained and evaluated. It also shows some practical applications.

Given a single photo and an associated name, the algorithm is able to recognize that person in other photos or videos,
even in real time. <a
    href="https://github.com/gsalibi/artificial-intelligence-course/tree/master/Project%204%20-%20Final"
    target="_blank">You can find
    the codes used in this project here</a>.

<img class="img-project" src="/assets/img/projects/p4-a.png" alt="Recognized faces" style="max-width: 600px" />
<br>

<img class="img-project" src="/assets/img/projects/p4-b.png" alt="Recognized faces" style="max-width: 600px" />
<br>

<hr>

<br>

## Introduction to Digital Image Processing (2019)

<p class="right"> *Used language: Python* </p>

This course was taken in the first semester of 2019 at Unicamp. You can find the complete project in <a
    href="https://github.com/gsalibi/introduction-to-digital-image-processing-course" target="_blank">this repository</a>.
**objectives:** to present theoretical and practical aspects related to the image processing area. Describe techniques for image acquisition, transformation and analysis using a computer. The following topics have been covered:

- Introduction
  - Representation of digital images
  - Componentes of image processing system
  - Application areas
- Fundamentals of Digital Images
  - Human visual system
  - Image formation
  - Sampling and quantization
  - Spatial resolution and image depth Basic pixel relationships (neighborhood, connectivity, adjacency, path, distance measurements, related components)
  - Noise in images
- Image Enhancement Techniques
  - Image quality
  - Gray scale transformation
  - Histogram of images
  - Correlation and convolution operations
  - Spatial domain filtering
  - Frequency domain filtering
- Image Segmentation
  - Discontinuity detection
  - Edge detection
  - Threshold (global and local)
  - Region-based segmentation
- Representation and Description
  - Representation schemes (chain code, polygonal approximations, signatures, skeleton of a region)
  - Descriptors (basic descriptors, Fourier descriptors, moments, regional descriptors, texture)
  - Mathematical Morphology
- Image Compression
  - Fundamentals of image compression (coding redundancy, interpixel redundancy, psychovisual redundancy)
  - Lossless compression
  - Lossy compression
- Image Registration
  - Geometric transformations
  - Spatial transformations
  - Image interpolation
  - Correspondence between images
- Image Classification (TRABALHO 5)
  - Image analysis elements
  - Patterns and pattern classes
  - Decision methods (marriage, statistical classifiers, neural networks, fuzzy logic)

Projects:  
- <a href="https://github.com/gsalibi/introduction-to-digital-image-processing-course/tree/master/Project%200" target="_blank">Project 0 - Fundamentals of digital images</a>  
- <a href="https://github.com/gsalibi/introduction-to-digital-image-processing-course/tree/master/Project%201" target="_blank">Project 1 - Filtering</a>  
- <a href="https://github.com/gsalibi/introduction-to-digital-image-processing-course/tree/master/Project%202" target="_blank">Project 2 - Color quantization</a>  
- <a href="https://github.com/gsalibi/introduction-to-digital-image-processing-course/tree/master/Project%203" target="_blank">Project 3 - Morphological operators for segment text regions</a>  
- <a href="https://github.com/gsalibi/introduction-to-digital-image-processing-course/tree/master/Project%204" target="_blank">Project 4 - Detection of common points to create panoramic images</a>  
- <a href="https://github.com/gsalibi/introduction-to-digital-image-processing-course/tree/master/Project%205" target="_blank">Project 5 - Machine Learning for Image Color Reduction</a>

<br>

<img class="img-project" src="/assets/img/projects/c2-1.jpg" alt="Color quantization" style="max-width: 600px" />
<p class="center">Project 2 - This image was produced using only two colors (black and white), with no other shades of gray</p>
<br>

<hr>

<br>

## Databases (2018)

<p class="right"> *Used language: MySQL* </p>

This course was taken in the first semester of 2018 at Unicamp. You can find the complete project in <a
    href="https://github.com/gsalibi/databases-course" target="_blank">this repository</a>.
The following topics have been covered:

- Introduction - database management architecture
- Data models: introduction to the concepts of data modeling, conceptual and logical models, including relational models and normalization
- Application design based on conceptual models
- The relational model: definitions and formalization
- Mapping the ER model to the relational model; mapping between models, from conceptual to physical
- Processing of queries in relational algebra
- Query optimization
- Transaction processing - Protection, concurrency control and recovery
- Non-strictly relational database systems
- Development of practical projects

Projects:
- <a href="https://github.com/gsalibi/databases-course/tree/master/T1" target="_blank">Project 1 - Business logic and entity–relationship model
</a>  
- <a href="https://github.com/gsalibi/databases-course/tree/master/T2" target="_blank">Project 2 - Improvement, MySQL development and documentation</a>  
- <a href="https://github.com/gsalibi/databases-course/tree/master/T3" target="_blank">Project 3 - Complete system implementation and elaboration and use of complex queries.</a>  

<br>

<img class="img-project" src="/assets/img/projects/c3-1.jpg" alt="Entity–relationship model" style="max-width: 600px" />
<p class="center">Entity–relationship model</p>

<br>

<hr>

<br>

## Software Engineering (2018)

<p class="right"> *Used languages: UML and Java* </p>

This course was taken in the first semester of 2018 at Unicamp. The following topics have been covered:

- Software Engineering Paradigms
- Agile Methodologies
- Software Processes
- Software Process Models
- Requirements Extraction and Specification
- Analysis and Design of Software Systems
- Architecture Patterns and Design Patterns

Although this is a design-oriented discipline, a system has been implemented in the past few weeks using java and can be found <a href="https://github.com/gsalibi/software-engineering-course" target="_blank">here</a>.

<br>

<img class="img-project" src="/assets/img/projects/c4-1.png" alt="Software engineering project" style="max-width: 600px" />

<br>

<hr>

<br>

## Computer Organization and Assembly (2018)

<p class="right"> *Used languages: Assembly(ARM and LEG)* </p>

This course was taken in the first semester of 2018 at Unicamp. You can find the complete project in <a
    href="https://github.com/gsalibi/computer-organization-and-assembly-course" target="_blank">this repository</a>.
The following topics have been covered:

- Computer history
- Basic computer organization
- Memory and addressing. Representation of information in memory
- Introduction to processor architecture
- Set of instructions: access to memory, arithmetic, logic and shift operations, procedures and functions
- Assembly Language Programming, using two sets of instructions: LEG and ARM processors
- Relationship with high-level languages, rudiments of compilation: implementation of efficient repetitions, data structures, passing parameters, function return values, object orientation
- Input / Output instructions, interruptions and access to peripherals
- Assemblers, connectors and loaders

Projects:
- Several tasks have been programmed in the ARM and LEG languages and can be found <a href="https://github.com/gsalibi/computer-organization-and-assembly-course" target="_blank">here</a>.

<br>

<img class="img-project" src="/assets/img/projects/c5-1.png" alt="Entity–relationship model" style="max-width: 600px" />
<p class="center">ARM code</p>

<br>

<hr>

<br>

## Design and Analysis of Algorithms (2017)

<p class="right"> *Used language: C++* </p>

This course was taken in the second semester of 2017 at Unicamp. **objectives:** To analyze the correctness and complexity of algorithms in a formal way. Model common problems and subproblems. Design and develop algorithms using classical techniques. The following topics have been covered:

- Introduction
- Algorithm complexity
- Correction of algorithms
- Design of algorithms by induction and divide-and-conquer
- Sorting algorithms
- Introduction to randomized algorithms and ordering by partitioning
- Linear time ordering
- Order statistics
- Dynamic programming
- Greedy algorithms

Although this course is much more theoretical and mathematical, some practical projects have been implemented in C ++ and can be found <a href="https://github.com/gsalibi/design-and-analysis-of-algorithms-course" target="_blank">here</a>.

<br>

<hr>

<br>

## Data Structures (2016)

<p class="right"> *Used languages: C* </p>

The following topics have been covered:

- Basic data representation structures
  - Abstract Data Type
    - **contents:** dynamic memory allocation; use of pointing variables and vectors; abstract data type definition
    - **objectives:** to allocate data dynamically; abstract complex structures by separating data, operations and implementation
  - Connected Structures, Notions of Efficiency
    - **contents:** node; asymptotic notation
    - **objectives:** to create lists dynamically; calculate the efficiency of simple algorithms
  - List operations and variations
    - **contents:** circular lists, double linked lists, operations
    - **objectives:** to implement operations and list variants
  - Stacks and Queues
    - **contents:** dynamic set; collection removal policies; stacks application
    - **objectives:** to identify real situations that can be modeled as stacks and queues
- Recursive programming techniques
  - Recursion
    - **contents:** simple recursion; efficiency of recursive algorithms; call stack
    - **objectives:** simulate recursion using call stack
  - Divide-and-conquer
    - **contents:** recursive sorting algorithms: merge-sort and quick-sort
    - **objectives:** to solve subproblems recursively using divide-and-conquer
  - Backtracking
    - **contents:** N-queens problem; partial problem solution; backtracking troubleshooting
    - **objectives:** to identify subproblems; solve subproblems recursively using backtracking
- Dynamic sets on trees
  - Trees
    - **contents:** binary tree
    - **objectives:** represent structures and sets hierarchically
  - Binary Search Trees
    - **contents:** search, insertion and removal in binary search trees
    - **objectives:** to implement dynamic sets in a binary tree
  - Balanced Trees
    - **contents:** AVL tree
    - **objectives:** to implement dynamic sets in a binary tree efficiently
  - Splay Tree
    - **contents:** splay tree; principle of locality and reference
    - **objectives:** to identify situations in which the principle of locality and reference can be used to improve the efficiency of a program
  - B-Tree
    - **contents:** B-tree; disk page and latency concepts
    - **objectives:** to implement dynamic assembly in permanent storage medium
  - Priority queues and heap-sort
    - **contents:** max-heap; heap-sort ordering method
    - **objectives:** to implement operation with maximum efficiency
  - Prefix Tree and Huffman Encoding
    - **contents:** dictionary; coding; Huffman's algorithm
    - **objectives:** apply priority queue; get Huffman coding
  - Evaluation of data structures for dynamic sets
    - **contents:** overview of trees
    - **objectives:** evaluate the best algorithm and data structure for problems with dynamic data set
- Advanced data structures
  - Hashing
    - **contents:** hashing function, hash table
    - **objectives:** to implement dynamic set in almost constant time
  - Graphs
    - **contents:** definition of graphs; graph terminology
    - **objectives:** to identify situations that can be modeled with graphs
  - Graph representation
    - **contents:** representation of graphs in memory: adjacency list and adjacency matrix; depth first search and breadth first search
    - **objectives:** to implement basic operations with graphs
  - Graph algorithms
    - **contents:** shortest path algorithm (Dijkstra); topological sorting
    - **objectives:** apply classic graph algorithms to real problems
  - Generalized lists and general tree
    - **contents:** generalized lists: atom, list; general tree
    - **objectives:** to interpret data structures as generalized lists
  - Memory management
    - **contents:** free list; peer system; garbage collection; reference count
    - **objectives:** to understand dynamic allocation implementations and their interference with data structure

Some projects can be found <a href="https://github.com/gsalibi/data-structures-course" target="_blank">here</a>.