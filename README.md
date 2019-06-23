## Parsing raw text files into JSON and XML formats

### Input Data Format:
The input data consists of a list of resumes in a raw text format:

A single resume takes the following form:
<br/>

<pre>
D: 29711
JOB_PROC: Please submit your resumes to:http://tbe.taleo.net/NA6/ats/careers/requisition.jsp?org=QUESTRADE&cws=1&rid=223
Please clearly mention in your application letter that you learned of
this job opportunity through Career Center and mention the URL of its
website - www.careercenter.am, Thanks.
DEAD_LINE: 14 October 2014, 18:00
JOB_T: Head of Corporate Customers Relationship Management Division
OPEN TO/
DATE_START: 12 July 2005
JOB_LOC: Yerevan, Armenia
REQUIRED QUALIFICATIONS:
- Higher education;
- At least 2 years of work experience in programming.
REMUNERATION/
ABOUT COMPANY:
 According to Brown-Wilson Group Survey* EPAM Systems is
the #1 software engineering outsourcing services provider in Central and
Eastern Europe. Founded in 1993, EPAM maintains North American
headquarters in Lawrenceville, NJ. 
Currently there are 3500+ highly qualified IT professionals working at
EPAM Systems. EPAM software development centers are located in Russia,
Hungary, Belarus, Ukraine and Armenia. The company continues its growth
and development.  
Our mission is: ""Delivering excellence in software engineering"" to the
benefit of our clients.
*http://www.theblackbookofoutsourcing.com/top10itooffshoreeasterncentraleurope.html
SALARY: High salary is guaranteed
JOB DESCRIPTION: The ""Clean Energy and Water"" (CEW) Program is a
four-year initiative funded by the US Agency for International
Development. The objective of the Program is to assist sustainable
management of water and energy sectors in the Republic of Armenia (RA).
Within the framework of the Program, technical assistance will be
provided to the RA Government to build river basin management planning
capacities in Armenia. Particularly, as part of the assistance in Vorotan
river basin management planning, biological monitoring will be
implemented, which will also include description and assessment of
ecological status of water bodies in the river basin, in accordance with
the RA legislation and Guidelines of the EU Water Framework Directive, as
implementation of the international best practice. Under this Statement
of Work, the activities will be implemented according to the following
tasks:
RESP:
- Develop software using .NET;
- Be responsible for project architecture design;
- Be responsible for dedicated server and clients configuration;
- Research work when required;
- Follow team lead, system architecture and Tech Lead in designing the
systems.
------------------------------
</pre>

### Output Data Format:
