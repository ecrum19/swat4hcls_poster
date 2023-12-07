# Storing and Querying Personal Genomic Data in Solid Pods
### Elias D. Crum[1,2], Gokhan Ertaylan[1], Ruben Taelman[2], Bart Buelens[1], and Ruben Verborgh [2]
(1: VITO / 2: IDLab, Ghent University)

**Abstract**
Medical care is in the process of being fundamentally transformed, away from a one-size-fits-all approach and toward a personalized, genetically-informed approach. Since the sequencing of the first human genome two decades ago, technological advancements have recently allowed for the cost of sequencing a whole human genome to reach only around 300 euros. In combination with the cost of genome sequencing continually decreasing, research linking genetic data to medical diagnosis and treatment have introduced an augmented approach to medical practice -- personalized medicine. Concurrently, in the modern age of digital data, privacy concerns regarding collection and storage of sensitive personal data, such as personal genome sequence data, has resulted in public debate and legal regulation. Currently, there are many challenges to applying the concepts of personalized medicine to medical practice. Here we identify three such fundamental challenges associated with the storing, querying, and privacy controls of personal genome sequences, a necessary prerequisite of personalized medicine. We also propose a potentially attractive solution involving the Solid ecosystem and Linked-data, especially from the perspectives of patients and clinicians.


**Introduction** Related Work?

Human genome sequencing advancements have allowed for early personalized medicine applications, such as in drug development and prescription as well as in cancer diagnosis and treatment. Examples of these applciations include ... genetics for specific drug prescription or dosing guidelines as well as cancer treatment ... While these approaches have largely been in academic clinical-trials, with the cost of human genome sequencing has decreasing in recent years personalized medicine approaches are becoming more viable for the general population. When paired with ever-increasing documentation of the impacts of specific genetic variations on human health, personal genome sequences (PGS) are becoming an ever more powerful tool within healthcare.

Importantly, as with other health records and data, PGS data is exceedingly private, thus being classified as "sensitive data" in the 2018 European Union's General Data Protection Regulation (GDPR) legislation. Because of the sensitive nature of PGS data, storage, access, and sharing of this data is a pertinent issue. In the context of the practice of personalized medicine, two main perspectives on the issue of PGS data storage and usage are most important -- the patient and the clinician. In existing applicaiton frameworks for storing and querying human genomic data, design features are prioritized for researchers, thus leaving the needs and concerns of non-researchers unfulfilled. 

In this paper, we discuss potential methods of PGS storage, privacy controls, and querying that address current challenges to personalized medicine relevant to both clinicians and patients through the use of the decentralized data storage ecosystem of Solid. 


**Problem Identification**

From the patient perspective, similar to other sensitive personal data, these PGS data will necessitate scalable, efficient, and secure storage, sharing, and querying technologies. Currently, most PGS data is stored in centralized databases that are inaccessible or controllable by patients. Thus, patients rarely have control over who their genomic data can be accessed by, transparency about how or with whom their genoic data is or will be used, nor the ability to access, view, or query their own PGS data. In addition, centralized databases are consistently cited in data leaks where malicious actors are able to gain access and publicize stored sensitive data. 

From the clinician perspective, centrally stored PGS data, because of its sensitive nature, is often stored in data silos where pertinent patient data is not discoverable nor queriable. Additionally, assessing links between various types of data for a single patient or similar data between multiple patients, that may be valuable for a clinician, is nearly impossible due to current data privacy and storage efficiency strategies in centralized databases.

For genomic data to more efficiently inform clinical practice, patient genomic data must be both discoverable and queryable for authenticated individuals and/or applicaitons. From a patient perspective, it would be valuable to have control over who accesses your sensitive genomic data, as well as to control if they want to allow that use. For such a system that prioritizes data privacy, patient control, and performant querying capabilities for clinician-focused applications, An attractive, largely unexplored, solution is presented by the Solid ecosystem. Futhermore, the representation of human genome data, especially clinically relevant data like variant call format (VCF) files, as linked data could improve the usability of genomic data for medical decision making by clinicans. 


**Implementation Considerations**
The proposed framework will have three main components that address the challenges discussed above.

(1) Storing and publishing PGS data in a decentralized environment -- Solid Pod
The storage and display of personal genomic data for the patient will be accomplished using Solid personal data pods. The PGS data will be represented in personal Solid pods as Linked Data fragments thereby making data linkages to other patient data within the same pod, publicly available data in an external database, or linkages to other private patient data of other solid pods discoverable and queryable to those with authorization. Authorization will be able to be controlled by the owner of the pod exclusively. Lastly, the pod will contain an api-like interface that allows for its connection to applications and user interfaces. 


(2) Querying and/or requesting data from the data pod
The personal pod will be queryable and able to return requested information given an authenticated request. The query processing techniques for handling the vast scale of personal genomic data stored within and across Solid data vaults is an area that requires significant investigation. The use of existing open-source query englines like Comunica provide a potentially useful solution due to __. While query algorithms within Comunica may require optimization to for genomic data, the platform offers a proven, performant starting point for such queries. Performance and runtime efficacy of Linked Data querying approaches must be assessed but __. Additionally, query result formatting must be taken into consideration, especially for conneciton to applicaitons that require highly standardized input formats.
        

(3) Standardized data accessing system encouraging universal application by healthcare professionals and software developers 
The overarching goal of such a PGS data storage system involves embedding the PGS storage and accessing system within in the Worldwide/European/Belgian Data Sharing Landscape. To achieve this scalibility, an ontology will be established for RDF conversion that follows existing standardization initiatives such as FHIR / GA4GH (beacons) / ISO Genomics or others. The result would improve the sharibility of such data, with patient permission, to clinicians and researchers alike.

**Conclusion**
The PENGQUIN project aims to propel personalized medicine forward by fostering the development of a secure, efficient, and widely applicable system for personal genome storage and querying within the Solid ecosystem. The PENGQUIN project endeavours to unlock the full potential of personal genomic data storage and querying to help advance personalized healthcare and preventive medicine, ultimately benefiting individuals and the broader healthcare community.

**References**
...

