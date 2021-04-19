---
description: Die notifysample-Methode gibt alle Threads frei, die auf Beispiele warten.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Cbasezucator. notifysample-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356040"
---
# <a name="cbaseallocatornotifysample-method"></a>Cbasezucator. notifysample-Methode

Die- `NotifySample` Methode gibt alle Threads frei, die auf Beispiele warten.

## <a name="syntax"></a>Syntax


```C++
void NotifySample();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Threads auf Beispiele warten, ist der Wert von [**cbasezucator:: m \_ lwaiting**](cbaseallocator-m-lwaiting.md) größer als 0 (null). Wenn *m \_ lwaiting* größer als 0 (null) ist, ruft diese Methode die **ReleaseSemaphore** -Funktion auf dem [**cbasezucator:: m \_ hsem**](cbaseallocator-m-hsem.md) -Semaphore auf und aktiviert alle wartenden Threads. Außerdem wird *m \_ lwaiting* auf Null zurückgesetzt.

Diese Methode wird innerhalb der [**cbasezucator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) -Methode aufgerufen, wenn eine Stichprobe an die freie Liste zurückgegeben wird. und aus der [**cbasebelegcator::D ecommit**](cbaseallocator-decommit.md) -Methode, wenn für die Zuweisung ein Commit ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




