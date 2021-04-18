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
# <a name="section"></a><span data-ttu-id="0a6ae-103">`Section`</span><span class="sxs-lookup"><span data-stu-id="0a6ae-103">Section</span></span>

<span data-ttu-id="0a6ae-104">Der Abschnitt ist der dritte Teil des Eigenschaften Satz-Streams und enthält die tatsächlichen Eigenschaften Satz Werte.</span><span class="sxs-lookup"><span data-stu-id="0a6ae-104">The section is the third part of the property set stream and contains the actual property set values.</span></span>

<span data-ttu-id="0a6ae-105">Ein Abschnitt enthält:</span><span class="sxs-lookup"><span data-stu-id="0a6ae-105">A section contains:</span></span>

-   <span data-ttu-id="0a6ae-106">Byte Anzahl für den Abschnitt, der die Byte Anzahl selbst einschließt.</span><span class="sxs-lookup"><span data-stu-id="0a6ae-106">Byte count for the section which is inclusive of the byte count itself.</span></span>
-   <span data-ttu-id="0a6ae-107">Array von 32-Bit-Eigenschaften-ID/Offset-Paaren.</span><span class="sxs-lookup"><span data-stu-id="0a6ae-107">Array of 32-bit Property ID/Offset pairs.</span></span>
-   <span data-ttu-id="0a6ae-108">Array von Eigenschaftentyp-Indikatoren/Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="0a6ae-108">Array of property Type Indicators/Value pairs.</span></span>

<span data-ttu-id="0a6ae-109">Offsets sind der Abstand zwischen dem Anfang des Abschnitts und dem Anfang des Eigenschafts Paars (Typ, Wert).</span><span class="sxs-lookup"><span data-stu-id="0a6ae-109">Offsets are the distance from the start of the section to the start of the property (type, value) pair.</span></span> <span data-ttu-id="0a6ae-110">Dadurch kann ein Abschnitt ohne Übersetzung der internen Struktur als Bytearray kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a6ae-110">This allows a section to be copied as an array of bytes without any translation of internal structure.</span></span>

<span data-ttu-id="0a6ae-111">Die folgenden Pseudo Strukturen veranschaulichen das Format eines-Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="0a6ae-111">The following pseudo-structures illustrate the format of a section.</span></span>

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

 

 




