---
title: '`Section`'
description: Der Abschnitt ist der dritte Teil des Eigenschaftensatzstreams und enthält die tatsächlichen Eigenschaftssatzwerte.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bca5dd2801e437ecfffe663f2702abc4c202d721ecbda8a9b95656e40a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682800"
---
# <a name="section"></a>`Section`

Der Abschnitt ist der dritte Teil des Eigenschaftensatzstreams und enthält die tatsächlichen Eigenschaftssatzwerte.

Ein Abschnitt enthält Folgendes:

-   Byteanzahl für den Abschnitt, der die Byteanzahl selbst einschließt.
-   Array von 32-Bit-Eigenschafts-ID/Offset-Paaren.
-   Array von Eigenschaftstypindikatoren-Wert-Paaren.

Offsets sind der Abstand zwischen dem Anfang des Abschnitts und dem Anfang des Eigenschaftspaars (Typ, Wert). Dadurch kann ein Abschnitt ohne Übersetzung der internen Struktur als Bytearray kopiert werden.

Die folgenden Pseudostrukturen veranschaulichen das Format eines Abschnitts.

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

 

 




