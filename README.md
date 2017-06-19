# dossier
Machine assisted dossiers

"dossier" tool for journalists and researchers backed by dedupe.io. In the complete version, the tool would have

* individual pages for people and organizations,
* with dedupe.io suggesting connections that can be reviewed and accepted by the user
* ability for the user to edit info about the entities
* ability for the user to add relations between people and organizations manually
* ability for the user to maintain notes
* permissioning systems for all of that.

I know this is the type of tool you've though of for a while. It would be great if we could find a time to chat to hear your thoughts and see if we can perhaps pool some resources.


## Prior Art
#### Pudo
- http://pudo.org/blog/2014/03/30/grano.html
- http://untangled.knightlab.com/readings/charting-social-network-analysis-tools.html
- https://github.com/alephdata


## Familysearch.org

## Opencorporates
- https://blog.opencorporates.com/2014/01/08/understanding-corporate-networks-part-4-how-we-record-the-data/

# Sketch

The work of collecting information about an entity can organized into the following stages

### 1 **Physical** Collection of physical material.
In our projects the physical will mean collecting some files. For a security forces example, this could be audio testimony from witnesses and victimes. Collecting news articles or official documentation and scanning.

Here, it is important to collect
- who or what did the collecting. when, where
- if there was transcribing or scanning, who or what did this where


### 2. **Tokens** interpeting tokens from the physical material (OCR, typing, scraping) https://plato.stanford.edu/entries/types-tokens/#DisBetTypTok
Assuming that we are working with physical artifact that we believe to be representations of language, our next step is to interpret these artifacts as a sequence of tokens. If the source artificact is say an "Microsoft Office File", this 'interpretation' may just be reading it as such a file and converting to some more convenient format. If the source artifact is a scanned page, then this interpetation might be done OCR or a human transcriber. Similar for audio.

Here it is important to collect
- who or what did the tokenization, when and where.

###  3. **Signifiers** deciding which tokens are references to entities and attributes
If we have a spreadsheet, this is interpreting that a column called "recipient" contains references to persons who received something. If we have less structured text, the is a tasks of "[Named Entity Recognition](https://en.wikipedia.org/wiki/Named-entity_recognition)" and [Coreference resolution](https://nlp.stanford.edu/projects/coref.shtml). Notice that this is not deciding that a particular token refers to particular entity, but that token refers to **some** entity within a class. 


### 4. **Interpretation of Abstract Claims** 
If we have a spreadsheet that has a columns call "donor", "recipient", and "amount", we might interpret a row of data as making the following claims.

- There exists some entity with designated by the token in the "donor" field.
- There exists some entity with designated by the token in the "recipient" field.
- The entity designated by the token in the "recipient" field recieved an amount of money designed by the "amount" field from the entity designated by the token in the "donor" field

### 5. **Entity Resolution** Positing that a signifier or signifiers are referential to particular entity
We have to often decide which signifiers are signified the **same** thing. 

### 6. **Adjudication of Claims** Accepting or rejecting abstract claims for a particular entity
Upon deciding which signifiers are about the same entity, we resolve the abstract claims to specific claims about entitites. This claims can sometimes conflict. We have to choose which claims to adopt and reject.


### Data Model
Informing all of this is a data model. This is more or less formal model of the portion of the world that the researcher cares about and her belief about how those portions are related. For example, for security force monitoring, we believe and care to believe that security forces are organizations composoed of sub organizations; these oranizations and suborganizations have names, that they have commanding officers; etc. We believe that those commanding officers are people, and that these people have names, and birthdates, and previous posts. We may also believe that they have favorite colors, but probably won't include that in our model.

The data model determines 

- universe of material we will collect
- what classes of signifiers we care about extracting
- what types of claims we will bother making interpretations about
- what type of claims can be condordant or discordant



