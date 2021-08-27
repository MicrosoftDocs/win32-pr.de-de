---
description: Eine asynchrone Anforderung zum Abrufen von Compute-Shaderdaten für die angegebene Verteilung.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesRequest2::RequestComputeShaderDataAsync-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F73EA7B4-9E20-4BFD-8F87-20CE0B6C96D8
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderDataAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9ec24a7bf33ef62c658a80afd278a52c0291cb0
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626507"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderDataAsync-Methode

Eine asynchrone Anforderung zum Abrufen von Compute-Shaderdaten für die angegebene Verteilung.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestComputeShaderDataAsync(
   EventID                    eventID,
   IPipeLineStagesCallback2 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*Eventid*   
Das angegebene Dispatchereignis.

*requestCallback*   
Die Adresse des Rückrufs, der verwendet wird, um den Host über Ergebnisse zu benachrichtigen.

*requestCookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert und verwendet werden kann, um zu signalisieren, dass sie abgebrochen wird.

*progressIntervalMsecs*   
Nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPipeLineStagesRequest2**](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
