---
description: Die folgende Tabelle enthält Rückgabewerte, die von Funktionen zurückgegeben werden können, die ASN.1-Codierung (Abstract Syntax Notation One) ausführen.
ms.assetid: cb1f34dd-dab4-4ffb-a73b-79a214290509
title: ASN.1 Codieren/Decodieren von Rückgabewerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c48bc5bc122f322650c7913ea9d1978d5113da31fa650a23e8f439555d7ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880100"
---
# <a name="asn1-encodingdecoding-return-values"></a>ASN.1 Codieren/Decodieren von Rückgabewerten

Die folgende Tabelle enthält Rückgabewerte, die von Funktionen zurückgegeben werden können, die ASN.1-Codierung [*(Abstract Syntax Notation One)*](../secgloss/a-gly.md) ausführen.



| Definierte Konstante           | Textnachricht                                      | Hexadezimalwert |
|----------------------------|---------------------------------------------------|-------------------|
| CRYPT \_ E \_ ASN1-FEHLER \_      | BASIS des ASN.1-Zertifikats zum Codieren/Decodieren des Rückgabewerts | 0x80093100        |
| CRYPT \_ E \_ ASN1 \_ INTERNAL   | INTERNER ASN.1-Codierungs- oder Decodierungsfehler             | 0x80093101        |
| CRYPT \_ E \_ ASN1 \_ EOD        | ASN.1: Unerwartetes Ende der Daten                      | 0x80093102        |
| CRYPT \_ E \_ ASN1 \_ CORRUPT    | BESCHÄDIGTE ASN.1-Daten                              | 0x80093103        |
| CRYPT \_ E \_ ASN1 \_ LARGE      | ASN.1-Wert zu groß                             | 0x80093104        |
| CRYPT \_ E \_ ASN1-EINSCHRÄNKUNG \_ | ASN.1-Einschränkung verletzt                         | 0x80093105        |
| CRYPT \_ E \_ ASN1 \_ MEMORY     | ASN.1 nicht genügend Arbeitsspeicher                               | 0x80093106        |
| CRYPT \_ E \_ ASN1 \_ OVERFLOW   | ASN.1-Pufferüberlauf                             | 0x80093107        |
| CRYPT \_ E \_ ASN1 \_ BADPDU     | DIE ASN.1-Funktion wird für diese PDU nicht unterstützt.         | 0x80093108        |
| CRYPT \_ E \_ ASN1 \_ BADARGS    | ASN.1 ungültige Argumente für Funktionsaufruf              | 0x80093109        |
| CRYPT \_ E \_ ASN1 \_ BADREAL    | ASN.1 ungültiger realer Wert                              | 0x8009310A        |
| CRYPT \_ E \_ ASN1 \_ BADTAG     | ASN.1 ungültiger Tagwert erreicht                           | 0x8009310B        |
| CRYPT \_ E \_ ASN1 \_ CHOICE     | ASN.1 ungültiger Auswahlwert                            | 0x8009310C        |
| CRYPT \_ E \_ ASN1 \_ RULE       | ASN.1-Regel für ungültige Codierung                           | 0x8009310D        |
| CRYPT \_ E \_ ASN1 \_ UTF8       | ASN.1 bad Unicode (UTF8)                          | 0x8009310E        |
| CRYPT \_ E \_ ASN1-PDU-TYP \_ \_  | UNGÜLTIGER PDU-Typ für ASN.1                                | 0x80093133        |
| CRYPT \_ E \_ ASN1 \_ UNE        | ASN.1 noch nicht implementiert                         | 0x80093134        |
| CRYPT \_ E \_ ASN1 \_ EXTENDED   | ASN.1 übersprungene unbekannte Erweiterungen                  | 0x80093201        |
| CRYPT \_ E \_ ASN1 \_ NOEOD      | ENDE DER ASN.1-Daten erwartet                        | 0x80093202        |



 

 

 
