---
description: Anforderungen zum Generieren von Shader-Ablaufverfolgungsanweisungen in einer Debuganforderung. Das ablaufverfolgungsbasierte Debuggen erfolgt auf der CPU (Warp) anstelle der GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest2::GenerateInstructions-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3af0e624435c03416db0bf8d74bc3aa8418ae78
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625156"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2::GenerateInstructions-Methode

Anforderungen zum Generieren von Shader-Ablaufverfolgungsanweisungen in einer Debuganforderung. Das ablaufverfolgungsbasierte Debuggen erfolgt auf der CPU (Warp) anstelle der GPU.

## <a name="syntax"></a>Syntax


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a>Parameter

*errorCallback*   
Die Adresse eines Rückrufs für Fehler, die beim Generieren von Shader-Ablaufverfolgungsanweisungen auftreten können.

*requestInfo*   
Die Adresse einer DebugShaderRequestInfo-Struktur, die das angeforderte Ereignis/den angeforderten Scheitelpunkt/Pixel beschreibt.

*pPixelHistory*   
Die Adresse der Pixelverlaufsergebnisse, die zum Suchen des zugeordneten zu debuggende Pixels verwendet werden. Gilt nur beim Debuggen eines Pixel-Shaders.

*pCallback*   
Die Adresse eines Rückrufs, der verwendet wird, um den Host über Ergebnisse zu benachrichtigen.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
