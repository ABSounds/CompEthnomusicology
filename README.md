# A Study of the Rhythmic Complexity of the Different Tempo Ranges of Arab-Andalusian Music

This research project explores the rhythmic complexities present in Arab-Andalusian music and how they vary across different tempo ranges. The project proposes a measure of complexity and applies it to a dataset of annotated scores to identify the differences in the distribution of rhythm complexity between the different forms of the _nawba_ (classical Arab-Andalusian composition).

## Tempo Ranges
The _nawba_ typically includes three main tempo ranges, performed in order of increasing tempo: _muassa‘_ (slow), _mahzūz_ (medium), and _inṣirāf_ (fast).

## Dataset
The dataset used for this task is the Arab-Andalusian Music (AAM) dataset [4] from Music Technology Group in Barcelona. It contains 158 nawba scores in .xml format, including metadata for the nawbas, lyrics, and information about the sections that compose each of the scores. For this paper, five of these scores were analyzed.

## Methodology
To compare the complexity of the compositions targeting each of the tempo ranges, a "complexity" measure is proposed. To measure this complexity of each of the tempo ranges, the Python library music21[5] was used. From the annotated scores, only the _muassa‘_, _mahzūz_, and _inṣirāf_ sections were taken, and all notes contained in them were analyzed.

Considering the time signature of each of the sections (and changes in time signature inside the same section), three "complexity" levels were established:
- Level 0: notes starting on the beat.
- Level 1: notes starting any amount of 8th note positions after the beat.
- Level 2: notes starting on a 16th note position.
- Level 3: notes starting on a 32nd note position or 16th note triplets.

The number of occurrences of each of the complexity levels for all the analyzed scores are noted and compared to the total number of notes as a percentage.

## Usage
This repository provides a iPython Notebook that can be used to analyze and compare the complexity of Arab-Andalusian music compositions across different tempo ranges. The script requires the music21 library to be installed, as well as the AAM dataset in .xml format.

Once installed, run all the cells in the `RhythmComplexity_TempoRanges_Analysis.ipynb` file.

## Conclusion
This project was part of the Audio and Music Processing Lab as part of the Master's in Sound and Music Computing. It provides insights into the rhythmic characteristics of Arab-Andalusian music and highlights the potential for further research using similar computational methods and tools.