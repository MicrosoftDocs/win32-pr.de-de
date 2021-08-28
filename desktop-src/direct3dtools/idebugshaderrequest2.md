---
description: 'Anforderung zum Starten des Debuggens eines Shaders. Diese Anforderung besteht aus zwei Teilen: Generieren einer Ablaufverfolgung und Debuggen einer Ablaufverfolgung.'
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: faf884a0235e08af47618809e62155c9c31e644e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622956"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2-Schnittstelle

Anforderung zum Starten des Debuggens eines Shaders. Diese Anforderung besteht aus zwei Teilen: Generieren einer Ablaufverfolgung und Debuggen einer Ablaufverfolgung.

## <a name="members"></a>Member

Die **IDebugShaderRequest2-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDebugShaderRequest2** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IDebugShaderRequest2-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">Beschreibung</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></td><td style="text-align: left;"><p>Anforderungen zum Starten des Debuggens der angegebenen Liste von Anweisungen.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></td><td style="text-align: left;"><p>Anforderungen zum Generieren von Shader-Ablaufverfolgungsanweisungen in einer Debuganforderung. Das ablaufverfolgungsbasierte Debuggen erfolgt auf der CPU (Warp) anstelle der GPU.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
