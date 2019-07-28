# Domain Specific Languages built from Software Product Lines: An Empirical Study on Visual and Textual Approaches

Authors: <a href="mailto:annabarbosah@hotmail.com">Anna Barbosa</a>, Eduardo Santana de Almeida

This webpage presents the complementary material of the paper *Domain Specific Languages built from Software Product Lines: An Empirical Study on Visual and Textual Approaches*

### Abstract Generic and specific solutions can be applied to all branches of science and engineering. While a generic approach provides a general solution for many problems in a certain area, although this solution may be suboptimal, a specific approach provides a much better solution for a smaller set of problems. DSLs, specific solutions, are means of simplify the software development process. DSLs can be classified as internal, written in a host language, or external, separate languages which bring their own syntax. An external DSL needs a language, compiler or interpreter, and an editor to support the new language. It also can be displayed in a visual and/or textual notation. Although the correct selection of notations need to be done in order to maximize those advantages, the software engineering field has a lack of a body of empirical evidence that supports such selection. This study aims to evaluate the effects of DSL on software development using software product lines. This study proposes to implement a textual and a visual DSL for the Conference Management and the Smart Home Domains, using legacy product lines and integrating the DSL development with Software Product Line Engineering. We conducted two studies. An exploratory study with the system’s original developers to validate our DSL and characterizing barriers and benefits to software development using DSL and an empirical study to compare the textual and the visual DSL regarding readability, effectiveness, efficiency, and ease of use. Visual notation had better performance when reporting bugs, while the textual notation is faster when changing DSL programs. Regarding the participants’ sense of success in completing the activities, the report of bugs using the textual notation had a better outcome than they expected. 

Keywords: Domain Specific Language, Workbench, Empirical evaluation, Software Product Line, Dynamic Software Product Line

# Exploratory Study Questions

**Preliminary Questions before the development process:**

  - Do you see the communication among the business experts and the
    developer team as a problem during software development?

  - Is it normal that misunderstandings among the business experts and
    the developer team delay software development?

  - If the previous answers were true, did you think that those
    misunderstandings can be mitigated by some software tool or
    technique?

  - What do you know about Domain Specific Languages (DSLs)? Did you
    have used an
    <span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>
    before? If not, is there a reason for this? Do you know that
    <span data-acronym-label="SQL" data-acronym-form="singular+short">SQL</span>
    is an
    <span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>?

**Questions after the development:**

  - Do you think these
    <span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>s
    represent your application domain? Why?

  - From your point of view, would the development process be improved
    by the
    <span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>?

  - Do you think the use of
    <span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>
    can enhance communication with business experts?

  - What are the positive and negative aspects of using
    <span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>s?

  - Is the *product derivation approach* using
    <span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>
    more efficient than the one you used before?

  - Would you use
    <span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>
    in a future project?

  - Do you suggest any improvement in the
    <span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>?

# Change Requests and Expected Actions

## Conference Management Domain

Change requests for visual and textual DSLs for the **Conference
Management** Domain.

### Experiment and Exploratory Study Requests

**EvCR1**. The client needs to invite researchers as "Convidado".
Including a new type, "Convidado", in **User** definition.  
The question below was performed on the **exploratory study** and
substituted for the **EvCR4** on the **experiment study**. **EvCR2**.
The system is not accepting "Debit" **Payment** anymore, only "Credit"
or "AVista". Remove this Payment type.  
**EvCR**(2/3). This product was sold to another company, "EvCo", change
the program name.  
**EvCR**(3/4). The Conference will be organized for an external company,
and the system do not need the **Organizer** type of User. Remove it.  
The question below was introduced on the **experiment study** in the
place of **EvCR2**

**EvCR4**. The System will manage the Payments, include the **Payment**
Option. Define Insert, Remove, ListAll, Update and Management as
Commands. The **Payment** Option should have two categories: "Credito"
and "AVista". Each Category has to call "askCardInfo" and
"generateBoleto" Functions respectively. None of these has a
associated screen.

### Developer Requests

**EvDCR1**. The client called requesting that the new type "Convidado"
need to generate a voucher at the end; no boleto, credit or debit is to
be sent. You need to create a new function "generateVoucher", that sends
a voucher, and associate it with the "Convidado" **User** type, created
in **EvCR1**.  
**EvDCR2**. Include property as optional on grammar, separated by a "+",
such as "+" property=ID and adjust the User Entity template to accept
the new properties as get/set.  
**EvDCR3**. Change validation to not allow "askCardInfo" as function of
Payment.

## Smart Home Domain

Changing requests for visual and textual DSLs for the **Smart Home**
Domain.

### Experiment and Exploratory Study Requests

**SHomeCR1**. The smart home will be sold to a store and they need the
"Lock Doors" feature to be *Mandatory*.  
**SHomeCR2**. The company wants a cheaper system. Create a product
without any automatic feature, only user control should be permitted.
Thus, sensors should not be created. OBS: Automatic features are
features activated and deactivated by a sensor, independent of the user
control.  
**SHomeCR3**. "AlarmsAgainstRobbery" feature, when activated, has to
call the police instead of ring the alarms. You need to instantiate a
new actuator "Phone" with type *INFO* and update the feature in the
DSL.  
**SHomeCR4**. The company wants to increment the Smart Home, you have to
create a new *Optional* feature "AlarmAgainstFire".

#Error summary of Domain Specific Languages

The application domain is characterized by the relevant elements
(concepts) and their relationships. . More generally, a
<span data-acronym-label="DSL" data-acronym-form="singular+short">DSL</span>
is composed by elements. An element can be related to others elements
and have properties.

## Taxonomy of the errors in the Domain Specific Languages

1.  <span>Elements with the same name</span> a) Same Property on the
    same Element b) Duplicated Elements

2.  <span>Relationship Errors</span> a) Relations with wrong types of
    Elements, Wrong Element or Relation Type b) Duplicated Relationships

3.  <span>Inheritance Errors</span> a) Cycles in the inheritance
    Relationships b) Properties with the same name in the child and
    father elements.

4.  <span>Missing Errors</span> a) Element is missing a Property b)
    Element is missing a mandatory Relationship c) Element is missing a
    Property of a Relationship

5.  <span>Declaration Errors</span> a) Element is not declared b)
    Property of a Relationship is not declared

6.  <span>Other errors</span>


