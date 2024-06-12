# IBA-ICE Refactor Changelog

## May 25, 2024

### Added:
1. ***One-dimensional Barcode Content*** =def. A Barcode Content that is encoded as a pattern consisting of one-dimensional symbols arranged as parallel lines.
   1. ***UPC Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of 6 or 12 numerical digits and is used to scan consumer goods.
      1. ***UPC-A Barcode Content*** =def. A UPC Barcode Content that is encoded as a pattern consisting in 12 numerical digits.
      2. ***UPC-E Barcode Content*** =def. A UPC Barcode Content that is encoded as a pattern consisting of 6 numerical digits.
   2. ***Codabar Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of numerical digits 0-9 and the characters -$:/.+ and is used by logistics and healthcare professionals.
   3. ***Code 128 Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern of up to 128 ASCII characters and is used primarily in supply chains.
   4.  ***Code 39 Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consistinf of 39 characters that are numbers 0-9, capital letters A-Z, or the symbols -.$/+% and space and is used primarily in automotive and defense industries.
   5.   ***Code 93 Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of up to 93 ASCII characters and is used in logistics to identify packages in retail inventory, lable electornic components, and provide supplementary delivery information.
   6.  ***EAN Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of 8 or 13 numerical digits and is used to scan consumer goods.
         1.   ***EAN8 Barcode Content*** =def. An EAN Barcode Content that is encoded as a pattern consisting of 8 numerical digits and is used to designate products at the point of sale.
         2.  ***EAN13*** =def. An EAN Barcode Content that is encoded as a pattern consisting of 13 numerical digits and is used to designate products at the point of sale.
         3.  ***Jan13 Barcode Content*** =def. An EAN Barcode Content that is encoded as a pattern consisting of 13 numerical digits and is used primarily in Japan to designate products at the point of sale.
         4.   ***ISSN Barcode Content*** =def. An EAN Barcode Content that is used to designate periodicals.
         5.   ***ISBN Barcode Content*** =def. An EAN Barcode Content that is used to designate books.
   7.   ***GS1 DataBar Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of 2-14 numerical digits and is used in retail and healthcare.
   8.   ***ITF Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of an even number of numerical characters and is used primarily in packaging and distribution.
   9. ***MSI Plessey Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of an indefinite number of numerical characters and is used for inventory control and marking storage containers and shelves in warehouse environments.

2. ***Two-dimensional Barcode Content*** =def. A Barcode Content that is encoded as a pattern consisting of two-dimensional symbols.
   1. ***Pdf417 Code Content*** =def. A Two-Dimensional Barcode Content that is used in applications that require the storage of huge amounts of data.
   2. ***QR Code Content*** =def. A Two-Dimensional Barcode Content that is encoded as a pattern consisting of numeric, alphanumeric, binary, or kanji information and is used primarily for tracking and marketing. **I think "information" is wrong here. Perhaps better to use 'symbols.'**
   3.  ***Aztec Code Content*** =def. A Two-Dimensional Barcode Content that is used by the transportation industry to scan tickets.
   4.  ***Data Matrix Code Content*** =def. A Two-Dimensional Barcode Content that is encoded as a pattern consisting of cells arranged in rectangular patterns and is used for marking small items in logistics and operations. **Is it encoded as a pattern consisting of cells arranged in a rectanguar pattern, or it it just cells arranged in a rectangular pattern?**

### Reccomended
1. The corresponding IBAs in AO are reccommended for deprecation.

## May 26, 2024

### Added:

1. Information Structure Entity
   1. http://www.ontologyrepository.com/CommonCoreOntologies/InformationStructureEntity
   2. definition "A Generically Dependent Continuant that can relate Information Content Entities, and, if it does, partly constitutes an additional Information Content Entity that has it and the related Information Content Entities as parts."
2. List Structure
   1. http://www.ontologyrepository.com/CommonCoreOntologies/ListStructure
   2. definition "An Information Structure Entity that can sequentially relate discrete Information Content Entities in an ordered or unordered manner."@en
   3. 'definition source' "https://en.wikipedia.org/wiki/List"^^xsd:anyURI
3. List Content
   1. definition "An Information Content Entity that is encoded with some List Structure."
4. List
   1. definition "An Information Bearing Artifact that is carrier of some List Content."
  
### Removed:
1. Original IBA definition of 'List'

## June 3, 2024

### Added:

1. Counterparts to IBA subclasses in the Cyber Ontology. These terms still need definitions, and the IBAs need to be edited such that they follow the pattern 'X is a IBA that is carrier of Y.' _**Note:**_ I have not done anything that would promote any term in Cyber to the midlevel. I have only edited Cyber such that it is more consistent with the refactor.

## June 4, 2024

### Added:

#### Object Properties

1. is_generically_dependent_part_of definition "x is generically dependent part of y =def. x & y are instances of generically dependent continuant, and x is continuant part of y."@en **_Note:_** Perhaps should be in BFO.
   1. is_information_structure_of definition "x is information structure of y =def. x is an instance of information structure entity, y is an instance of Information Content Entity, and x is generically dependent continuant part of y."@en
   2. is_information_content_part_of definition "x is information content part of y =def. x & y are instances of Information Content Entity, and x is generically dependent continuant part of y."@en
  
2. Inverse of the above.

## June 6, 2024

### Changes:

1. 'is_information_structure_of' to 'is_generic_structure_of'

### Additions:

#### GDC Branch

1. Generic Structure Entity =def. definition "A Generically Dependent Continuant that can relate Generically Dependent Continuants, and if it does, partly consititutes an additional Generically Dependent Continuant along with the Generically Dependent Continuants it relates."@en
   1. Database Structure (currently no def)
   2. Spreadsheet Structure (currently no def)
3. Generic Glyph Entity =def. definition "A Generically Dependent Continuant whose concretization can concretize some Information Content Entity wholly."@en
   1. Primitive Generic Glyph Entity =def. definition "A Generic Glyph Entity that does not extend in any direction in logical space."@en
      1. 'example of usage' "The GDCs concretized by 'X', 'F', 'L', '.', ',', '!', '1', '2', '3'."@en
   3. Composite Generic Glyph Entity =def. definition "A Generic Glyph Entity that has generically dependent continuant part some Generic Structure Entity."@en

#### ICE Branch

1. Book Content =def. definition "A Document Content intended to be consumed by a relatively general audience and whose concretization is of substantial length."@en
2. Video Content =def. definition "A Document Content consisting of a sequence of Image Contents that are intended to be presented in temporal sequence and perceived as a visual whole."@en
3. Database content is now equivalent to an ICE that has generic structure some Database Structure.
4. Spreadsheet content is now equivalent to an ICE that has generic structure some Database Structure.
5. Document Form Content =def. definition "An Information Content Entity generically depends on some Document Form."@en


## June 12, 2024 (currently writing this)

### Overall Changes

Here is a first draft of the refactor. In the following, I will address changes that were made to the GDC branch, and as I do I will address the corresponding changes to the IBA branch. There is no need to read the above changes, as some of them were the result of scope creep which has been fixed in the following.

#### High-level Changes
1. I added the class 'Information Entity' defined as "A Generically Dependent Continuant whose concretizations can facilitate some Act of Communication."
   1. The justification for this is threefold. First, it allows me to later refer to the subclasses of the term in other definitions. Second, it adds sematic content to the subclasses, namely, that they can facilitate acts of communication. Third, it future-proofs the GDC branch, which might later include further groups of GDCs, like Mathematical Entities, or any other entities which are specific to certain domains. Structures, for example, are found in most domains (math, physics, biology, sociology), but this project just focuses on _Information_ structures.
2. I added the class 'Information Structure Entity' defined as "An Information Entity that can relate Information Entities, and if it does, partly consititutes an additional Information Entity along with the Information Entities it relates."
   1. The justification for this is that there are some information entities that need to be defined in terms of their structure. For example, Databases and Spreadsheets.
4. I added the class 'Information Glyph Entity' defined as "An Information Entity whose concretization can concretize some Information Content Entity wholly."
   1. The justification for this is that some entities, like Barcodes, need to be defined in terms of the marks used to represent them. 'Wholly' is meant to distinguish glyphs from structures, since concretizations of the latter can _partially_ concretize Information Content Entities insofar as they are parts of glyphs.
5. I changed the definition of Information Content Entity to reflect that it is now a subclass of 'Information Entity,' instead of 'Generically Depedent Continuant.'
6. I added subclasses of 'continuant part of' (and its inverse, but I won't mention those changes since they're somewhat redundant).
   1. generically_dependent_continuant_part_of
   2. information_structure_of
   3. information_content_part_of
