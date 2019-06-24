## Parsing raw text files into JSON and XML formats

In simple terms, this project is a demonstration of the varied use of regular expressions in identifying patterns to extract data from a raw text file and process it into meaningful formats such as XML and JSON. This exercise depicts the use of positive-negative look aheads, capturing and non capturing groups etc. 

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

#### XML Format: 
<br/>

```html
<listings>
	<listing id="20389">
		<title>
		N/A
		</title>
		<location>
		Yerevan, Armenia
		</location>
		<job_descriptions>
			<description>
			The purpose of this post is to assist in the management
			and coordination of Armenia Country Office grants portfolio, including
			partner agreements and ensure that Armenia programme adheres to all its
			grant management obligations internally within Save the Children and
			externally with donors
			</description>
			<description>
			The position will also act as a key liaison and
			support point in relation to financial management of grants and budget
			monitoring.
			</description>
		</job_descriptions>
		<job_responsibilities>
			<responsibility>
			Develop Flash-powered web applications, charts/ diagrams with
			ActionScript;
			</responsibility>
			<responsibility>
			Plot graphical charts in ActionScript language for provided XML data;
			</responsibility>
			<responsibility>
			Participate in creative brainstorms and provide support for design
			tasks;
			</responsibility>
			<responsibility>
			Draft site/page diagrams and participate in the review process;
			</responsibility>
			<responsibility>
			Provide technical support and assistance, if requested.
			</responsibility>
		</job_responsibilities>
		<required_qualifications>
			<qualification>
			Demonstrate the ability to juggle multiple projects simultaneously;
			</qualification>
			<qualification>
			Experience in writing and editing;
			</qualification>
			<qualification>
			Photo editing or multi-media experience is a plus;
			</qualification>
			<qualification>
			Bachelor"s degree required with 1-2 professional experience
			(post-undergrad);
			</qualification>
			<qualification>
			Experience in a fast-paced corporate or agency environment preferred,
			as is experience with Adobe PhotoShop, Adobe PageMaker or QuarkExpress,
			Macromedia Dreamweaver, Macromedia Fireworks, WebTrends, and/or HTML.
			</qualification>
			<qualification>
			English fluency; second language capabilities strongly preferred.
			</qualification>
		</required_qualifications>
		<salary>
		 Competitive

		</salary>
		<application_procedure>
		All applications must be submitted either in
		English or Russian languages; and saved in either MS Word or Adobe PDF
		format. Please be sure that your application includes the following: 
		- Cover letter mentioning the full job title you are applying for
		(maximum 1 page);
		- Current Resume or Curriculum Vitae (CV) with a passport size photo;
		- Names and contact information of two referees.
		Please, as a title of letter put the position"s name you"re applying
		for: 
		Please submit your applications to: hr@..., or deliver hard copy
		version to: 20 Kurghinyan Str., Araratyan dst. 2, Yerevan 0068, Republic
		of Armenia.
		Please clearly mention in your application letter that you learned of
		this job opportunity through Career Center and mention the URL of its
		website - www.careercenter.am, Thanks.
		</application_procedure>
		<start_date>
		28 March 2014
		</start_date>
		<application_deadline>
		31 August 2010
		</application_deadline>
		<about_company>

		 The USAID funded Armenia Legislative Strengthening
		Program (ALSP) is being implemented together by prime contractor,
		Development Associates, Inc. (DA) and subcontractor, Development
		Alternatives, Inc. (DAI). The project was extended beginning September
		1, 2004 for an additional three year period with concentration of
		activities on working with and engaging the National Assembly of the
		Republic of Armenia to be more inclusive of the legislative community in
		all of its activities as well as to improve the substantive legislation
		being drafted and adopted. The Program is part of USAIDs strategic
		mandate to: ""create a more responsive and effective Parliament"" and
		""expand civic participation"".

		</about_company>
	</listing>
</listings>
```

#### JSON Format
<br/>

```json
{
	"listings": {
		"listing": [
			{
				"_id": "29711", 
				"title": "Head of Corporate Customers Relationship Management Division", 
				"location": "Yerevan, Armenia", 
				"job_description": {
					"description": [
						"The ""Clean Energy and Water"" (CEW) Program is a four-year initiative funded by the US Agency for International Development", 
						"The objective of the Program is to assist sustainable management of water and energy sectors in the Republic of Armenia (RA). Within the framework of the Program, technical assistance will be provided to the RA Government to build river basin management planning capacities in Armenia", 
						"Particularly, as part of the assistance in Vorotan river basin management planning, biological monitoring will be implemented, which will also include description and assessment of ecological status of water bodies in the river basin, in accordance with the RA legislation and Guidelines of the EU Water Framework Directive, as implementation of the international best practice", 
						"Under this Statement of Work, the activities will be implemented according to the following tasks:"
					]
				}, 
				"job_responsibilities": {
					"responsibility": [
						"Develop software using .NET;", 
						"Be responsible for project architecture design;", 
						"Be responsible for dedicated server and clients configuration;", 
						"Research work when required;", 
						"Follow team lead, system architecture and Tech Lead in designing the systems."
					]
				}, 
				"required_qualifications": {
					"qualification": [
						"Higher education;", 
						"At least 2 years of work experience in programming. REMUNERATION/"
					]
				}, 
				"salary": " High salary is guaranteed ", 
				"application_procedure": "Please submit your resumes to:http://tbe.taleo.net/NA6/ats/careers/requisition.jsp?org=QUESTRADE&cws=1&rid=223 Please clearly mention in your application letter that you learned of this job opportunity through Career Center and mention the URL of its website - www.careercenter.am, Thanks.", 
				"start_date": "12 July 2005", 
				"application_deadline": "14 October 2014, 18:00", 
				"about_company": "  According to Brown-Wilson Group Survey* EPAM Systems is the #1 software engineering outsourcing services provider in Central and Eastern Europe. Founded in 1993, EPAM maintains North American headquarters in Lawrenceville, NJ.  Currently there are 3500+ highly qualified IT professionals working at EPAM Systems. EPAM software development centers are located in Russia, Hungary, Belarus, Ukraine and Armenia. The company continues its growth and development.   Our mission is: ""Delivering excellence in software engineering"" to the benefit of our clients. *http://www.theblackbookofoutsourcing.com/top10itooffshoreeasterncentraleurope.html "
			}
		]
	}
}
```
