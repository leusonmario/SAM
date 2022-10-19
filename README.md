# Semantic analysis merge tool  

The semantic analysis merge(SAM) tool can be used to identify behaviour changes, that are caused by semantic conflicts after changes in the same region of the code. 

### Requirements

- Java 8
- Maven
- Python3
- Setup `JAVA_HOME` and `MAVEN_HOME` environment variables

### Installation

to install the semantic analysis merge tool in your local repository, simply run  
`./setup.sh ${path_to_your_repository}`


# Workflow

![SAM flow](https://i.imgur.com/N2GQRHL.png)

The post merge hook is called after the commit is done and there is already a generated merge commit.  
By comparing the parents and the ancestor of this merge commit, its possible to find mutual changes on functions and check if there was a behaviour change by executing test cases.

### References
[DiffJ](https://github.com/jpace/diffj)  
[Osean](https://github.com/spgroup/OSean.EX)  
[SMAT](https://github.com/spgroup/SMAT)  
