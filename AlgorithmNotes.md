# Algorithm Notes

## Initial Thoughts
Semitones may play a *key* (yes, there will be puns) part in this algorithm. What seems clear is definitely a class that instantiates a chord object for every single given note in a chord. The purpose of this is to establish a different chord object for every possible root note to account for all keys and ultimately all chord possibilities.

For example, given the notes X C E G C E, from left to right being the deepest/lowest strings on the guitar:
The low E string is not included, therefore, the anticipated root note for this chord falls on note on the next lowest string, the C note on the A string.
By creating a chord object based around the C note as the root, I can use semitones to automatically fill in every single possible interval variant.

Every key contains the notes A B C D E F G. By assuming the root note is C, then we can arrange the chord object so that notes are in such order starting with the root:
C D E F G A B
 
 //////////////////////////////////////////////////////////
Next I need to integrate semitones somehow. The problem is I need semitones to determine what the note actually is so that I can compared the note with the user's entered note.
////////////////////////////////////////////////////////

Root Note: C
//////////// Unfilled out, need to figure out this section
/////////////////////////////////////////////////////////
Sus2: 2 semitones
Minor Third (m3): 3 semitones
Major Third (3): 4 semitones
Sus4: 5 semitones
Diminished Fifth (b5): 6 semitones
Perfect Fifth (5): 7 semitones
Augmented Fifth (#5): 8 semitones
Minor Sixth (b6): 8 semitones
Major Sixth (6): 9 semitones
Diminished Seventh (dim7): 9 semitones
Minor Seventh (b7): 10 semitones
Major Seventh (maj7): 11 semitones
Diminished Ninth (b9): 1 semitone (or 1 semitone above the root)
Major Ninth (9): 10 semitones
Augmented Ninth (#9): 11 semitones
Perfect Eleventh (11): 10 semitones
Augmented Eleventh (#11): 11 semitones
Diminished Thirteenth (b13): 8 semitones above the 7th
Major Thirteenth (13): 9 semitones above the 7th