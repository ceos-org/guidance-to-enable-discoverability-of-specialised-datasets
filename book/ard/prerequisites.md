# Prerequisites


The guidelines can be applied to the various flavours of metadata specifications covered in the remainder of this document.

To apply the above high level requirements, the following information related to CEOS specifications or more precisely CEOS-ARD Product Family specifications should be agreed:

- Document citations, including precise title, date and document identifier (URI)
- Conformance class identifiers (URI) - when used in future specifications.

## Requirements for Citations

The proposed recommendations assume that CEOS-ARD Product Family specifications (PFS) will in the future use identification of documents and conformance classes similar to current OGC practice.

For example, OGC identifies specification documents and conformance classes using URI.

| Specification Title | Version | External identifier (URI) |
|------|-----|-----|
| OGC API - Processes - Part 1: Core | 1.0.0 | http://www.opengis.net/doc/IS/ogcapi-processes-1/1.0 | 
| OGC API - Features - Part 1: Core | 1.0 |  http://www.opengis.net/doc/IS/ogcapi-features-1/1.0 | 

Winthin documents, conformance classes are defined via URI as well.

| Specification Title | Version |  Conformance Class Example | Conformance Class Example (URI)
|------|-----|-----|-----|
| OGC API - Processes - Part 1: Core | 1.0.0  | Core | http://www.opengis.net/spec/ogcapi-processes-1/1.0/conf/core |
| OGC API - Features - Part 1: Core | 1.0 | GeoJSON | http://www.opengis.net/spec/ogcapi-features-1/1.0/conf/geojson | 

As the above practices are not yet in place for CEOS-ARD specification, we assume the following identifiers.  They will be updated once the final identifiers are available.

Below are a number of the current specifications.  They are meant as examples and the recommendations should apply to all current and 
future specifications.  Note that the "title" to be used in citations of the various PFS (e.g. NRB) may currently not be well defined.

| Specification Title | Version | Date | External identifier (URI) |
|------|-----|-----|-----|
| CEOS-ARD Product Family Specification: Surface Reflectance | 5.0.1 | 6/12/2023 | https://ceos.org/ard/files/PFS/SR/v5.0.1 | 
| CEOS-ARD Product Family Specification: Normalised Radar Backscatter | 5.5 | 14/10/2021 | https://ceos.org/ard/files/PFS/NRB/v5.5 | 
| CEOS-ARD Product Family Specification: Surface Temperature | 5.0 | 08/06/2020 | https://ceos.org/ard/files/PFS/ST/v5.0 | 

```{warning}
Do we want to preserve the folder names currently used as URI to identify the actual documents ? or will documents get different URI on the cover sheet as per OGC practice ?.
```

It should be noted that the above identifiers are not the actual download URL which are:

- https://ceos.org/ard/files/PFS/SR/v5.0.1/CEOS-ARD_Product_Family_Specification_Surface_Reflectance-v5.0.1.pdf
- https://ceos.org/ard/files/PFS/NRB/v5.5/CARD4L-PFS_NRB_v5.5.pdf 
- https://ceos.org/ard/files/PFS/ST/v5.0/CARD4L_Product_Family_Specification_Surface_Temperature-v5.0.pdf

The current PFS specifications do currently not define conformance classes.  These may be added at a later stage and will allow to express partial compliance.

```{warning}
URI and meaning of compliance classes have still to be defined.  Below are examples only...
```

| Specification Title | Version |  Conformance Class  | Conformance Class (URI)
|------|-----|-----|-----|
| CEOS-ARD Product Family Specification: Surface Reflectance          | 5.0   | Threshold | http://ceos.org/spec/ard/PFS/SR/5.0/conf/threshold  |
| CEOS-ARD Product Family Specification: Surface Reflectance          | 5.0   | Threshold | http://ceos.org/spec/ard/PFS/SR/5.0/conf/threshold_geometric_correction  |
| CEOS-ARD Product Family Specification: Surface Reflectance          | 5.0   | Threshold | http://ceos.org/spec/ard/PFS/SR/5.0/conf/target_geometric_correction  |
| CEOS-ARD Product Family Specification: Normalised Radar Backscatter | 5.5   | Threshold | http://ceos.org/spec/ard/PFS/NRB/5.5/conf/threshold | 


`````{admonition} CEOS-ARDMD-REC-0020 [Recommendation]
:class: tip
Metadata encoding shall use citation elements for CEOS-ARD PFS such as document titles, document identifiers (URI) and conformence class identifiers (URI) according to the conventions summarized above. 
`````

## Requirements for Keywords

The lightweight approach consists in including controlled keywords in the collection metadata to categorize the colections according to 
CEOS-ARD Product Family.  This approach is not suitable to express compliance with individual conformance classes however.

| Specification Title | Version |  Keyword  | Keyword (URI)
|------|-----|-----|-----|
| CEOS-ARD Product Family Specification: Surface Reflectance          | Any   | Surface Reflectance | `https://ceos.org/ard/metadata-codelists/PFS/SR`  |
| CEOS-ARD Product Family Specification: Surface Reflectance          | 5.0   | Surface Reflectance 5.0 | `https://ceos.org/ard/metadata-codelists/PFS/SR/5.0`  |
| CEOS-ARD Product Family Specification: Normalised Radar Backscatter | Any   | Normalised Radar Backscatter | `https://ceos.org/ard/metadata-codelists/PFS/NRB` | 
| CEOS-ARD Product Family Specification: Normalised Radar Backscatter | 5.5   | Normalised Radar Backscatter 5.5 | `https://ceos.org/ard/metadata-codelists/PFS/NRB/5.5` | 


```{warning}
Whether the keyword URI and specification URI can be identical is still to be agreed.
```

Controlled keywords are proposed that will be discoverable in the future via their online publication.
We propose the approach  used by INSPIRE (See example Codelist at https://inspire.ec.europa.eu/metadata-codelist/DegreeOfConformity).  Items have individual URI like this: https://inspire.ec.europa.eu/metadata-codelist/DegreeOfConformity/conformant.  For this INSPIRE example, values are then available in multiple formats (XML Registry, XML ISO 19135, RDF/XML, JSON etc.) at paths such as `https://inspire.ec.europa.eu/metadata-codelist/DegreeOfConformity/DegreeOfConformity.en.rdf`.

CEOS will publish and maintain a similar RDF/XML file with the available keywords and keyword URI.  The update of list of URI is expected to become part of the approval process for a new or updated PFS.

E.g. `https://ceos.org/ard/metadata-codelists/PFS/PFS.rdf` document (The exact online URL is still TBD). 

```xml
<?xml version='1.0' encoding='utf-8'?>
<rdf:RDF xmlns:dcat="http://www.w3.org/ns/dcat#"
         xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xmlns:rdfs="http://www.w3.org/2000/01/rdf-schema#"
         xmlns:owl="http://www.w3.org/2002/07/owl#"
         xmlns:skos="http://www.w3.org/2004/02/skos/core#"
         xmlns:dct="http://purl.org/dc/terms/">

	<skos:Concept rdf:about="https://ceos.org/ard/metadata-codelists/PFS">
		<skos:prefLabel xml:lang="en">Product Family Specification</skos:prefLabel>
		<rdfs:seeAlso rdf:resource="https://ceos.org/ard/index.html#specs"/>
	</skos:Concept>

	<skos:Concept rdf:about="https://ceos.org/ard/metadata-codelists/PFS/SR">
		<skos:inScheme rdf:resource="https://ceos.org/ard/concepts/concept_scheme/PFS"/>
		<skos:prefLabel xml:lang="en">Surface Reflectance</skos:prefLabel>
		<skos:notation xml:lang="en">SR</skos:notation>
		<skos:definition xml:lang="en">The Surface Reflectance Product Family Specification ...</skos:definition>
		<skos:broader rdf:resource="https://ceos.org/ard/metadata-codelists/PFS"/>
	</skos:Concept>
	
	<skos:Concept rdf:about="https://ceos.org/ard/metadata-codelists/PFS/SR/5.0">
	    <owl:deprecated rdf:datatype="http://www.w3.org/2001/XMLSchema#boolean">true</owl:deprecated>
		<skos:inScheme rdf:resource="https://ceos.org/ard/concepts/concept_scheme/PFS"/>
		<skos:prefLabel xml:lang="en">Surface Reflectance 5.0</skos:prefLabel>
		<skos:definition xml:lang="en">The Surface Reflectance Product Family Specification ...</skos:definition>
		<skos:broader rdf:resource="https://ceos.org/ard/metadata-codelists/PFS/SR"/>
		<rdfs:isDefinedBy rdf:resource="https://ceos.org/ard/files/PFS/SR/v5.0/CARD4L_Product_Family_Specification_Surface_Reflectance-v5.0.pdf"/>
		<rdfs:seeAlso rdf:resource="https://ceos.org/ard/files/PFS/SR/v5.0/CARD4L_Product_Family_Specification_Surface_Reflectance-v5.0.pdf"/>
	</skos:Concept>

	<skos:Concept rdf:about="https://ceos.org/ard/metadata-codelists/PFS/SR/5.0.1">
		<skos:inScheme rdf:resource="https://ceos.org/ard/concepts/concept_scheme/PFS"/>
		<skos:prefLabel xml:lang="en">Surface Reflectance 5.0.1</skos:prefLabel>
		<skos:definition xml:lang="en">The Surface Reflectance Product Family Specification ...</skos:definition>
		<skos:broader rdf:resource="https://ceos.org/ard/metadata-codelists/PFS/SR"/>
		<rdfs:isDefinedBy rdf:resource="https://ceos.org/ard/files/PFS/SR/v5.0.1/CEOS-ARD_Product_Family_Specification_Surface_Reflectance-v5.0.1.pdf"/>
		<rdfs:seeAlso rdf:resource="https://ceos.org/ard/files/PFS/SR/v5.0.1/CEOS-ARD_Product_Family_Specification_Surface_Reflectance-v5.0.1.pdf"/>
	</skos:Concept>

	<skos:Concept rdf:about="https://ceos.org/ard/metadata-codelists/PFS/NRB">
		<skos:inScheme rdf:resource="https://ceos.org/ard/concepts/concept_scheme/PFS"/>
		<skos:prefLabel xml:lang="en">Normalised Radar Backscatter</skos:prefLabel>
		<skos:notation xml:lang="en">NRB</skos:notation>
		<skos:definition xml:lang="en">The Normalised Radar Backscatter Family Specification ...</skos:definition>
		<skos:broader rdf:resource="https://ceos.org/ard/metadata-codelists/PFS"/>
	</skos:Concept>
	
	<skos:Concept rdf:about="https://ceos.org/ard/metadata-codelists/PFS/NRB/5.0">
	    <owl:deprecated rdf:datatype="http://www.w3.org/2001/XMLSchema#boolean">true</owl:deprecated>
		<skos:inScheme rdf:resource="https://ceos.org/ard/concepts/concept_scheme/PFS"/>
		<skos:prefLabel xml:lang="en">Normalised Radar Backscatter 5.0</skos:prefLabel>
		<skos:definition xml:lang="en">The Normalised Radar Backscatter Family Specification ...</skos:definition>
		<skos:broader rdf:resource="https://ceos.org/ard/metadata-codelists/PFS/NRB"/>
		<rdfs:isDefinedBy rdf:resource="https://ceos.org/ard/files/PFS/NRB/v5.0/CARD4L-PFS_Normalised_Radar_Backscatter-v5.0.pdf"/>
		<rdfs:seeAlso rdf:resource="https://ceos.org/ard/files/PFS/NRB/v5.0/CARD4L-PFS_Normalised_Radar_Backscatter-v5.0.pdf"/>
	</skos:Concept>
	
	<skos:Concept rdf:about="https://ceos.org/ard/metadata-codelists/PFS/NRB/5.5">
		<skos:inScheme rdf:resource="https://ceos.org/ard/concepts/concept_scheme/PFS"/>
		<skos:prefLabel xml:lang="en">Normalised Radar Backscatter 5.5</skos:prefLabel>
		<skos:definition xml:lang="en">The Normalised Radar Backscatter Family Specification ...</skos:definition>
		<skos:broader rdf:resource="https://ceos.org/ard/metadata-codelists/PFS/NRB"/>
		<rdfs:isDefinedBy rdf:resource="https://ceos.org/ard/files/PFS/NRB/v5.5/CARD4L-PFS_NRB_v5.5.pdf"/>
		<rdfs:seeAlso rdf:resource="https://ceos.org/ard/files/PFS/NRB/v5.5/CARD4L-PFS_NRB_v5.5.pdf"/>
	</skos:Concept>

</rdf:RDF>
```

