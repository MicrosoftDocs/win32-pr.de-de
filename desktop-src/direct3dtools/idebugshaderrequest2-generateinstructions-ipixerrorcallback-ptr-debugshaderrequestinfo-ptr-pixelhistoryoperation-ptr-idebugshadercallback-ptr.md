---
description: Fordert zum Generieren von shaderablaufverfolgungs-Anweisungen in einer Debuganforderung auf. Das Ablauf Verfolgungs basierte Debuggen erfolgt auf der CPU (Warp) anstelle der GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest2:: generateingestructions-Methode'
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
ms.openlocfilehash: e9c1bc2f6b3f885159f21cd7e644545d7639d6b3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521859"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2:: generateingestructions-Methode

Fordert zum Generieren von shaderablaufverfolgungs-Anweisungen in einer Debuganforderung auf. Das Ablauf Verfolgungs basierte Debuggen erfolgt auf der CPU (Warp) anstelle der GPU.

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

*errorcallback*   
Die Adresse eines Rückrufs für Fehler, die beim Erstellen von shaderablaufverfolgungs-Anweisungen auftreten können.

*RequestInfo*   
Die Adresse einer debugshaderrequestinfo-Struktur, die das angeforderte Ereignis/Scheitelpunkt/Pixel beschreibt.

*ppixelhistory*   
Die Adresse der Pixel Verlaufs Ergebnisse, die zum Suchen des zugeordneten Pixels zum Debuggen verwendet werden. Gilt nur beim Debuggen eines Pixelshaders.

*pCallback*   
Die Adresse eines Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
