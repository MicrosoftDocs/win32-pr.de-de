---
description: Stellt Informationen zu einer Shaderdebuggeranforderung dar.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DebugShaderRequestInfo-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9691b13936ca8ec8e75aa02d9525a9d57143b19e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628459"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo-Struktur

Stellt Informationen zu einer Shaderdebuggeranforderung dar.

## <a name="syntax"></a>Syntax


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a>Member

**Bühne**  
Die zu debuggende Pipelinephase.

**Eventid**  
Die ID des zu debuggenden Grafikereigniss.

**frameNumber**  
Der zu debuggende Frame.

**Scheitelpunkt**  
Der zu debuggende Scheitelpunkt.

**Pixel**  
Das zu debuggende Pixel.

**groupCoordinates**  
Die Koordinaten der zu debuggenden Gruppe.

**threadCoordinates**  
Die Koordinaten des zu debuggenden Threads

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



