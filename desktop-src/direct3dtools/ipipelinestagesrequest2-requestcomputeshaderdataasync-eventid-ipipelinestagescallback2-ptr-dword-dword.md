---
description: Eine asynchrone Anforderung zum Aufrufen von Compute-shaderdaten für die angegebene Verteilung.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest2:: requestcomputeshaderdataasync-Methode'
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
ms.openlocfilehash: cf0d4725d8d2172900a96e58b4c8786ca2a9c851
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346205"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2:: requestcomputeshaderdataasync-Methode

Eine asynchrone Anforderung zum Aufrufen von Compute-shaderdaten für die angegebene Verteilung.

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

*EventID*   
Das angegebene Dispatch-Ereignis.

*requestCallback*   
Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.

*requestcookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.

*progressintervalmsekunden*   
Nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPipeLineStagesRequest2**](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
