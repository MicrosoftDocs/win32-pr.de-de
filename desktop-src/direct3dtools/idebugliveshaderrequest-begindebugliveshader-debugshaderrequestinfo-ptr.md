---
description: Anforderungen zum Debuggen eines Shaders auf der GPU (Live Debugging) vs CPU (Ablauf Verfolgungs basiertes Debuggen).
MS-HAID: vspixengine.IDebugLiveShaderRequest\_BeginDebugLiveShader\_DebugShaderRequestInfo\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Idebugliveshaderrequest:: begindebugliveshader-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 805B2B68-C251-4192-85A3-F857B3F204C7
api_name:
- IDebugLiveShaderRequest.BeginDebugLiveShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b09bff6a414df620e06263e13d94c2f39e36903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746752"
---
# <a name="span-idvspixengineidebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptrspanidebugliveshaderrequestbegindebugliveshader-method"></a><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>Idebugliveshaderrequest:: begindebugliveshader-Methode

Anforderungen zum Debuggen eines Shaders auf der GPU (Live Debugging) vs CPU (Ablauf Verfolgungs basiertes Debuggen).

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginDebugLiveShader(
   DebugShaderRequestInfo * requestInfo
);
```

## <a name="parameters"></a>Parameter

*RequestInfo*   
Die Adresse einer debugshaderrequestinfo-Struktur, die das angeforderte Ereignis/Scheitelpunkt/Pixel beschreibt.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Idebugliveshaderrequest**](/windows/desktop/direct3dtools/idebugliveshaderrequest)

 

 
