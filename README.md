# The IBIS ([bis](https://vocab.methodandstructure.com/ibis#explanation)) Vocabulary

<div class="section" about="#" typeof="owl:Ontology">

  - Author  
    [<span property="foaf:name">Dorian
    Taylor</span>](https://doriantaylor.com/person/dorian-taylor#me)
  - Version  
    0.4
  - Created  
    December 11, 2012
  - Updated  
    December 12, 2012
    February 24, 2014
    February 22, 2018
    March 24, 2019
  - Namespace URI  
    <https://vocab.methodandstructure.com/ibis#>
  - Preferred Namespace Prefix  
    ibis

This document specifies a vocabulary for describing an IBIS (issue-based
information system).

The purpose of this vocabulary is to express the necessary semantics for
the internal representation of—and interchange between—collaborative
software systems that facilitate structured argumentation and
issue-based reasoning. This vocabulary augments the semantic elements of
[the gIBIS
paper](http://www.cs.hut.fi/Opinnot/T-93.850/2005/Papers/gIBIS1988-conklin.pdf)
by reusing components from, and thus integrating it into the Semantic
Web.

![](https://vocab.methodandstructure.com/ibis-classes)

This document was [inspired by work](http://hyperdata.org/xmlns/ibis/)
from [<span property="foaf:name">Danny
Ayers</span>](http://danny.ayers.name/index.rdf#me), which, as of around
October of 2012, has unfortunately disappeared from the web.
[I](http://doriantaylor.com/person/dorian-taylor#me) developed this
vocabulary to supplant the original after several attempts to reach Mr.
Ayers. It differs from the Ayers version primarily in that it is an
[extension of SKOS](http://www.w3.org/2004/02/skos/core#), due to the
suitability of the
[Concept](http://www.w3.org/2004/02/skos/core#Concept) as a common
ancestor for expressing the fundamental IBIS types.

As with the other vocabularies on this site, this prose version is
canonical, and the [RDF/XML](https://vocab.methodandstructure.com/1.rdf)
and [N3/Turtle](https://vocab.methodandstructure.com/1.n3) versions are
derived from it.

</div>

<div class="section">

## Classes

<div id="Issue" class="section" about="[ibis:Issue]" typeof="owl:Class">

### Issue

An Issue is a state of affairs, claimed by one or more Agents to either
be a misfit itself, or affecting some other Issue or Position.

  - Subclass of:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Property restrictions:  
    <span id="generalizes-issue" typeof="owl:Restriction">
    [skos:narrowerTransitive](http://www.w3.org/2004/02/skos/core#narrowerTransitive)
    ∈ [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
    </span>
    <span id="specializes-issue" typeof="owl:Restriction">
    [skos:broaderTransitive](http://www.w3.org/2004/02/skos/core#broaderTransitive)
    ∈ [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
    </span>
    <span id="replaces-issue" typeof="owl:Restriction">
    [ibis:replaces](https://vocab.methodandstructure.com/ibis#replaces)
    ∈ [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
    </span>
    <span id="replaced-by-issue" typeof="owl:Restriction">
    [ibis:replaced-by](https://vocab.methodandstructure.com/ibis#replaced-by)
    ∈ [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
    </span>
  - Disjoint with:  
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="Position" class="section" about="[ibis:Position]" typeof="owl:Class">

### Position

A Position asserts a moral, ethical, pragmatic, or similar kind of
assertion, typically identifying what, if anything, should be done about
an Issue.

  - Subclass of:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Property restrictions:  
    <span id="generalizes-position" typeof="owl:Restriction">
    [skos:narrowerTransitive](http://www.w3.org/2004/02/skos/core#narrowerTransitive)
    ∈
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
    </span>
    <span id="specializes-position" typeof="owl:Restriction">
    [skos:broaderTransitive](http://www.w3.org/2004/02/skos/core#broaderTransitive)
    ∈
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
    </span>
    <span id="replaces-position" typeof="owl:Restriction">
    [ibis:replaces](https://vocab.methodandstructure.com/ibis#replaces)
    ∈
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
    </span>
    <span id="replaced-by-position" typeof="owl:Restriction">
    [ibis:replaced-by](https://vocab.methodandstructure.com/ibis#replaced-by)
    ∈
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
    </span>
  - Disjoint with:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
    [ibis:Argument](https://vocab.methodandstructure.com/ibis#Argument)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="Argument" class="section" about="[ibis:Argument]" typeof="owl:Class">

### Argument

An Argument is a type of Issue that explicitly supports or refutes a
Position.

> An Argument need not only relate in scope to another Argument, but it
> must only be replaced by another argument.

  - Subclass of:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
  - Property restrictions:  
    <span id="replaces-argument" typeof="owl:Restriction">
    [ibis:replaces](https://vocab.methodandstructure.com/ibis#replaces)
    ∈
    [ibis:Argument](https://vocab.methodandstructure.com/ibis#Argument)
    </span>
    <span id="replaced-by-argument" typeof="owl:Restriction">
    [ibis:replaced-by](https://vocab.methodandstructure.com/ibis#replaced-by)
    ∈
    [ibis:Argument](https://vocab.methodandstructure.com/ibis#Argument)
    </span>
  - Disjoint with:  
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="Invariant" class="section" about="[ibis:Invariant]" typeof="owl:Class">

### Invariant

An Issue or Position can be marked Invariant to denote that it has been
deemed outside of the influence of the Agents in the system, i.e.,
something to be steered around.

  - Subclass of:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="Network" class="section" about="[ibis:Network]" typeof="owl:Class">

### Network

A network of issues, positions, and arguments.

  - Subclass of:  
    [skos:ConceptScheme](http://www.w3.org/2004/02/skos/core#ConceptScheme)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

</div>

<div class="section">

## Properties

<div class="section">

### Agency

Since argumentation doesn't happen in a vacuum, it is important to
provide a mechanism for connecting agents (ideally people) to the
process. While the [Dublin
Core](http://dublincore.org/documents/dcmi-terms/) and [provenance
ontologies](http://www.w3.org/TR/prov-o/) are available for expressing
authorship, there exist other agent-related considerations.

These terms are extensions to the original IBIS model.

<div id="endorses" class="section" about="[ibis:endorses]" typeof="owl:ObjectProperty">

#### endorses

An Agent can endorse a concept without having initially mentioned or
advanced it, and without any additional comment.

> This term, along with ibis:endorsed-by, enables an Agent to signal its
> agreement with a concept. To signal disagreement, explain why with an
> ibis:Argument that ibis:opposes the concept.

  - Domain:  
    [foaf:Agent](http://xmlns.com/foaf/0.1/Agent)
  - Range:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Inverse of:  
    [ibis:endorsed-by](https://vocab.methodandstructure.com/ibis#endorsed-by)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="endorsed-by" class="section" about="[ibis:endorsed-by]" typeof="owl:ObjectProperty">

#### endorsed by

A concept can be endorsed by an Agent without said Agent having
mentioned or advanced it initially, and without any additional comment.

> This term, along with ibis:endorses, enables an Agent to signal its
> agreement with a concept. To signal disagreement, explain why with an
> ibis:Argument that ibis:opposes the concept.

  - Domain:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Range:  
    [foaf:Agent](http://xmlns.com/foaf/0.1/Agent)
  - Inverse of:  
    [ibis:endorses](https://vocab.methodandstructure.com/ibis#endorses)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="concerns" class="section" about="[ibis:concerns]" typeof="owl:ObjectProperty">

#### concerns

The subject is an issue concerning the object, which can be any
resource.

  - Domain:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
  - Range:  
    [owl:Thing](http://www.w3.org/2002/07/owl#Thing)
  - Inverse of:  
    [ibis:concern-of](https://vocab.methodandstructure.com/ibis#concern-of)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="concern-of" class="section" about="[ibis:concern-of]" typeof="owl:ObjectProperty">

#### concern-of

The subject is an issue concerning the object, which can be any
resource.

  - Domain:  
    [owl:Thing](http://www.w3.org/2002/07/owl#Thing)
  - Range:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
  - Inverse of:  
    [ibis:concerns](https://vocab.methodandstructure.com/ibis#concerns)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

</div>

<div class="section">

### Subordination and Superordination

While all IBIS terms inherit the semantic relations from SKOS, the IBIS
paper specifies mereological relations peculiar to Issues. I have
relaxed the constraint specified in the paper, such that these relations
are now merely vestigial.

<div id="specializes" class="section" about="[ibis:specializes]" typeof="owl:ObjectProperty">

#### specializes

The subject is a more specific form of the object.

> The equivalent property skos:broader asserts that the object is
> broader than the subject, while the subject of ibis:specializes is
> more specific than the object.

  - Equivalent property:  
    [skos:broader](http://www.w3.org/2004/02/skos/core#broader)
  - Inverse of:  
    [ibis:generalizes](https://vocab.methodandstructure.com/ibis#generalizes)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="generalizes" class="section" about="[ibis:generalizes]" typeof="owl:ObjectProperty">

#### generalizes

The subject is a more generic form of the object.

> The equivalent property skos:narrower asserts that the object is
> narrower than the subject, while the subject of ibis:generalizes is
> more general than the object.

  - Equivalent property:  
    [skos:narrower](http://www.w3.org/2004/02/skos/core#narrower)
  - Inverse of:  
    [ibis:specializes](https://vocab.methodandstructure.com/ibis#specializes)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

</div>

<div class="section">

### Replacement

<div id="replaces" class="section" about="[ibis:replaces]" typeof="owl:ObjectProperty">

#### replaces

Indicates when a concept replaces another concept of the same type.

  - Domain:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Range:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Sub-property of:  
    [dct:replaces](http://purl.org/dc/terms/replaces)
  - Inverse of:  
    [ibis:replaced-by](https://vocab.methodandstructure.com/ibis#replaced-by)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="replaced-by" class="section" about="[ibis:replaced-by]" typeof="owl:ObjectProperty">

#### replaced by

Indicates when a concept is replaced by another concept of the same
type.

  - Domain:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Range:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Sub-property of:  
    [dct:isReplacedBy](http://purl.org/dc/terms/isReplacedBy)
  - Inverse of:  
    [ibis:replaces](https://vocab.methodandstructure.com/ibis#replaces)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

</div>

<div class="section">

### Suggestions

<div id="suggests" class="section" about="[ibis:suggests]" typeof="owl:ObjectProperty">

#### suggests

Indicates when the subject belief suggests the object issue.

  - Domain:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Range:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
  - Inverse of:  
    [ibis:suggested-by](https://vocab.methodandstructure.com/ibis#suggested-by)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="suggested-by" class="section" about="[ibis:suggested-by]" typeof="owl:ObjectProperty">

#### suggested by

Indicates when the subject issue is suggested by the object belief.

  - Domain:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
  - Range:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Inverse of:  
    [ibis:suggests](https://vocab.methodandstructure.com/ibis#suggests)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

</div>

<div class="section">

### Questions

<div id="questions" class="section" about="[ibis:questions]" typeof="owl:ObjectProperty">

#### questions

Indicates an issue that raises doubt on a belief.

  - Domain:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
  - Range:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Sub-property of:  
    [ibis:suggested-by](https://vocab.methodandstructure.com/ibis#suggested-by)
  - Inverse of:  
    [ibis:questioned-by](https://vocab.methodandstructure.com/ibis#questioned-by)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="questioned-by" class="section" about="[ibis:questioned-by]" typeof="owl:ObjectProperty">

#### questioned by

Indicates a belief called into question by an issue.

  - Domain:  
    [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)
  - Range:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
  - Sub-property of:  
    [ibis:suggests](https://vocab.methodandstructure.com/ibis#suggests)
  - Inverse of:  
    [ibis:questions](https://vocab.methodandstructure.com/ibis#questions)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

</div>

<div class="section">

### Response

<div id="response" class="section" about="[ibis:response]" typeof="owl:ObjectProperty">

#### response

Indicates a position that responds to the subject issue.

  - Domain:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
  - Range:  
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
  - Inverse of:  
    [ibis:responds-to](https://vocab.methodandstructure.com/ibis#responds-to)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="responds-to" class="section" about="[ibis:responds-to]" typeof="owl:ObjectProperty">

#### responds to

Indicates an issue to which the subject position responds.

  - Domain:  
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
  - Range:  
    [ibis:Issue](https://vocab.methodandstructure.com/ibis#Issue)
  - Inverse of:  
    [ibis:response](https://vocab.methodandstructure.com/ibis#response)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

</div>

<div class="section">

### Argumentation

<div id="supports" class="section" about="[ibis:supports]" typeof="owl:ObjectProperty">

#### supports

Indicates a subject argument that supports an object position.

  - Domain:  
    [ibis:Argument](https://vocab.methodandstructure.com/ibis#Argument)
  - Range:  
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
  - Inverse of:  
    [ibis:supported-by](https://vocab.methodandstructure.com/ibis#supported-by)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="supported-by" class="section" about="[ibis:supported-by]" typeof="owl:ObjectProperty">

#### supported by

Indicates a subject position supported by an object argument.

  - Domain:  
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
  - Range:  
    [ibis:Argument](https://vocab.methodandstructure.com/ibis#Argument)
  - Inverse of:  
    [ibis:supports](https://vocab.methodandstructure.com/ibis#supports)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="opposes" class="section" about="[ibis:opposes]" typeof="owl:ObjectProperty">

#### opposes

Indicates a subject argument that opposes an object position.

  - Domain:  
    [ibis:Argument](https://vocab.methodandstructure.com/ibis#Argument)
  - Range:  
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
  - Inverse of:  
    [ibis:opposed-by](https://vocab.methodandstructure.com/ibis#opposed-by)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

</div>

<div id="opposed-by" class="section" about="[ibis:opposed-by]" typeof="owl:ObjectProperty">

#### opposed by

Indicates a subject position opposed by an object argument.

  - Domain:  
    [ibis:Position](https://vocab.methodandstructure.com/ibis#Position)
  - Range:  
    [ibis:Argument](https://vocab.methodandstructure.com/ibis#Argument)
  - Inverse of:  
    [ibis:opposes](https://vocab.methodandstructure.com/ibis#opposes)

[Back to Top](https://vocab.methodandstructure.com/ibis#)

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
through [a process model
ontology](https://vocab.methodandstructure.com/ontology/process-model/1#).

</div>

</div>

<div class="section">

## References

  - [<span property="dct:title">Issues as Elements of Information
    Systems</span>
    (<span property="dct:creator" content="Werner Kunz">Kunz</span> and
    <span property="dct:creator" content="Horst Rittel">Rittel</span>,
    <span property="dct:date">1970</span>)](http://www.cc.gatech.edu/~ellendo/rittel/rittel-issues.pdf)
  - [<span property="dct:title">gIBIS: a hypertext tool for exploratory
    policy discussion</span>
    (<span property="dct:creator" content="Jeff Conklin">Conklin</span>
    and
    <span property="dct:creator" content="Michael L. Begeman">Begeman</span>,
    <span property="dct:date">1988</span>)](http://www.cs.hut.fi/Opinnot/T-93.850/2005/Papers/gIBIS1988-conklin.pdf)
  - [Wikipedia entry for
    IBIS](http://en.wikipedia.org/wiki/Issue-Based_Information_System)

</div>
