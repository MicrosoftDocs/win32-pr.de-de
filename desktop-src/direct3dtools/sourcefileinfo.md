---
description: Stellt Informationen zu einer Quell Code Datei dar.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Sourcefileingefo-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481990"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>Sourcefileingefo-Struktur

Stellt Informationen zu einer Quell Code Datei dar.

## <a name="syntax"></a>Syntax


```C++
} SourceFileInfo;
```

## <a name="members"></a>Member

**fileName**  
Eine com-Zeichenfolge, die den filePath der zugeordneten Quelldatei komprimiert.

**checksumb-tecount**  
Die Anzahl der Bytes in der Prüfsumme. Wenn checksumalgorithm gleich checksumalgorithm:: MD5 ist, lautet checksumb-Zähler 16. Wenn checksumalgorithm gleich checksumalgorithm:: SHA1 ist, lautet checksumb-Zähler 20.

**checksumalgorithm**  
Gibt den Algorithmus an, der zum Generieren der Prüfsumme der Datei verwendet wird. Unterstützte Algorithmen sind MD5 und SHA1. Weitere Informationen finden Sie unter checksumalgorithm-Aufzählung.

**checksumfirstpart**  
Der erste 8-Byte-Teil der Prüfsumme.

**checksumsecondpart**  
Der zweite 8-Byte-Teil der Prüfsumme.

**checksumthirdpart**  
Der dritte 8-Byte-Teil der Prüfsumme.

**checksumfourthpart**  
Der vierte 8-Byte-Teil der Prüfsumme.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



