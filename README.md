# A list of all features relevant for defining a harmonic segment

*An attempt of reuniting various encodings of harmonic analyses*

## General ideas

* As a minimum, define the extent of a harmonic segment and the chord and non-chord tones defining the harmony (i.e. all pitches considered as non-ornamental)
  * express tones as tonal pitch classes and as interval classes above the bass / lowest note (because the interpretations of what the root is might differ)
* all other expressions of the harmonic content (scale degrees, Roman numeral notation, pitch-class set etc.) can be added on top

## Concrete features (Note level)

* Extent, segment, area of validity
  * beginning (point or region)
  * ending (point or region)
  * [vertical segmentation (which staves form the harmony)]
* Context
  * preceding and subsequent segment
  * relationship to overarching and included segments (e.g. is component of, is composed of, overlaps with...)
  * additional overlap with preceding or subsequent segments (fuzzy boundaries)
* Which pitch classes are considered as part of the harmony (minimum: list of pitches, medium: ordered list, maximum: list of note IDs)
  * chord tones
    * bass / lowest pitch (class)
    * chord root (if applicable)
    * every other chord tone together with the interval class it forms over the bass / lowest pitch
    * for every pitch: information whether it is explicit or implicit in the score
      * boolean?
      * backlinks to non-chord tones replacing a chord tone (see below)?
      * list of occurrences (timestamps + durations (+ octaves), note IDs for a particular score)?
  * non-chord tones considered as belonging to the harmony
    * 
    * suspension/retardation: Which pitch is being suspended? Does the resolution occur in the same segment?
    * organ point / pedal point
    * ... ?
    
 ## Abstract features
 
 * chord type (Mm7, o7, Ger6 etc.)
 * implied key/scale/tonality
   * local key
   * applied key (e.g. `/V`)
 * scale degrees resulting for pitch classes
 * evokes expecation of
 * is part of a sequence
 
 ## General features of a segment that can be derived from the score
 
 * ambitus
 * prevalence of pitches (in the particular octaves)
 * duration
 * metrical positions of pitches (in the particular octaves)
 * shape / contour
 * inner structure
 * density
 * timbre mix
 
