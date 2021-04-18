---
title: '`Section`'
description: Der Abschnitt ist der dritte Teil des Eigenschaften Satz-Streams und enthält die tatsächlichen Eigenschaften Satz Werte.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f51891d14a9690e295379b7bcf619fe0fbe19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340618"
---
# <a name="section"></a>`Section`

Der Abschnitt ist der dritte Teil des Eigenschaften Satz-Streams und enthält die tatsächlichen Eigenschaften Satz Werte.

Ein Abschnitt enthält:

-   Byte Anzahl für den Abschnitt, der die Byte Anzahl selbst einschließt.
-   Array von 32-Bit-Eigenschaften-ID/Offset-Paaren.
-   Array von Eigenschaftentyp-Indikatoren/Wert-Paaren.

Offsets sind der Abstand zwischen dem Anfang des Abschnitts und dem Anfang des Eigenschafts Paars (Typ, Wert). Dadurch kann ein Abschnitt ohne Übersetzung der internen Struktur als Bytearray kopiert werden.

Die folgenden Pseudo Strukturen veranschaulichen das Format eines-Abschnitts.

``` syntax
typedef struct tagPROPERTYSECTIONHEADER 
{ 
    DWORD  cbSection ;    // Size of Section 
    DWORD  cProperties ;  // Count of Properties in section 
} PROPERTYSECTIONHEADER; 
 
typedef struct tagPROPERTYIDOFFSET 
{ 
    DWORD  propid;    // Name of property 
    DWORD  dwOffset;  // Offset from start of section to property 
} PROPERTYIDOFFSET; 
 
typedef struct tagSERIALIZEDPROPERTYVALUE 
{ 
    DWORD  dwType;    // Property Type 
    BYTE   rgb[];     // Property Value 
} SERIALIZEDPROPERTYVALUE ;
```

 

 




