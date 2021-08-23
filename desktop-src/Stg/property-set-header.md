---
title: Eigenschaftensatzheader
description: Am Anfang des Eigenschaftensatzdatenstroms befindet sich ein Header. Sie besteht aus einem Byte-Reihenfolgenindikator, einer Formatversion, der ursprünglichen Betriebssystemversion, dem Klassenbezeichner (CLSID) und einem reservierten Feld.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Strukturierte Eigenschaftensatzheader Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506249ae917c6fbf00853a2547188a08ce14ebb29bc24d7e6daaa1aaa830cb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662220"
---
# <a name="property-set-header"></a>Eigenschaftensatzheader

Am Anfang des Eigenschaftensatzdatenstroms befindet sich ein Header. Sie besteht aus einem Byte-Reihenfolgenindikator, einer Formatversion, der ursprünglichen Betriebssystemversion, dem Klassenbezeichner (CLSID) und einem reservierten Feld.

Die folgende Pseudostruktur veranschaulicht den -Header.

``` syntax
typedef struct tagPROPERTYSETHEADER 
{ 
    // Header 
    WORD   wByteOrder ;  // Always 0xFFFE 
    WORD   wFormat ;     // Always 0 
    DWORD   dwOSVer ;    // System version 
    CLSID  clsID ;       // Application CLSID 
    DWORD  reserved ;    // Should be 1 
} PROPERTYSETHEADER;
```

 

 




