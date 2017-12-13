## Administrative Information
**Proposers name:** Sam Berlow

**Vendor affiliation:** Type Network

**Proposal name:** Optical Axes Proposal

**Date of submission:** 12/12/2017

**New or revised proposal:** New

**Previous revision date:** N/A

Everyone using fonts is familiar with the weight, width and postural (slant) attributes of a typeface family, and many professional typographers are familiar with fonts mastered for different optical size ranges. Traditionally, the most common attributes are available as named font instances (or styles) within font families. These attributes and others are also recorded in the font metadata fields of the OpenType v1.0 specification, such as values in the OS/2 table (e.g. cap height and x-height.)

But these could not be altered by users, and this led to widespread simplification about how typography is formed from the attributes of typefaces. Users want to manipulate more parameters than static font formats contain, or applications could offer. The metadata that was available was mostly for Latin, and the users of world scripts have found difficulties with more limited metadata, especially when mixing scripts on a page for print or digital media.

The variable fonts specification in the OpenType v1.8 font format changes that situation. We see the possibility to solve many typographic problems with it, if it includes a more in-depth and complete set of attributes that users can interact with, or adjust through programming.

OpenType variable fonts launched with registered axes that pertain to some of these attributes, such as width, weight, optical size, and slant. This proposal contains additional axes for attributes that are universal for all scripts and designs, and also some specific to Latin, such as cap height and vertical depth of descenders.

This initial proposal for Latin axes  is interrelated, and forms a gestalt system. The system can be extended with more axes, not in this proposal, for all the world’s scripts. A Latin variable font with these axes can be adjusted to harmonize with a static font from any of those scripts. For example, such a font paired in a document with a non-variable Chinese font can have multiple descender lengths, depending on whether Chinese or Latin is the primary script in a text run. We expect to see single variable fonts that contain several scripts and several sets of glyph group alignment axes.

We carefully chose these axis names and tags to convey their systematic nature. Instead of choosing familiar, common, general terms (like "x height" or "weight" or "spacing") with widely understood meanings, and then dissecting a specific meaning for use in a sharply defined axis using that name, we created names that may at first seem unfamiliar, but are descriptive – and soon become intuitive. 

These names represent a patterned sequence of direction, form and glyph group alignment. This pattern is the foundation for a new kind of discourse about type that has become very convenient internally at Type Network for discussing the details of all kinds of type design projects, variable or not, with our clients, including the Google Fonts team. We have made the distinction between ‘Universal’ parametric axes and ‘Latin’ parametric axes. The naming scheme helps to de-emphasize the Latin script as a default.

We also carefully designed the axes value ranges to form a unified programmable set that is built on typographic tradition, where measures of variation are reasoned about in per-mille-of-em, points, and degrees. This allows users to define spatial values relatively, which is especially useful when specifying typography with variable fonts, or to work with absolute values that can be found in any font.

Most of these axes are “lower level” in that they can be used in concert to define “higher level” axes (like a “weight” or “x height” axis.) Currently this means finding 2 positions on a set of lower level axes, and instantiating them as new masters, to be re-inserted into the design space as the extremes of a new axis. For users, the ability to control the low level parameters of high level type attributes with precision increases the number of typographic problems that they can solve. For typeface designers, their design process is simplified, as the number of masters that they are required to draw from scratch is reduced, while increasing the number of high level axes they can offer users.

Overall, we believe these axes allow type users, especially software developers and educators, to have a clearer picture of how typography is shaped by the attributes of typefaces. A near-future proposal, will follow with an overview containing world script alignments, time-base axes and axes for glyph-referencing among instances.


