---
description: Stellt eine Beschreibung eines Textur Slice dar.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixenginetextureslicedescriptor-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b80a23a5ec3340b775c314f66651926743249ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123980"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span id="vspixengine.pixenginetextureslicedescriptor"></span>Pixenginetextureslicedescriptor-Struktur

Stellt eine Beschreibung eines Textur Slice dar.

## <a name="syntax"></a>Syntax


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a>Member

**width**  
Die Breite (Anzahl der Stichproben in der X-Achse) des Slice.

**height**  
Die Höhe (Anzahl der Stichproben auf der Y-Achse) des Slice.

**blockrowbytes**  
Die Anzahl der Bytes pro Zeile in jedem Block.

**offset**  
Der Offset des Slice innerhalb der gesamten Textur.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



