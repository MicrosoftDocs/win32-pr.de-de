---
description: Die SignalTimerFired-Methode gibt den Timerbezeichner frei, der zum Planen des Renderings verwendet wird.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: CBaseRenderer.SignalTimerFired-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f08ed0e8348648d5d1af1127159b414b0ddbc40cfd470ff0834b7bc2b0723e9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052360"
---
# <a name="cbaserenderersignaltimerfired-method"></a>CBaseRenderer.SignalTimerFired-Methode

Die `SignalTimerFired` -Methode clears the timer identifier used to schedule rendering.

## <a name="syntax"></a>Syntax


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Filter ruft diese Methode auf, wenn der Renderingtimer aktiviert wird (siehe [**CBaseRenderer::WaitForRenderTime),**](cbaserenderer-waitforrendertime.md)oder wenn der Timer abgebrochen wird (siehe [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)). Die -Methode setzt die [**CBaseRenderer::m \_ dwAdvise-Membervariable**](cbaserenderer-m-dwadvise.md) auf 0 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




