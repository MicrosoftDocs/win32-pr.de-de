---
description: Stellt eine Pipeline Stufe dar, einschließlich Details zum verwendeten Shader.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pipelinestage-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957875"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>Pipelinestage-Struktur

Stellt eine Pipeline Stufe dar, einschließlich Details zum verwendeten Shader.

## <a name="syntax"></a>Syntax


```C++
} PipeLineStage;
```

## <a name="members"></a>Member

**Stageid**  
Die ID der Pipeline Stufe.

**Debugfähigen**  
true, wenn die Pipeline Stufe Debuggen unterstützt. andernfalls false.

**StageName**  
Eine com-Zeichenfolge, die den Namen der Pipeline Stufe enthält.

**"Zuder Ausgabe"**  
true, wenn die Pipeline Phase immer eine Pipeline Ausgabe aufweist. andernfalls false.

**Debug-Einstiegspunkt**  
Eine com-Zeichenfolge, die den Namen des Shader-Einstiegs Punkts enthält, sofern vorhanden.

**Shaderfile**  
Eine com-Zeichenfolge, die den filePath der Shader-Quelldatei enthält.

**Shaderbytestreamptr**  
Ein "fleptr" für den Shader-Bytestream. Dies wird zurückgegeben, um zu debuggen.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



