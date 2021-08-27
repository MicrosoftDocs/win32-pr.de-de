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
ms.openlocfilehash: b10d66a7843198f86eeaebcf8f49b13abdd8c100
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625546"
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

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



