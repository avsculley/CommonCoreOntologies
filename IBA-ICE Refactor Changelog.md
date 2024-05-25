IBA-ICE Refactor Changelog

May 25, 2024

Added:
1. ***One-dimensional Barcode Content*** =def. A Barcode Content that is encoded as a pattern consisting of one-dimensional symbols arranged as parallel lines.
    ***UPC Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of 6 or 12 numerical digits and is used to scan consumer goods.
        ***UPC-A Barcode Content*** =def. A UPC Barcode Content that is encoded as a pattern consisting in 12 numerical digits.
        ***UPC-E Barcode Content*** =def. A UPC Barcode Content that is encoded as a pattern consisting of 6 numerical digits.
    ***Codabar Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of numerical digits 0-9 and the characters -$:/.+ and is used by logistics and healthcare professionals.
    ***Code 128 Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern of up to 128 ASCII characters and is used primarily in supply chains.
    ***Code 39 Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consistinf of 39 characters that are numbers 0-9, capital letters A-Z, or the symbols -.$/+% and space and is used primarily in automotive and defense industries.
    ***Code 93 Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of up to 93 ASCII characters and is used in logistics to identify packages in retail inventory, lable electornic components, and provide supplementary delivery information.
    ***EAN Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of 8 or 13 numerical digits and is used to scan consumer goods.
        ***EAN8 Barcode Content*** =def. An EAN Barcode Content that is encoded as a pattern consisting of 8 numerical digits and is used to designate products at the point of sale.
        ***EAN13*** =def. An EAN Barcode Content that is encoded as a pattern consisting of 13 numerical digits and is used to designate products at the point of sale.
        ***Jan13 Barcode Content*** =def. An EAN Barcode Content that is encoded as a pattern consisting of 13 numerical digits and is used primarily in Japan to designate products at the point of sale.
        ***ISSN Barcode Content*** =def. An EAN Barcode Content that is used to designate periodicals.
        ***ISBN Barcode Content*** =def. An EAN Barcode Content that is used to designate books.
    ***GS1 DataBar Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of 2-14 numerical digits and is used in retail and healthcare.
    ***ITF Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of an even number of numerical characters and is used primarily in packaging and distribution.
    ***MSI Plessey Barcode Content*** =def. A One-Dimensional Barcode Content that is encoded as a pattern consisting of an indefinite number of numerical characters and is used for inventory control and marking storage containers and shelves in warehouse environments.

2. ***Two-dimensional Barcode Content*** =def. A Barcode Content that is encoded as a pattern consisting of two-dimensional symbols.
    ***Pdf417 Code Content*** =def. A Two-Dimensional Barcode Content that is used in applications that require the storage of huge amounts of data.
    ***QR Code Content*** =def. A Two-Dimensional Barcode Content that is encoded as a pattern consisting of numeric, alphanumeric, binary, or kanji information and is used primarily for tracking and marketing. **I think "information" is wrong here. Perhaps better to use 'symbols.'**
    ***Aztec Code Content*** =def. A Two-Dimensional Barcode Content that is used by the transportation industry to scan tickets.
    ***Data Matrix Code Content*** =def. A Two-Dimensional Barcode Content that is encoded as a pattern consisting of cells arranged in rectangular patterns and is used for marking small items in logistics and operations. **Is it encoded as a pattern consisting of cells arranged in a rectanguar pattern, or it it just cells arranged in a rectangular pattern?**


The corresponding IBAs in AO are reccommended for deprecation.