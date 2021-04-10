---
title: Format Bezeichner/Offset-paar
description: Der zweite Teil des Eigenschaften Satz-Streams enthält ein Format Bezeichner/Offset-Paar.
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f80a85175278b92fedbfd7b2d50d94007b7e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309811"
---
# <a name="format-identifieroffset-pair"></a><span data-ttu-id="ead46-103">Format Bezeichner/Offset-paar</span><span class="sxs-lookup"><span data-stu-id="ead46-103">Format Identifier/Offset Pair</span></span>

<span data-ttu-id="ead46-104">Der zweite Teil des Eigenschaften Satz-Streams enthält ein Format Bezeichner/Offset-Paar.</span><span class="sxs-lookup"><span data-stu-id="ead46-104">The second part of the property set stream contains one Format Identifier/Offset Pair.</span></span> <span data-ttu-id="ead46-105">Die fmtid ist der Name der Eigenschaften Gruppe. Es identifiziert eindeutig, wie der Inhalt des folgenden Abschnitts interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ead46-105">The FMTID is the name of the property set; it uniquely identifies how to interpret the contents of the following section.</span></span> <span data-ttu-id="ead46-106">Der Offset ist die Entfernung in Bytes vom Beginn des gesamten Streams bis zum Beginn des Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="ead46-106">The Offset is the distance, in bytes, from the start of the whole stream to where the section begins.</span></span>

<span data-ttu-id="ead46-107">Die folgende Struktur ist hilfreich bei der Verarbeitung von Format Bezeichnern/Offset-Paaren.</span><span class="sxs-lookup"><span data-stu-id="ead46-107">The following structure is helpful in handling Format Identifier/Offset Pairs.</span></span>

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




