# The IBIS ([bis](https://vocab.methodandstructure.com/ibis#explanation)) Vocabulary

<div class="section" about="#" typeof="owl:Ontology">

Author  
<a href="https://doriantaylor.com/person/dorian-taylor#me"
rel="dct:creator"><span property="foaf:name">Dorian Taylor</span></a>

Version  
0.5

Created  
December 11, 2012

Updated  
December 12, 2012

February 24, 2014

February 22, 2018

March 24, 2019

December 18, 2023

Namespace URI  
[`https://vocab.methodandstructure.com/ibis#`](https://vocab.methodandstructure.com/ibis#)

Preferred Namespace Prefix  
`ibis`

This document specifies a vocabulary for describing an IBIS (issue-based
information system).

The purpose of this vocabulary is to express the necessary semantics for
the internal representation of—and interchange between—collaborative
software systems that facilitate structured argumentation and
issue-based reasoning. This vocabulary augments the semantic elements of
<a
href="http://www.cs.hut.fi/Opinnot/T-93.850/2005/Papers/gIBIS1988-conklin.pdf"
about="#" type="application/pdf" rel="rdfs:seeAlso">the gIBIS paper</a>
by reusing components from, and thus integrating it into the Semantic
Web.

This document was <a
href="https://web.archive.org/web/20120606063823/http://hyperdata.org/xmlns/ibis/"
rel="rdfs:seeAlso">inspired by work</a> from <a
href="https://web.archive.org/web/20130113103138/http://danny.ayers.name/index.rdf#me"
about="https://web.archive.org/web/20120606063823/http://hyperdata.org/xmlns/ibis/"
rel="dct:creator"><span property="foaf:name">Danny Ayers</span></a>,
which, as of around October of 2012, has unfortunately disappeared from
the web. <a href="https://doriantaylor.com/person/dorian-taylor#me"
rel="dct:creator">I</a> developed this vocabulary to replace it. It
differs from the Ayers version primarily in that it is an
<a href="http://www.w3.org/2004/02/skos/core#"
rel="owl:imports">extension of SKOS</a>, due to the suitability of the
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="dct:references">Concept</a> as a common ancestor for expressing the
fundamental IBIS types.

As with the other vocabularies on this site, this prose version is
canonical, and the
<a href="https://vocab.methodandstructure.com/ibis.rdf"
rel="rdfs:seeAlso">RDF/XML</a> and
<a href="https://vocab.methodandstructure.com/ibis.n3"
rel="rdfs:seeAlso">N3/Turtle</a> versions are derived from it.

</div>

<div class="section">

## Classes

![](https://vocab.methodandstructure.com/ibis-classes)

<div id="Entity" class="section" about="[ibis:Entity]"
typeof="owl:Class">

### `Entity`

`ibis:Entity` is the abstract superclass of from which the more specific
entities are derived.

Subclass of:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:subClassOf"><code>skos:Concept</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="Issue" class="section" about="[ibis:Issue]" typeof="owl:Class">

### `Issue`

An Issue is a state of affairs, claimed by one or more Agents to either
be a misfit itself, or affecting some other Issue or Position.

Subclass of:  
<a href="https://vocab.methodandstructure.com/ibis#Entity"
rel="rdfs:subClassOf"><code>ibis:Entity</code></a>

Property restrictions:  
<span id="generalizes-issue" typeof="owl:Restriction">
<a href="http://www.w3.org/2004/02/skos/core#narrowerTransitive"
rel="owl:onProperty"><code>skos:narrowerTransitive</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="owl:allValuesFrom"><code>ibis:Issue</code></a> </span>

<span id="specializes-issue" typeof="owl:Restriction">
<a href="http://www.w3.org/2004/02/skos/core#broaderTransitive"
rel="owl:onProperty"><code>skos:broaderTransitive</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="owl:allValuesFrom"><code>ibis:Issue</code></a> </span>

<span id="replaces-issue" typeof="owl:Restriction">
<a href="https://vocab.methodandstructure.com/ibis#replaces"
rel="owl:onProperty"><code>ibis:replaces</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="owl:allValuesFrom"><code>ibis:Issue</code></a> </span>

<span id="replaced-by-issue" typeof="owl:Restriction">
<a href="https://vocab.methodandstructure.com/ibis#replaced-by"
rel="owl:onProperty"><code>ibis:replaced-by</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="owl:allValuesFrom"><code>ibis:Issue</code></a> </span>

Disjoint with:  
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="owl:disjointWith"><code>ibis:Position</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="Position" class="section" about="[ibis:Position]"
typeof="owl:Class">

### `Position`

A Position asserts a moral, ethical, pragmatic, or similar kind of
assertion, typically identifying what, if anything, should be done about
an Issue.

Subclass of:  
<a href="https://vocab.methodandstructure.com/ibis#Entity"
rel="rdfs:subClassOf"><code>ibis:Entity</code></a>

Property restrictions:  
<span id="generalizes-position" typeof="owl:Restriction">
<a href="http://www.w3.org/2004/02/skos/core#narrowerTransitive"
rel="owl:onProperty"><code>skos:narrowerTransitive</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="owl:allValuesFrom"><code>ibis:Position</code></a> </span>

<span id="specializes-position" typeof="owl:Restriction">
<a href="http://www.w3.org/2004/02/skos/core#broaderTransitive"
rel="owl:onProperty"><code>skos:broaderTransitive</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="owl:allValuesFrom"><code>ibis:Position</code></a> </span>

<span id="replaces-position" typeof="owl:Restriction">
<a href="https://vocab.methodandstructure.com/ibis#replaces"
rel="owl:onProperty"><code>ibis:replaces</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="owl:allValuesFrom"><code>ibis:Position</code></a> </span>

<span id="replaced-by-position" typeof="owl:Restriction">
<a href="https://vocab.methodandstructure.com/ibis#replaced-by"
rel="owl:onProperty"><code>ibis:replaced-by</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="owl:allValuesFrom"><code>ibis:Position</code></a> </span>

Disjoint with:  
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="owl:disjointWith"><code>ibis:Issue</code></a>

<a href="https://vocab.methodandstructure.com/ibis#Argument"
rel="owl:disjointWith"><code>ibis:Argument</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="Argument" class="section" about="[ibis:Argument]"
typeof="owl:Class">

### `Argument`

An Argument is a type of Issue that explicitly supports or refutes a
Position.

> An Argument need not only relate in scope to another Argument, but it
> must only be replaced by another argument.

Subclass of:  
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="rdfs:subClassOf"><code>ibis:Issue</code></a>

Property restrictions:  
<span id="replaces-argument" typeof="owl:Restriction">
<a href="https://vocab.methodandstructure.com/ibis#replaces"
rel="owl:onProperty"><code>ibis:replaces</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Argument"
rel="owl:allValuesFrom"><code>ibis:Argument</code></a> </span>

<span id="replaced-by-argument" typeof="owl:Restriction">
<a href="https://vocab.methodandstructure.com/ibis#replaced-by"
rel="owl:onProperty"><code>ibis:replaced-by</code></a> ∈
<a href="https://vocab.methodandstructure.com/ibis#Argument"
rel="owl:allValuesFrom"><code>ibis:Argument</code></a> </span>

Disjoint with:  
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="owl:disjointWith"><code>ibis:Position</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="Invariant" class="section" about="[ibis:Invariant]"
typeof="owl:Class">

### `Invariant`

An `ibis:Entity` can be marked `ibis:Invariant` to denote that it has
been deemed outside of the influence of the agents in the system, i.e.,
something to be steered around.

Subclass of:  
<a href="https://vocab.methodandstructure.com/ibis#Entity"
rel="rdfs:subClassOf"><code>ibis:Entity</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="Network" class="section" about="[ibis:Network]"
typeof="owl:Class">

### `Network`

A network of issues, positions, and arguments.

Subclass of:  
<a href="http://www.w3.org/2004/02/skos/core#ConceptScheme"
rel="rdfs:subClassOf"><code>skos:ConceptScheme</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

</div>

<div class="section">

## Properties

![](https://vocab.methodandstructure.com/ibis-properties)

<div class="section">

### Agency

Since argumentation doesn't happen in a vacuum, it is important to
provide a mechanism for connecting agents (ideally people) to the
process. While the
<a href="http://dublincore.org/documents/dcmi-terms/" about="#"
rel="rdfs:seeAlso">Dublin Core</a> and
<a href="http://www.w3.org/TR/prov-o/" about="#"
rel="rdfs:seeAlso">provenance ontologies</a> are available for
expressing authorship, there exist other agent-related considerations.

These terms are extensions to the original IBIS model.

<div id="endorses" class="section" about="[ibis:endorses]"
typeof="owl:ObjectProperty">

#### `endorses`

An Agent can endorse a concept without having initially mentioned or
advanced it, and without any additional comment.

This term, along with ibis:endorsed-by, enables an Agent to signal its
agreement with a concept. To signal disagreement, explain why with an
ibis:Argument that ibis:opposes the concept.

Domain:  
<a href="http://xmlns.com/foaf/0.1/Agent"
rel="rdfs:domain"><code>foaf:Agent</code></a>

Range:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:range"><code>skos:Concept</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#endorsed-by"
rel="owl:inverseOf"><code>ibis:endorsed-by</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="endorsed-by" class="section" about="[ibis:endorsed-by]"
typeof="owl:ObjectProperty">

#### `endorsed by`

A concept can be endorsed by an Agent without said Agent having
mentioned or advanced it initially, and without any additional comment.

This term, along with ibis:endorses, enables an Agent to signal its
agreement with a concept. To signal disagreement, explain why with an
ibis:Argument that ibis:opposes the concept.

Domain:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:domain"><code>skos:Concept</code></a>

Range:  
<a href="http://xmlns.com/foaf/0.1/Agent"
rel="rdfs:range"><code>foaf:Agent</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#endorses"
rel="owl:inverseOf"><code>ibis:endorses</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

</div>

<div class="section">

### Relations to Concepts

This IBIS vocabulary is based on SKOS, and therefore has a close
relationship with it. These properties connect IBIS to with skos

<div id="concepts" class="section" about="[ibis:concepts]"
typeof="owl:ObjectProperty">

#### `concepts`

This relates a concept scheme to the IBIS network.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Network"
rel="rdfs:domain"><code>ibis:Network</code></a>

Range:  
<a href="http://www.w3.org/2004/02/skos/core#ConceptScheme"
rel="rdfs:range"><code>skos:ConceptScheme</code></a>

Sub-property of:  
<a href="http://purl.org/dc/terms/requires"
rel="rdfs:subPropertyOf"><code>dct:requires</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="main-concepts" class="section" about="[ibis:main-concepts]"
typeof="owl:ObjectProperty owl:FunctionalProperty">

#### `main-concepts`

This relates the *preferred* concept scheme to the IBIS network.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Network"
rel="rdfs:domain"><code>ibis:Network</code></a>

Range:  
<a href="http://www.w3.org/2004/02/skos/core#ConceptScheme"
rel="rdfs:range"><code>skos:ConceptScheme</code></a>

Sub-property of:  
<a href="https://vocab.methodandstructure.com/ibis#concepts"
rel="rdfs:subPropertyOf"><code>ibis:concepts</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="concerns" class="section" about="[ibis:concerns]"
typeof="owl:ObjectProperty">

#### `concerns`

The subject is an issue concerning the object, which can be any
resource.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Entity"
rel="rdfs:domain"><code>ibis:Entity</code></a>

Range:  
<a href="http://www.w3.org/2002/07/owl#Thing"
rel="rdfs:range"><code>owl:Thing</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#concern-of"
rel="owl:inverseOf"><code>ibis:concern-of</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="concern-of" class="section" about="[ibis:concern-of]"
typeof="owl:ObjectProperty">

#### `concern-of`

The subject is an issue concerning the object, which can be any
resource.

Domain:  
<a href="http://www.w3.org/2002/07/owl#Thing"
rel="rdfs:domain"><code>owl:Thing</code></a>

Range:  
<a href="https://vocab.methodandstructure.com/ibis#Entity"
rel="rdfs:range"><code>ibis:Entity</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#concerns"
rel="owl:inverseOf"><code>ibis:concerns</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

</div>

<div class="section">

### Subordination and Superordination

While all IBIS terms inherit the semantic relations from SKOS, the IBIS
paper specifies mereological relations peculiar to Issues. I have
relaxed the constraint specified in the paper, such that these relations
are now merely vestigial.

<div id="specializes" class="section" about="[ibis:specializes]"
typeof="owl:ObjectProperty">

#### `specializes`

The subject is a more specific form of the object.

The equivalent property skos:broader asserts that the object is broader
than the subject, while the subject of ibis:specializes is more specific
than the object.

Equivalent property:  
<a href="http://www.w3.org/2004/02/skos/core#broader"
rel="owl:equivalentProperty"><code>skos:broader</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#generalizes"
rel="owl:inverseOf"><code>ibis:generalizes</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="generalizes" class="section" about="[ibis:generalizes]"
typeof="owl:ObjectProperty">

#### `generalizes`

The subject is a more generic form of the object.

The equivalent property skos:narrower asserts that the object is
narrower than the subject, while the subject of ibis:generalizes is more
general than the object.

Equivalent property:  
<a href="http://www.w3.org/2004/02/skos/core#narrower"
rel="owl:equivalentProperty"><code>skos:narrower</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#specializes"
rel="owl:inverseOf"><code>ibis:specializes</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

</div>

<div class="section">

### Replacement

<div id="replaces" class="section" about="[ibis:replaces]"
typeof="owl:ObjectProperty">

#### `replaces`

Indicates when a concept replaces another concept of the same type.

Domain:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:domain"><code>skos:Concept</code></a>

Range:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:range"><code>skos:Concept</code></a>

Sub-property of:  
<a href="http://purl.org/dc/terms/replaces"
rel="rdfs:subPropertyOf"><code>dct:replaces</code></a>

<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#replaced-by"
rel="owl:inverseOf"><code>ibis:replaced-by</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="replaced-by" class="section" about="[ibis:replaced-by]"
typeof="owl:ObjectProperty">

#### `replaced-by`

Indicates when a concept is replaced by another concept of the same
type.

Domain:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:domain"><code>skos:Concept</code></a>

Range:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:range"><code>skos:Concept</code></a>

Sub-property of:  
<a href="http://purl.org/dc/terms/isReplacedBy"
rel="rdfs:subPropertyOf"><code>dct:isReplacedBy</code></a>

<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#replaces"
rel="owl:inverseOf"><code>ibis:replaces</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

</div>

<div class="section">

### Suggestions

<div id="suggests" class="section" about="[ibis:suggests]"
typeof="owl:ObjectProperty">

#### `suggests`

Indicates when the subject belief suggests the object issue.

Domain:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:domain"><code>skos:Concept</code></a>

Range:  
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="rdfs:range"><code>ibis:Issue</code></a>

Sub-property of:  
<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#suggested-by"
rel="owl:inverseOf"><code>ibis:suggested-by</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="suggested-by" class="section" about="[ibis:suggested-by]"
typeof="owl:ObjectProperty">

#### `suggested-by`

Indicates when the subject issue is suggested by the object belief.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="rdfs:domain"><code>ibis:Issue</code></a>

Range:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:range"><code>skos:Concept</code></a>

Sub-property of:  
<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#suggests"
rel="owl:inverseOf"><code>ibis:suggests</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

</div>

<div class="section">

### Questions

<div id="questions" class="section" about="[ibis:questions]"
typeof="owl:ObjectProperty">

#### `questions`

Indicates an issue that raises doubt on a belief.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="rdfs:domain"><code>ibis:Issue</code></a>

Range:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:range"><code>skos:Concept</code></a>

Sub-property of:  
<a href="https://vocab.methodandstructure.com/ibis#suggested-by"
rel="rdfs:subPropertyOf"><code>ibis:suggested-by</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#questioned-by"
rel="owl:inverseOf"><code>ibis:questioned-by</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="questioned-by" class="section" about="[ibis:questioned-by]"
typeof="owl:ObjectProperty">

#### `questioned-by`

Indicates a belief called into question by an issue.

Domain:  
<a href="http://www.w3.org/2004/02/skos/core#Concept"
rel="rdfs:domain"><code>skos:Concept</code></a>

Range:  
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="rdfs:range"><code>ibis:Issue</code></a>

Sub-property of:  
<a href="https://vocab.methodandstructure.com/ibis#suggests"
rel="rdfs:subPropertyOf"><code>ibis:suggests</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#questions"
rel="owl:inverseOf"><code>ibis:questions</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

</div>

<div class="section">

### Response

<div id="response" class="section" about="[ibis:response]"
typeof="owl:ObjectProperty">

#### `response`

Indicates a position that responds to the subject issue.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="rdfs:domain"><code>ibis:Issue</code></a>

Range:  
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="rdfs:range"><code>ibis:Position</code></a>

Sub-property of:  
<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#responds-to"
rel="owl:inverseOf"><code>ibis:responds-to</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="responds-to" class="section" about="[ibis:responds-to]"
typeof="owl:ObjectProperty">

#### `responds-to`

Indicates an issue to which the subject position responds.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="rdfs:domain"><code>ibis:Position</code></a>

Range:  
<a href="https://vocab.methodandstructure.com/ibis#Issue"
rel="rdfs:range"><code>ibis:Issue</code></a>

Sub-property of:  
<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#response"
rel="owl:inverseOf"><code>ibis:response</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

</div>

<div class="section">

### Argumentation

<div id="supports" class="section" about="[ibis:supports]"
typeof="owl:ObjectProperty">

#### `supports`

Indicates a subject argument that supports an object position.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Argument"
rel="rdfs:domain"><code>ibis:Argument</code></a>

Range:  
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="rdfs:range"><code>ibis:Position</code></a>

Sub-property of:  
<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#supported-by"
rel="owl:inverseOf"><code>ibis:supported-by</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="supported-by" class="section" about="[ibis:supported-by]"
typeof="owl:ObjectProperty">

#### `supported-by`

Indicates a subject position supported by an object argument.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="rdfs:domain"><code>ibis:Position</code></a>

Range:  
<a href="https://vocab.methodandstructure.com/ibis#Argument"
rel="rdfs:range"><code>ibis:Argument</code></a>

Sub-property of:  
<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#supports"
rel="owl:inverseOf"><code>ibis:supports</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="opposes" class="section" about="[ibis:opposes]"
typeof="owl:ObjectProperty">

#### `opposes`

Indicates a subject argument that opposes an object position.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Argument"
rel="rdfs:domain"><code>ibis:Argument</code></a>

Range:  
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="rdfs:range"><code>ibis:Position</code></a>

Sub-property of:  
<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#opposed-by"
rel="owl:inverseOf"><code>ibis:opposed-by</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

<div id="opposed-by" class="section" about="[ibis:opposed-by]"
typeof="owl:ObjectProperty">

#### `opposed-by`

Indicates a subject position opposed by an object argument.

Domain:  
<a href="https://vocab.methodandstructure.com/ibis#Position"
rel="rdfs:domain"><code>ibis:Position</code></a>

Range:  
<a href="https://vocab.methodandstructure.com/ibis#Argument"
rel="rdfs:range"><code>ibis:Argument</code></a>

Sub-property of:  
<a href="http://www.w3.org/2004/02/skos/core#semanticRelation"
rel="rdfs:subPropertyOf"><code>skos:semanticRelation</code></a>

Inverse of:  
<a href="https://vocab.methodandstructure.com/ibis#opposes"
rel="owl:inverseOf"><code>ibis:opposes</code></a>

<a href="https://vocab.methodandstructure.com/ibis#"
rel="rdfs:isDefinedBy">Back to Top</a>

</div>

</div>

</div>

<div class="section">

## Revisions

The initial version of this vocabulary was adapted directly from the
gIBIS paper and [implemented as a Web
application](https://github.com/doriantaylor/p5-app-ibis). It was
immediately evident through use that it made little sense that an
[Argument](https://vocab.methodandstructure.com/ibis#Argument) was
something disjoint from an
[Issue](https://vocab.methodandstructure.com/ibis#Issue), both from a
semantic perspective, and from the perspective of implementing the user
interface. It made more sense, therefore, to make
[Argument](https://vocab.methodandstructure.com/ibis#Argument) a
subclass of [Issue](https://vocab.methodandstructure.com/ibis#Issue).

It also made sense to provide a mechanism to indicate the negotiability
of an [Issue](https://vocab.methodandstructure.com/ibis#Issue) or a
[Position](https://vocab.methodandstructure.com/ibis#Position). For
instance, we can imagine an
[Issue](https://vocab.methodandstructure.com/ibis#Issue) (or
[Argument](https://vocab.methodandstructure.com/ibis#Argument)) like
“The QWERTY keyboard is a ubiquitously familiar interface.” Consider
also a [Position](https://vocab.methodandstructure.com/ibis#Position)
expressing a standing policy prescription, like “Never appease a
tyrant.” In both these cases, it is useful to mark them as
[Invariant](https://vocab.methodandstructure.com/ibis#Invariant), which
we do by decorating them with the
[Invariant](https://vocab.methodandstructure.com/ibis#Invariant) class.

I initially created the
[generalizes](https://vocab.methodandstructure.com/ibis#generalizes),
[specializes](https://vocab.methodandstructure.com/ibis#specializes),
[replaces](https://vocab.methodandstructure.com/ibis#replaces), and
[replaced-by](https://vocab.methodandstructure.com/ibis#replaced-by)
predicates to correspond to the paper, but again, through use, it became
evident that the constraint that only an
[Issue](https://vocab.methodandstructure.com/ibis#Issue) could make use
of them made little sense.

Without this constraint, the
[generalizes](https://vocab.methodandstructure.com/ibis#generalizes)/[specializes](https://vocab.methodandstructure.com/ibis#specializes)
pair are redundant versus their super-properties,
[skos:narrower](http://www.w3.org/2004/02/skos/core#narrower) and
[skos:broader](http://www.w3.org/2004/02/skos/core#broader). I'm keeping
them around, though, as equivalent properties, because of the lexical
ambiguity in the SKOS terms. I also added same-class constraints, but
against
[skos:broaderTransitive](http://www.w3.org/2004/02/skos/core#broaderTransitive)
and
[skos:narrowerTransitive](http://www.w3.org/2004/02/skos/core#narrowerTransitive)
to reintroduce the potential for transitivity.

I decided to retain
[replaces](https://vocab.methodandstructure.com/ibis#replaces) and
[replaced-by](https://vocab.methodandstructure.com/ibis#replaced-by) as
sub-properties of their Dublin Core counterparts, though only to
reinforce them as object properties over the domain and range of
[skos:Concept](http://www.w3.org/2004/02/skos/core#Concept).

After enough time in the saddle, I am fairly convinced that
[questions](https://vocab.methodandstructure.com/ibis#questions) and
[suggests](https://vocab.methodandstructure.com/ibis#suggests) are
roughly inversely related, with <span class="dfn">questions</span> being
a stronger form of
[suggested-by](https://vocab.methodandstructure.com/ibis#suggested-by),
and have such made the former a subproperty of the latter.

<div class="section">

### Future Directions

Other IBIS implementations have an explicit concept of a *Question*,
which I considered but ultimately left out. There is already a
discontinuity between the grammatical form of a question and its purpose
in ordinary dialogue—i.e., are we actually asking for information or is
the question merely rhetorical. We don't need to confuse things further
by cementing that discontinuity into formal language.

There is also the natural tendency that once we have agreed on a
particular
[Position](https://vocab.methodandstructure.com/ibis#Position), that we
commit it to action. It is therefore tempting to extend the IBIS
vocabulary into some sort of project planning apparatus. I have chosen
instead to leave this vocabulary alone if possible, and extend it
through
<a href="https://vocab.methodandstructure.com/process-model#" about="#"
rel="rdfs:seeAlso">a process model ontology</a>.

</div>

</div>

<div class="section">

## References

-   <a href="http://www.cc.gatech.edu/~ellendo/rittel/rittel-issues.pdf"
    rel="rdfs:seeAlso" type="application/pdf"><span
    property="dct:title">Issues as Elements of Information Systems</span>
    (<span property="dct:creator" content="Werner Kunz">Kunz</span> and
    <span property="dct:creator" content="Horst Rittel">Rittel</span>, <span
    property="dct:date">1970</span>)</a>
-   <a
    href="http://www.cs.hut.fi/Opinnot/T-93.850/2005/Papers/gIBIS1988-conklin.pdf"
    type="application/pdf" rel="rdfs:seeAlso"><span
    property="dct:title">gIBIS: a hypertext tool for exploratory policy
    discussion</span> (<span property="dct:creator"
    content="Jeff Conklin">Conklin</span> and <span property="dct:creator"
    content="Michael L. Begeman">Begeman</span>, <span
    property="dct:date">1988</span>)</a>
-   <a href="http://en.wikipedia.org/wiki/Issue-Based_Information_System"
    rel="rdfs:seeAlso">Wikipedia entry for IBIS</a>

</div>
