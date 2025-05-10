# LinearSpectrumGenerator

# Description
LinearSpectrumGenerator is a Python script that computes the linear spectrum of a given peptide sequence. The linear spectrum is a collection of all possible subpeptides (including the full peptide) of a given sequence, where the mass of each subpeptide is calculated based on the provided amino acid mass table. The script returns the sorted linear spectrum, which can be useful for mass spectrometry analysis and peptide identification.

# Functionality
linear_spectrum(peptide, amino_acid_mass)
Purpose: Computes the linear spectrum of a peptide by considering all subpeptides, calculating their masses, and sorting them.

# Approach:

* Uses the prefix mass array technique to efficiently compute the masses of all possible subpeptides in the sequence.
* Computes the mass of each subpeptide by using a cumulative sum (prefix_mass).
* Returns the sorted list of all subpeptide masses, which represents the linear spectrum of the peptide.

# Parameters
peptide (str): The input peptide sequence (e.g., "IAMT").

amino_acid_mass (dict): A dictionary mapping amino acid residues to their respective masses (e.g., {'G': 57, 'A': 71, ...}).

# Returns
list: A sorted list of masses corresponding to all subpeptides of the input peptide.

# Example Usage
```
amino_acid_mass = {
    'G': 57, 'A': 71, 'S': 87, 'P': 97, 'V': 99, 'T': 101, 'C': 103, 'I': 113,
    'L': 113, 'N': 114, 'D': 115, 'K': 128, 'Q': 128, 'E': 129, 'M': 131, 'H': 137,
    'F': 147, 'R': 156, 'Y': 163, 'W': 186
}

peptide = "IAMT"

result = linear_spectrum(peptide, amino_acid_mass)
print(result)
```

# Output Example:
[0, 71, 101, 113, 131, 184, 202, 232, 303, 315, 416]

# Applications
* This script is useful for various bioinformatics applications, including:
* Mass Spectrometry Data Analysis: Helps in interpreting experimental data by comparing the observed spectrum to theoretical linear spectra.
* Peptide Identification: Assists in peptide matching and identification using mass spectrometry data.
* Proteomics Research: Used in peptide characterization and protein sequence analysis.
* Computational Biology: Supports the development of algorithms for protein sequencing and structure prediction.

# Requirements
* Python 3.x
* No external libraries required.

# License
This project is licensed under the MIT License – see the LICENSE file for details.









