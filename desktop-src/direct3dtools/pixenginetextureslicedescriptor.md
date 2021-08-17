---
description: Stellt eine Beschreibung eines Texturslices dar.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureSliceDescriptor-Struktur
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
ms.openlocfilehash: 915ef0158ca4c38eb6f9bbfe7bd3f1baf400b42a37b8f300e3f042bd610204c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119294"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor-Struktur

Stellt eine Beschreibung eines Texturslices dar.

## <a name="syntax"></a>Syntax


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a>Member

**width**  
Die Breite (Anzahl der Stichproben auf der X-Achse) des Slices.

**height**  
Die Höhe (Anzahl der Stichproben auf der Y-Achse) des Slices.

**blockRowBytes**  
Die Anzahl der Bytes pro Zeile in jedem Block.

**offset**  
Der Offset des Slices innerhalb der gesamten Textur.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



