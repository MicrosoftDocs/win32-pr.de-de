---
description: Stellt eine Pipelinephase dar, einschließlich Details zum verwendeten Shader.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PipeLineStage-Struktur
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
ms.openlocfilehash: 10f1d1780404303109a72fe1a12023bc35b2c0ca
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625166"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>PipeLineStage-Struktur

Stellt eine Pipelinephase dar, einschließlich Details zum verwendeten Shader.

## <a name="syntax"></a>Syntax


```C++
} PipeLineStage;
```

## <a name="members"></a>Member

**StageId**  
Die ID der Pipelinephase.

**Debugfähigen**  
TRUE, wenn die Pipelinephase das Debuggen unterstützt; andernfalls FALSE.

**StageName**  
Eine COM-Zeichenfolge, die den Namen der Pipelinephase enthält.

**GuaranteedOutput**  
TRUE, wenn die Pipelinephase immer über eine Pipelineausgabe verfügt; andernfalls FALSE.

**DebugEntryPoint**  
Eine COM-Zeichenfolge, die den Namen des Shader-Einstiegspunkts enthält, sofern eine solche Zeichenfolge vorgibt.

**ShaderFile**  
Eine COM-Zeichenfolge, die den Dateipfad der Shader-Quelldatei enthält.

**ShaderByteStreamPtr**  
Eine FILEPTR für den Shader-Bytestream. Dies wird zum Debuggen zurück übergeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



