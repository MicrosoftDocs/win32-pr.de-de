---
description: Ein Rückruf, der den Host darüber benachrichtigt, welche Pipelinestufen keine Meshdaten für das in der zugeordneten Anforderung angegebene Ereignis zurückgeben können.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback::MeshDataNotAvailableCallback-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9c95f661c5a18f2573fe477f3aa1ef4d0035ee1e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622136"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback-Methode

Ein Rückruf, der den Host darüber benachrichtigt, welche Pipelinestufen keine Meshdaten für das in der zugeordneten Anforderung angegebene Ereignis zurückgeben können.

## <a name="syntax"></a>Syntax


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a>Parameter

*numberStages*   
Die Anzahl der zurückgegebenen Phasenfehler.

*\_count0-Fehler*   
Die Fehler in der Pipelinephase.

*Breite*   
Die Breite der Swapkette, die mit dem Zeichnen-Aufruf assocaitiert ist. Dies wird beim Anfordern von Pipelinevorschaubildern verwendet.

*Höhe*   
Die Höhe der Swapkette, die mit dem Zeichnen-Aufruf assocaitiert wurde. Dies wird beim Anfordern von Pipelinevorschaubildern verwendet.

*eid*   
Das in den Ergebnissen dargestellte Ereignis.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
