---
title: "Digital Emblem (DIEM) Use Cases"
abbrev: "DIEM Use Cases"
category: info
docname: draft-diem-fainchtein-protocol-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: AREA
workgroup: DIEM Working Group
keyword:
venue:
  group: WG
  type: Working Group
  mail: WG@example.com
  arch: https://example.com/WG
  github: USER/REPO
  latest: https://example.com/LATEST

author:
  -
    fullname: Rahel A. Fainchtein
    organization: JHU/APL
    email: rahel.fainchtein@jhuapl.edu

  -
    fullname: Casey Deccio
    organization: Brigham Young University
    email: casey@deccio.net

  -
    fullname: Brian Haberman
    organization: Fastly
    email: brian@innovationslab.net

  -
    fullname: Bill Woodcock
    organization: PCH
    email: woody@pch.net

  -
    fullname: Allison Mankin
    organization: PCH
    email: allison.mankin@gmail.com

  -
    fullname: Alex Rosenberg
    organization: Veridigo
    email: alexr@veridigo.com

normative:
  RFC2119:
  RFC8174:

informative:
  BLUEHELMET:
    target: https://guide-humanitarian-law.org/content/article/3/peacekeeping/
    title: The Practical Guide to Humanitarian Law
    author:
       org: Doctors Without Borders
  BLUESHIELD:
    target: https://www.unesco.org/en/heritage-armed-conflicts/enhanced-protection-cultural-property-highest-importance-humanity
    title: Enhanced Protection - Cultural Property of Highest Importance to Humanity
    author:
       org: United Nations Educational, Scientific and Cultural Organization
  REDCROSS:
    target: https://www.icrc.org/en/doc/assets/files/other/protection_emblems.pdf
    title: The Protection of the Red Cross / Red Crescent Emblems
    author:
       org: International Committee of the Red Cross
  PRESS:
    target: https://safety.rsf.org/appendix-i-protection-of-journalists-in-war-zones/
    title: RSF Resource for Journalists' Safety
    author:
       org: Reporters Without Borders
  DIPLOMAT:
    target: https://www.law.cornell.edu/cfr/text/19/148.83
    title: Personnel of Foreign Governments and International Organizations and Special Treatment for Returning Individuals
    author:
       org: Cornell Law School - Legal Information Institute
  RAMSAR:
    target: https://www.ramsar.org
    title: The Convention on Wetlands
    author:
       org: Convention on Wetlands Secretariat
  ISPM15:
    target: https://www.ippc.int/static/media/files/publication/en/2019/02/ISPM_15_2018_En_WoodPackaging_Post-CPM13_Rev_Annex1and2_Fixed_2019-02-01.pdf
    title: "International Standards for Phytosanitary Measures No. 15: Regulation of Wood Packaging Material in International Trade"
    author:
       org: International Plant Protection Convention, Food and Agriculture Organization of the United Nations
  UNMODELREGS:
    target: https://unece.org/transport/dangerous-goods/un-model-regulations-rev-23
    title: "UN Model Regulations on the Transport of Dangerous Goods"
    author:
       org: United Nations Economic and Social Council
  HARMONIZED:
    target: https://www.wcotradetools.org/en/harmonized-system
    title: "Harmonized System"
    author:
       org: World Customs Organization
...

--- abstract

International law defines a number of emblems, such as the blue helmets of United Nations peacekeeping forces,
the blue and white shield of UNESCO, and the Red Cross of the International Committee of the Red Cross, as indicative
of special protections under the Geneva Conventions. Similar protections attach to journalists who wear "Press" protective
emblems on the battlefield, under Article 79 of Protocol I of the Geneva Conventions and Resolution 2222 of the United
Nations Security Council. The emblems of national governments and inter-governmental organizations protect diplomatic
pouches, couriers, and envoys under the Vienna Convention on Diplomatic Relations. Other marks enjoy protections against
mis-use under the Paris Convention, the Madrid Protocol, and the Trade-Related Aspects of Intellectual Property Rights.

This document provides an initial summary of problems placing emblems into digital use cases 
and documents identified requirements
from a number of stakeholders with active or potential interests in digital emblems.
To Do: align abstract and document with the WG charter.


--- middle

# Introduction

International law defines a number of emblems, such as the blue helmets of United Nations (UN) peacekeeping forces {{BLUEHELMET}},
the blue and white shield of UNESCO {{BLUESHIELD}}, and the Red Cross of the International Committee of the Red Cross (ICRC) {{REDCROSS}},
as indicative of special protections under international law. Similar protections attach to journalists who wear "Press" protective
emblems on the battlefield {{PRESS}}. The emblems of national governments and inter-governmental organizations protect diplomatic
pouches, couriers, and envoys {{DIPLOMAT}}, and international law protects certain marks against counterfeiting.


# Conventions and Definitions

{::boilerplate bcp14-tagged}

# Limitations of Physical Emblems

Physical emblems have served a number of key functions over hundreds of years and continue to do so to this day.
As technology advances and newer capabilities become
available, it is beneficial to examine limitations with existing emblems and identify potential needs going forward.

The following describes a number of limitations with physical emblems that may be addressed with digital emblems as complements.

## Authenticity

It is generally not possible to evaluate the authenticity of a physical emblem in real-time. Physical emblems do not carry any type of
attestation from an authorized party indicating the validity of emblem. Mis-use of a physical emblem requires a post-facto investigation.

## Visibility

Physical emblems may not always be visible to an observing party. They can be difficult or impossible to see in the dark. The physical emblem
may be deployed on the opposite side of an object from an observing party. They may be difficult to observe from a distance or at
an oblique angle. The visibility of a physical emblem may be affected by wear, vandalism, or obfuscation.

## Mis-use

Physical emblems may not provide sufficient context to indicate the validity of their observed use. Physical emblems requested for use in a specific
location and/or at a certain time can be re-used at other locations or times that are not authorized. Limited capabilities exist to correlate the
validity of a physical emblem with specific locations, times, items, or people subject to protection. 

## Management

As noted above, potential mis-use of a physical emblem typically requires a post-facto investigation. There is no mechanism to revoke
the instance of a physical emblem that has been abused, compromised, or is no longer valid.

# Notional Requirements for Digital Emblems

Because there are multiple use cases for digital emblems, some of which are fundamentally different
from one another, it is not presumed that any one use of a digital emblem would necessarily have all or most of these requirements
for a given implementation. In this vein, the working group will identify a core set of baseline requirements for digital emblems.
Additional use cases will require further extensions. ToDo: move potential requirements which are outside the initial scope of the WG to a separate section.

## Potential Identification Requirements

A digital emblem capable of acting as an official marking of legal significance needs to be identifiable by its intended purpose
and what assets it applies to. To do this, digital emblems may have these requirements (identified in relation to diverse use cases).  Requirements of particular use cases will vary.

- Provide a clearly detectable and unambiguous marking mappable to enable verification,
- Be machine-readable to enable automated verification,
- Be capable of carrying a visual representation of the physical emblem it represents,
- Carry an unambiguous indication of the international law, laws or agreement pertaining to the entity marked with the emblem,
- Be possible to associate with a range or specific quantity of persons or items,
- Be possible to associate with online services (e.g., websites, email servers, databases),
- Be possible to associate with data in transit or at rest,
- Be possible to associate with network-addressable equipment (e.g., routers, servers, laptops, IoT devices),
- Be possible to associate with a physical object (e.g., building, vehicle, container),
- Be possible to associate with a person or group of people

## Potential Distribution Requirements

A digital emblem applicable to a variety of physical and digital assets will need to support discovery mechanisms
to ensure emblem verification is a practical process. Practicality can mean multiple things, including
minimizing the risk that verifying emblems will disclose verifier presence or behavior, minimizing the cost of verifying digital
emblems, and ensuring universal access to emblem-bearing for legally entitled assets.

To accomplish practical emblem distribution, digital emblems can have requirements to...

- Not impose an undue cost to verify,
- Not impose an undue cost to apply to or remove from an asset,
- Not impose an undue cost to acquire authority to deploy,
- Not require verifiers of the emblem to reveal to the emblem bearer that existence checking is occurring,
- Not prevent verifiers of the emblem from revealing to the emblem bearer that existence checking is occurring,
- Make it possible to view an emblem via a communications network,
- Make it possible to view an emblem optically (e.g. QR code), or wirelessly (e.g. RFID) ToDo: this is an example of a potential requirement that will be outside the initial scope of the working group.

## Potential Trust model requirements

A digital emblem needs to be trustworthy in order to provide any value. This means that parties verifying the presence of emblems need to
know that the asset bearing an emblem is entitled to do so for the declared asset, time frame, and other scopes. 

- Be authorized by a party that has the legal authority to issue it,
- Identify the authorizing party that issued it to ensure accountability of emblem use,
- Carry an unambiguous indication of the international law or laws conferring protection upon the entity marked with the emblem,
- Be capable of providing a reference to additional relevant information (e.g., photographs, unique identifiers) which can be used to corroborate the association of the digital emblem with the entity bearing it,
- Be revocable when they are no longer valid,
- Be restrictable by temporal scope,
- Be restrictable by geographic scope,
- Be robust against being replayed by invalid bearers,
- Be robust against forgery of its various properties.

# Security Considerations

A key part of this document highlights some risks surrounding physical emblems. Technical implementations of digital emblems will undoubtedly
incur their own security considerations. However, this document does not propose technical solutions; it enumerates  use cases that justify
creating technical solutions and potential requirements.  Many of the potential requirements pertain to possible security and privacy directions.


# Use Cases for Digital Emblems
Digital emblems are verifiable labels that can be associated with an entity so
that a verifier can prove that the entity (person, place, or thing) has some property the digital emblem represents.
This is a collection of brief use cases that necessitate the creation of one or more standards for
digital emblems to be used to express some status of the entity bearing them.
Each use case contains a list of potential attributes to associate with the entity as a
part of the emblem. It is assumed that each use case would contain a link or reference to the
law, regulation, or policy that governs the protections granted under the emblem.

These use cases come from discussions with the organizations identified. This is a representative (not exhaustive) list
of use cases for digital emblems.

## International Committee of the Red Cross (ICRC)
The ICRC is responsible for the visual Red Cross, Red Crescent, and Red Crystal emblems
used to label physical assets such as buildings and vehicles so that wartime combatants know
that International Humanitarian Law (IHL) forbids attacking that asset. The ICRC has been challenging
private industry and academic researchers to create a digital equivalent to these visual
emblems that can be used to label digital assets as protected under IHL the same way they
can label physical assets today.

* Indication of location
* Textual description

The ICRC has shared the following concrete use cases as part of their industry
and academic research engagement.

### Labeling web servers
Ensuring that attackers targeting a server hosting websites the attacker wishes to compromise know that the server hosting those sites is IHL protected.

### Labeling personal-use devices
Doctors use laptops to process IHL protected data both on hospital premises and on the move.

### Labeling power-constrained devices
IoT devices are used to manage various equipment within hospitals, and their power constraints may pose unique limitations on digital emblem solutions.

### Labeling networks from within
A device on a network that was compromised by a non-network path (such as malware loaded from a USB device) needs to discover that it compromised a network that is IHL protected (distinct from discovering the compromised device is protected).

### Labeling networks from without
Attackers trying to compromise a network through a network path can discover an emblem for an IP address for a NAT or gateway behind which are IHL protected assets.

### Miscellaneous
Other valuable use cases may exist across the following areas:
protections of buildings (e.g., hospitals), people (e.g., aid workers), vehicles
(e.g., ambulances), objects (e.g., medical devices), digital services (e.g., family
reunification services), and data at-rest & in-transit. Permission to use an emblem is delegated
to each UN member nation.

## United Nations
UN Peacekeepers may require protective markings in theater as well as facilities associated
with the mission.

## United Nations Educational, Scientific, and Cultural Organization (UNESCO)
Requires protections for items of cultural heritage, both physical and digital. Priority is on
buildings and physical artworks. These can be denoted with location information, descriptions,
and linked images. There is a special concern with repatriating stolen works, which would benefit
from a provenance trail via an emblem. Their is also an interest in ensuring that a physical instantiation
of an emblem accompany each artwork and leverage the digital emblem to track the current location and
any special handling needed.

* Indication of location
* Image(s)
* Textual description
* Chain-of-custody / provenance

## Organization for the Prohibition of Chemical Weapons (OPCW)
Requires protection of Schedule 1 chemicals in transit between signatory countries for research,
medical, pharmaceutical, or protective purposes. Emblem would identify place, date, and volume
of production. Also a need to encrypt the description/characteristics of the items for access only
by the receiving customs agencies and material handlers. This encryption precludes other actors from
determining the contents being transported.

* Indication of location (dynamic as materials are moved)
* Indication of quantity
* Textual description

## International Atomic Energy Agency (IAEA)
IAEA administers several treaties, especially related to the controlled shipment of atomic fuels and wastes
across borders. Similar use case as OPCW.

## Basel Convention
Regulates the trans-boundary movement of hazardous wastes. Use cases are functionally identical to OPCW and IAEA.

## Press
Journalists in conflict zones require protective markings that indicate their status as a non-combatant.

## Ramsar Convention on the Wetlands (UNESCO)
The Convention on Wetlands of International Importance especially as Waterfowl Habitat "providees the single most global framework for intergovernmental cooperation on wetland issues" and it features a list of geographic areas designated by Member States.  A digital emblem for the geographic areas potentially requires
* Indication of location
* Access to presence or absence of Ramsar designation of a specified location
* Textual description
* Ability to validate the presence or absence of Ramsar designation

## World Intellectual Property Organization (WIPO)
WIPO administers 26+ treaties with different protections for different things. Brands that are
protected under international law (e.g., Madrid Protocol) can mark their shipments with an emblem
allowing customs agents to positively identify legitimate products.

* Copyright/Brand image
* Textual description
* Chain-of-custody / provenance

## International Civil Aviation Organization (ICAO)
Requires protection of civil aviation flights and the ability to assert that they are not dual-use (i.e., not
carrying military cargo). Digital emblem would carry a geographic description of the flight plan, its current
location, and an indicator of its identity (i.e., tail number). Potential need for the emblem to reference a flight manifest.

* Indication of location
  * Flight plan is static
  * Current location is dynamic
* Textual description (i.e., manifest, identifying characteristics such as tail number)

## World Health Organization (WHO)
Similar use case as the ICRC.

## United Nations Food and Agriculture Organization (FAO)
Among other things is responsible for the International Plant Protection Convention (IPPC) and
International Standards for Phytosanitary Measures standards including ISPM 15 {{ISPM15}} that requires wood
packaging materials (pallets, crates, dunnages) to be debarked, heat-treated or fumigated with
methyl-bromide, and stamped or branded with a compliance mark known as a "wheat stamp."

## United Nations Economic and Social Council (ECOSOC)
UN Model Regulations {{UNMODELREGS}} includes "Recommendations on the Transport of Dangerous Goods." This includes labeling of
items with a four digit "UN Number" that indicates the comounds contained within, such as chemicals, explosives,
flammable liquids, etc. For example, items containing lithium-based batteries are labeled with 3480 or 3481 and
accompanied by a specific "battery mark" emblem.

## World Customs Organization (WCO)
Specifies "Harmonized Systems" codes {{HARMONIZED}} that classify items such as livestock, arms and ammunition, chemicals, plastics,
machinery, foodstuffs, etc. They also provide a system for labeling origin of items and valuation of items, all
enforced by numerous international trade agreements between individual nations and groups of nations.

# IANA Considerations

This document has no IANA actions.

# Contributors
Tony DeSimone, Kerstin Vignard, and Erin Hahn provided insight into the legal and policy issues surrounding emblems.
Tommy Jensen, Felix Linker and Mauro Vignati provided many of the requirements that derive from digital asset use cases.

--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
