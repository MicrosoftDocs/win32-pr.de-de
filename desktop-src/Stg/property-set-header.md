---
title: Eigenschaften Satz Header
description: Am Anfang des Eigenschaften Satz-Streams ist ein-Header. Sie besteht aus einem Byte Reihenfolge Indikator, einer Format Version, der Ursprungs Betriebssystemversion, der Klassen Kennung (CLSID) und einem reservierten Feld.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Strukturierter Speicher für Eigenschaften Satz Header
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8d66eeec6525414ba3c6f0a0bb4f4fa34431c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311574"
---
# <a name="property-set-header"></a>Eigenschaften Satz Header

Am Anfang des Eigenschaften Satz-Streams ist ein-Header. Sie besteht aus einem Byte Reihenfolge Indikator, einer Format Version, der Ursprungs Betriebssystemversion, der Klassen Kennung (CLSID) und einem reservierten Feld.

In der folgenden Pseudo Struktur wird der-Header veranschaulicht.

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

 

 




