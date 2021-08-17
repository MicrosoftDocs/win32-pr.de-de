---
description: Stellt Informationen zu einer Quellcodedatei dar.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SourceFileInfo-Struktur
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
ms.openlocfilehash: 9b6afd5f3b383aff5c6d5168b259b13fe4429ac40d5b19a21c8e2f6a207cecd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119234"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo-Struktur

Stellt Informationen zu einer Quellcodedatei dar.

## <a name="syntax"></a>Syntax


```C++
} SourceFileInfo;
```

## <a name="members"></a>Member

**fileName**  
Eine COM-Zeichenfolge, die den Dateipfad der zugeordneten Quelldatei enthält.

**checksumByteCount**  
Die Anzahl der Bytes in der Prüfsumme. Wenn checkSumAlgorithm gleich CHECKSUMALGORITHM::md5 ist, ist checkSumByteCount 16. Wenn checkSumAlgorithm gleich CHECKSUMALGORITHM::sha1 ist, ist checkSumByteCount 20.

**checkSumAlgorithm**  
Gibt den Algorithmus an, der zum Generieren der Prüfsumme der Datei verwendet wird. Unterstützte Algorithmen sind MD5 und SHA1. Weitere Informationen finden Sie in der CHECKSUMALGORITHM-Enumeration.

**checkSumFirstPart**  
Der erste 8-Byte-Teil der Prüfsumme.

**checkSumSecondPart**  
Der zweite 8-Byte-Teil der Prüfsumme.

**checkSumThirdPart**  
Der dritte 8-Byte-Teil der Prüfsumme.

**checkSumFourthPart**  
Der vierte 8-Byte-Teil der Prüfsumme.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



