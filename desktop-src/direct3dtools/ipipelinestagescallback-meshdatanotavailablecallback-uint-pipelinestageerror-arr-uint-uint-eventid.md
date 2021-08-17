---
description: Ein Rückruf, der den Host benachrichtigt, von welchen Pipelinestufen keine Meshdaten für das in der zugeordneten Anforderung angegebene Ereignis zurückgegeben werden können.
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
ms.openlocfilehash: 41fbedaa6deaf2a799f8d721309bfbe1b44bc2110dfae0a3cf30a4afbe0fa1f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276080"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback-Methode

Ein Rückruf, der den Host benachrichtigt, von welchen Pipelinestufen keine Meshdaten für das in der zugeordneten Anforderung angegebene Ereignis zurückgegeben werden können.

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
Die Pipelinephasenfehler.

*Breite*   
Die Breite der Vertauschkette, die mit dem Zeichnen-Aufruf assocaited wurde. Dies wird verwendet, wenn Pipelinevorschauimages angefordert werden.

*Höhe*   
Die Höhe der Swapkette, die mit dem Draw-Aufruf assocaited wurde. Dies wird verwendet, wenn Pipelinevorschauimages angefordert werden.

*im 19.*   
Das in den Ergebnissen dargestellte Ereignis.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
