---
description: Stellt eine Beschreibung eines Textur Formats dar.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixenginetextureformatdebug-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957965"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span id="vspixengine.pixenginetextureformatdesc"></span>Pixenginetextureformatdebug-Struktur

Stellt eine Beschreibung eines Textur Formats dar.

## <a name="syntax"></a>Syntax


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a>Member

**dxgiformat**  
Das DXGI-Format der Textur.

**DataFormat**  
Das Datenformat der Textur.

**blockbytes**  
Die Anzahl von Bytes in einem Datenblock.

**blockheight**  
Die Höhe (Number Samples in der Y-Achse) des Blocks.

**blockWidth**  
Die Breite (Anzahl der Stichproben in der X-Achse) des Blocks.

**channelx**  
Beschreibt die Eigenschaften des X-Kanals. Weitere Informationen finden Sie in der pixenginechanneldescription-Struktur.

**channelely**  
Beschreibt die Eigenschaften des Y-Kanals. Weitere Informationen finden Sie in der pixenginechanneldescription-Struktur.

**channelz**  
Beschreibt die Eigenschaften des Z-Kanals. Weitere Informationen finden Sie in der pixenginechanneldescription-Struktur.

**channelw**  
Beschreibt die Eigenschaften des W-Kanals. Weitere Informationen finden Sie in der pixenginechanneldescription-Struktur.

**Swizzle**  
Beschreibt das auf das Beispiel angewendete Swizzle (Channel-Swap).

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



