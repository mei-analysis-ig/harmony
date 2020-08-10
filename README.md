# A list of all features relevant for defining a harmonic segment

*An attempt of reuniting various encodings of harmonic analyses*

## General ideas

* As a minimum, define the extent of a harmonic segment and the chord and non-chord tones defining the harmony (i.e. all pitches considered as non-ornamental) **--> concrete features**
  * express tones as tonal pitch classes and add the octaves in which each occurs; from there intervallic representations can be derived at will
  * there should be a closed set of necessary features that always need to be defined for guaranteeing a minimum of interoperability
* all other expressions of the harmonic content (scale degrees, Roman numeral notation, pitch-class set etc.) can be added on top **--> abstract features**

## Concrete features (Note level)

This list tries to be exhaustive but some features will probably remain explicit. For example, the ending of a segment is often implicitly encoded through the beginning of the next one.

* Extent, segment, area of validity
  * beginning (point or region)
  * ending (point or region)
  * (special cases?) vertical segmentation (which notes are part of the harmony?): list of note IDs? List of staves?
* Context
  * preceding and subsequent segment
  * relationship to overarching and included segments (e.g. is component of, is composed of, overlaps with...)
  * additional overlap with preceding or subsequent segments (fuzzy boundaries)
* Which pitch classes are considered as part of the harmony (list of pitch classes, ordered on the line of fifths, each pitch class having octave(s) information added)
  * chord tones
    * bass / lowest pitch (class)
    * chord root (if applicable)
    * every other chord tone together with the interval class it forms over the bass and/or (?) over the root
    * for every pitch: information whether it is explicit or implicit in the score
      * boolean?
      * backlinks to non-chord tones replacing a chord tone (see below)?
      * list of occurrences (timestamps + durations (+ octaves), note IDs for a particular score)?
  * non-chord tones considered as belonging to the harmony
    * suspension/retardation: Which pitch is being suspended? Does the resolution occur in the same segment?
    * organ point / pedal point
    * ... ?
    
 ## Abstract features
 
 This will always be an open list, since new harmony standards can be added in the future.
 
 * chord type (Mm7, o7, Ger6 etc.)
 * implied key/scale/tonality
   * local key
   * applied key (e.g. `/V`)
 * scale degrees resulting for pitch classes
 * evokes expecation of
 * is part of a (particular) sequence
 * is part of a cadence
 
 ### Feature Matrix
 
 This table can serve as a test whether the concrete features suffice to derive the abstract features required for the different harmony systems.
 
 | features > standard v | segmentation & context | root            | bass                      | intervals over root          | intervals over bass          | distinction chord vs. non-chord tones |
|-----------------------|------------------------|-----------------|---------------------------|------------------------------|------------------------------|---------------------------------------|
| Absolute Chords       | +                      | + (pitch class) | + (pitch class)           | + (chord type)               | -                            | + (chord type vs. parantheses)        |
| Funktionstheorie      | +                      | + (function)    | + (root interval)         | + (all additions)            | -                            | + (function vs. additions)            |
| Roman Numerals        | +                      | + (numeral)     | + (implicit in inversion) | + (alterations, suspensions) | + (inversion)                | + (numeral + inversion vs. additions) |
| Bassstufen            | +                      | -               | + (numeral)               | -                            | + (figured bass conventions) | -                                     |
 
 
 ## General features of a segment that can be derived from the score
 
 These are features that can be used to characterize any kind of score segment and don't necessarily form part of a metamodel of harmony.
 
 * ambitus
 * prevalence of pitches (in the particular octaves)
 * duration
 * metrical positions of pitches (in the particular octaves)
 * shape / contour
 * inner structure
 * density
 * timbre mix
 
