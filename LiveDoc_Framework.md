# Living Documentation Framework

## Principles

1. There needs to be a <u>*significant*</u> amount of complexity in a <u>*unit of logic*</u> before it is worth documenting and testing

2. Don't write documentation for things that we aren't willing to write a test for

## Usage  

> **Step 1**: Identify why you are producing documentation. What value will it provide to users or team members on a day to day basis? What problem will this documentation solve?

> **Step 2**: Identify the specific chunks of meta data that will solve the problem.     

> **Step 3**: Determine the appropriate location to keep that meta data so that it will be kept up to date with the actual data it is describing.  

> **Step 4**: Identify how users or team members will want to view and interact with the documentation.  i.e. format, style, presentation tool, interactivity

## Framework  

### Definitions   

- Publish To: Where will the documentation be viewed from?  

- Target User: Who will read this documentation?  

- Value: Why is this documentation being written?  

- Category: What keyword will be used to find your documentation?  

- Code Aspect: Where in the source code should this documentation be located?   

- Type: What is the purpose of the referenced Code Aspect that will be explained?  

- Tools: What tools will be used to publish the documentation?   

### Example
| Publish To | Target User | Value | Category | Code Aspect | Type | Tools |
| ---------- | ----------- | ----- | ------------------ | --------- | -------- | ----- |
| User Help Guide | End User wanting to review how the system works | Describe a user story and its assertions | @process, @assertions, @inputs, @outputs | Functional Tests | Scenarios | GitBook |
| In context help text | logged in User currently doing a task | To map the business rules onto the underlying programming logic | @scopes, @assertions, @pre-conditions, @field-constraints | Front end unit tests | Features | React-DocGen, Mark-down |
| Developer guide | Developers, IT Consultants | Because of tools like swagger, doc of functions should limited to explaining exceptions to design convention | @purpose, @parameters, @checks, @returns | Back end logic | Functions | Sphinx, PY Doc |
| Database meta data  | Data Architects, Developers | Because of tools like schema spy, doc of data model should be limited to adding postgresql comments on tables and columns  | @table-comment, @column-comment | Django Model Classes | Data Structure | Schema Spy |
| Data Class-ification File | Privacy Officers, Data Custodians | Privacy Impact Assessments should be based on the currently implemented system | @privacy-classification | Django Model Classes | Data Class-ification | GitBook |
| Deploy-ment Guide | Developers | Instructions for running a dockerfile and what that will produce | @images, @application-instances, @ports, @versions | Dockerfile | Infra-structure | GitBook |
| Deploy-ment Guide | Developers | Instructions for seeding the database with test data and what should be inserted for a given commit in order to create a fully testing instance | @fixtures, @migrations, @version-upgrade | Fixtures and Migrations | Infra-structure | GitBook |
