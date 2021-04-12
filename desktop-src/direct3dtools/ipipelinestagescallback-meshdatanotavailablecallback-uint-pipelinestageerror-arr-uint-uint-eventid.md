---
description: Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen keine Mesh-Daten für das in der zugeordneten Anforderung angegebene Ereignis zurückgeben können.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipipelinestagescallback:: meshdatanotavailablecallback-Methode'
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
ms.openlocfilehash: 42391c342e2f11b39d1535b5286a92e161d0fd9b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482582"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>Ipipelinestagescallback:: meshdatanotavailablecallback-Methode

Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen keine Mesh-Daten für das in der zugeordneten Anforderung angegebene Ereignis zurückgeben können.

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

*anzahlphasen*   
Die Anzahl der zurückgegebenen Phasenfehler.

*count0- \_ Fehler*   
Fehler in der Pipeline Stufe.

*Breite*   
Die Breite der Austausch Kette mit dem Draw-Befehl. Diese wird verwendet, wenn Pipeline-Vorschau Bilder angefordert werden.

*Flugh*   
Die Höhe der Austausch Kette mit dem Draw-Befehl. Diese wird verwendet, wenn Pipeline-Vorschau Bilder angefordert werden.

*VEI*   
Das in den Ergebnissen dargestellte Ereignis.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Ipipelinestagescallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
