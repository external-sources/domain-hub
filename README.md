# Yggdrasil

This projects aim's to replace [hosts-sources](https://github.com/external-sources/hosts-sources) as it is an outdated
and unpractical way to collect, store and search for records.

I have chosen the name Yggdrasil over Odin, as Yggdrasil have its roots everywhere, while Odin might be the God of
wisdom, then he needs to rely on his ravens to obtain knowledge from the nine realms.

## Goals

1. Import external sources, such as hosts, json, plain text files and MariaDB
2. Load the data into some Database; this could be json, CSV or MariaDB.
3. Sort by first domain, then URI, at last by category.
4. Keep track of the sources for domain and URI records
5. Make a search command that can sort and list results
    1. Sort output by source, then records
    2. Sort output sorted (clean format), no sources
    3. Output from none DNS sources like EasyList, uBlock and Adguard.
    4. Output records from My Privacy DNS project [Matrix](https://github.com/mypdns/matrix)
    5. Output MyPDNS RPZ records, extract directly from MariaDB
6. Manage Matrix records. (Add,Delete.Alter) to:
    1. PowerDNS Auth server's API <https://docs.powerdns.com/authoritative/http-api/zone.html>
    2. Alter the source files within the Matrix [source/](https://github.com/mypdns/matrix/tree/master/source)
       directory.
7. Incorporate PyFunceble for availability test before committing
8. Future, working with a webcrawler that can categorize sites and scripts to search for primarily trackers and adult
   sites

## About Yggdrasil

Yggdrasil (from Old Norse Yggdrasil) is an immense and central sacred tree in Norse cosmology. Around it exists all
else, including the Nine Worlds.

Yggdrasil is attested in the Poetic Edda compiled in the 13th century from earlier traditional sources, and in the Prose
Edda compiled in the 13th century by Snorri Sturluson. In both sources, Yggdrasil is an immense ash tree that is central
to the cosmos and considered very holy. The gods go to Yggdrasil daily to assemble at their traditional governing
assemblies. The branches of Yggdrasil extend far into the heavens, and the tree is supported by three roots that extend
far away into other locations; one to the well Urðarbrunnr in the heavens, one to the spring Hvergelmir, and another to
the well Mímisbrunnr. Creatures live within Yggdrasil, including the dragon Níðhöggr, an unnamed eagle, and the stags
Dáinn, Dvalinn, Duneyrr and Duraþrór.

Scholars generally consider Hoddmímis holt, Mímameiðr, and Læraðr to be other names for the tree. The tree is an example
of sacred trees and groves in Germanic paganism and mythology, and scholars in the field of Germanic philology have long
discussed its implications.

## Etymology

The generally accepted meaning of Old Norse Yggdrasill is "Odin's horse", meaning "gallows". This interpretation comes
about because drasill means "horse" and Ygg(r) is one of Odin's many names. The Poetic Edda poem Hávamál describes how
Odin sacrificed himself by hanging from a tree, making this tree Odin's gallows. This tree may have been Yggdrasil. "The
horse of the hanged" is a kenning for gallows and therefore Odin's gallows may have developed into the expression "
Odin's horse", which then became the name of the tree.

Nevertheless, scholarly opinions regarding the precise meaning of the name Yggdrasill vary, particularly on the issue of
whether Yggdrasill is the name of the tree itself or if only the full term askr Yggdrasil (where Old Norse askr means "
ash tree") refers specifically to the tree. According to this interpretation, askr Yggdrasils would mean the world tree
upon which "the horse [Odin's horse] of the highest god [Odin] is bound". Both of these etymologies rely on a presumed
but unattested *Yggsdrasill.

A third interpretation, presented by F. Detter, is that the name Yggdrasill refers to the word yggr ("terror"), yet not
in reference to the Odinic name, and so Yggdrasill would then mean "tree of terror, gallows". F. R. Schröder has
proposed a fourth etymology according to which yggdrasill means "yew pillar", deriving yggia from *igwja (meaning "
yew-tree"), and drasill from *dher- (meaning "support").

## Attestations

### Poetic Edda

In the Poetic Edda, the tree is mentioned in the three poems Völuspá, Hávamál and Grímnismál.

### Völuspá

In the second stanza of the Poetic Edda poem Völuspá, the völva (a shamanic seeress) reciting the poem to the god Odin
says that she remembers far back to "early times", being raised by jötnar, recalls nine worlds and nine ídiðiur (
rendered in a variety of ways by translators—Dronke, for example, provides "nine wood-ogresses"), and when Yggdrasil was
a seed ("glorious tree of good measure, under the ground"). In stanza 19, the völva says:

> An ash I know there stands,  
> Yggdrasill is its name,  
> a tall tree, showered  
> with shining loam.  
> From there come the dews  
> that drop in the valleys.  
> It stands forever green over  
> Urðr's well.

In stanza 20, the völva says that from the lake under the tree come three "maidens deep in knowledge" named Urðr,
Verðandi, and Skuld. The maidens "incised the slip of wood", "laid down laws" and "chose lives" for the children of
mankind and the destinies (ørlǫg) of men. In stanza 27, the völva details that she is aware that "Heimdallr's hearing is
couched beneath the bright-nurtured holy tree." In stanza 45, Yggdrasil receives a final mention in the poem. The völva
describes, as a part of the onset of Ragnarök, that Heimdallr blows Gjallarhorn, that Odin speaks with Mímir's head, and
then:

> Yggdrasill shivers,  
> the ash, as it stands.  
> The old tree groans,  
> and the giant slips free.

### Hávamál

In stanza 138 of the poem Hávamál, Odin describes how he once sacrificed himself to himself by hanging on a tree. The
stanza reads:

> I know that I hung on a windy tree  
> nine long nights,  
> wounded with a spear, dedicated to Odin,  
> myself to myself,  
> on that tree of which no man knows  
> from where its roots run

In the stanza that follows, Odin describes how he had no food nor drink there, that he peered downward, and that "I took
up the runes, screaming I took them, then I fell back from there." Odin later used "the knowledge of the sacred runes"
as a magical tool to give to mankind to increase humans' skill in magic and poetry.

While Yggdrasil is not mentioned by name in the poem and other trees exist in Norse mythology, the tree is near
universally accepted as Yggdrasil by scholars, and if the tree is Yggdrasil, then the name Yggdrasil directly relates to
this story.

### Grímnismál

In the poem Grímnismál, Odin (disguised as Grímnir) provides the young Agnar with cosmological lore. Yggdrasil is first
mentioned in the poem in stanza 29, where Odin says that, because the "bridge of the Æsir burns" and the "sacred waters
boil," Thor must wade through the rivers Körmt and Örmt and two rivers named Kerlaugar to go "sit as judge at the ash of
Yggdrasill". In the stanza that follows, a list of names of horses are given that the Æsir ride to "sit as judges" at
Yggdrasil.

In stanza 31, Odin says that the ash Yggdrasil has three roots that grow in three directions. He details that beneath
the first lives Hel, under the second live frost jötnar, and beneath the third lives mankind. Stanza 32 details that a
squirrel named Ratatoskr must run across Yggdrasil and bring "the eagle's word" from above to Níðhöggr below. Stanza 33
describes that four harts named Dáinn, Dvalinn, Duneyrr and Duraþrór consume "the highest boughs" of Yggdrasil.

In stanza 34, Odin says that more serpents lie beneath Yggdrasil "than any fool can imagine" and lists them as Góinn and
Móinn (possibly meaning Old Norse "land animal"), which he describes as sons of Grafvitnir (Old Norse, possibly "
ditch wolf"), Grábakr (Old Norse "Greyback"), Grafvölluðr (Old Norse, possibly "the one digging under the plain"
or possibly amended as "the one ruling in the ditch"), Ófnir (Old Norse "the winding one, the twisting one"),
and Sváfnir (Old Norse, possibly "the one who puts to sleep = death"), who Odin adds that he thinks will forever
gnaw on the tree's branches.

In stanza 35, Odin says that Yggdrasil "suffers agony more than men know", as a hart bites it from above, it decays on
its sides, and Níðhöggr bites it from beneath. In stanza 44, Odin provides a list of things that are what he refers
to as the "noblest" of their kind. Within the list, Odin mentions Yggdrasil first, and states that it is the "noblest of
trees".
