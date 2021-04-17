---
description: Stellt Informationen über eine Shader-Debuggeranforderung dar.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Debugshaderrequestinfo-Struktur
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
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521587"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span id="vspixengine.debugshaderrequestinfo"></span>Debugshaderrequestinfo-Struktur

Stellt Informationen über eine Shader-Debuggeranforderung dar.

## <a name="syntax"></a>Syntax


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a>Member

**inszeniert**  
Die zu debuggende Pipeline Phase.

**EventID**  
Die ID des zu debuggenden Grafik Ereignisses.

**Framezahl**  
Der zu debuggende Frame.

**Vertex**  
Der zu debuggende Scheitelpunkt.

**Megapixel**  
Das zu debuggende Pixel.

**groupkoordinaten**  
Die Koordinaten der Gruppe, die debuggt werden soll.

**Thread Koordinaten**  
Die Koordinaten des zu debuggenden Threads.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



