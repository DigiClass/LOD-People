Project title: Persons and Names of the Middle Kingdom


URL: https://pnm.uni-mainz.de/info


Description: A selection of persons obtained from the project's sparql endpoint https://pnm.uni-mainz.de/sparql
See also dataset under http://dx.doi.org/10.5281/zenodo.1411391 and decription of the data model under https://pnm.uni-mainz.de/ontology/

Source code and documentation also on Github: 
* https://github.com/ailintom/persons-names-MK for the web application and the SQL database
* https://github.com/ailintom/persons-names-MK-rdf for the SPARQL endpoint and RDF representation

The following SPARQL query was used to obtain the sample data: 

```Turtle
prefix pnm: <https://pnm.uni-mainz.de/ontology#>
prefix skos: <http://www.w3.org/2004/02/skos/core#>
prefix lawd: <http://lawd.info/ontology/>
prefix crm: <http://www.cidoc-crm.org/cidoc-crm/>
prefix dcterms: <http://purl.org/dc/terms/>
prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>
prefix crmeh: <http://purl.org/crmeh#>
prefix pav: <http://purl.org/pav/2.0/>
prefix ontolex: <http://www.w3.org/ns/lemon/ontolex#>
prefix geo: <http://www.w3.org/2003/01/geo/wgs84_pos#>
prefix xsd: <http://www.w3.org/2001/XMLSchema#>

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>

CONSTRUCT { ?instance rdf:type ?type;
            pnm:lived ?life ;
            ?b ?name .
           ?life ?a ?c .
           ?bond a pnm:persons_bond ;
           ?e ?instance ;
           ?g ?h .
           ?statement pnm:refers_to ?instance ;
                      ?ee ?f .
           ?attestation pnm:has_identity_statement ?statement ;
                        ?m ?n .
           ?attbond a pnm:attested_bond ;
                      ?o ?attestation ;
                      ?p ?q;
           
}
where { 
  ?instance rdf:type crm:E21_Person;
            pnm:lived ?life ;
            ?b ?name .
           ?life ?a ?c .
           ?bond a pnm:persons_bond ;
           ?e ?instance ;
           ?g ?h .
           ?statement pnm:refers_to ?instance ;
                      ?ee ?f .
           ?attestation pnm:has_identity_statement ?statement ;
                        ?m ?n .
           ?attbond a pnm:attested_bond ;
                      ?o ?attestation ;
                      ?p ?q;
           
}
 LIMIT 6000000
```

The sample data does not include data on inscriptions, objects, bibliography, find groups, and many other entities contained in the dataset.

License: CC BY 4.0


Contact Person: Alexander Ilin-Tomich ailintom@uni-mainz.de


Data format ttl
 

