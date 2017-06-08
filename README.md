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

# Sketch

The work of collecting information about an entity can organized into the following stages

1. **Physical** Collection of physical material.
2. **Tokens** interpeting tokens from the physical material (OCR, typing, scraping) https://plato.stanford.edu/entries/types-tokens/#DisBetTypTok
3. **Signifiers** deciding which tokens are references to entities and attributes
4. **Interpretation of Abstract Claims** interpreting the signifiers of a text to be making an abstract claim about the world (i.e. that **A** person referenced as "John Smith" exists; **A** person referenced as "John Smith" was age 22 at the now-time of this text
5. **Entity Resolution** Positing that a signifier or signifiers are referential to particular entity
6. **Adjudication of Claims** Accepting or rejecting abstract claims for a particular entity

Informing all of this is a data model. This is more or less formal model of the portion of the world that the researcher cares about and her belief about how those portions are related. For example, for security force monitoring, we believe and care to believe that security forces are organizations composoed of sub organizations; these oranizations and suborganizations have names, that they have commanding officers; etc. We believe that those commanding officers are people, and that these people have names, and birthdates, and previous posts. We may also believe that they have favorite colors, but probably won't include that in our model.

The data model determines 

- universe of material we will collect
- what classes of signifiers we care about extracting
- what types of claims we will bother making interpretations about
- what type of claims can be condordant or discordant



