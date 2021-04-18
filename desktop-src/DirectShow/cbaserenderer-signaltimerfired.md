---
description: Die signaltimerfired-Methode löscht den Zeit Geber Bezeichner, der zum Planen des Rendering verwendet wurde.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Cbaserderderer. signaltimerfired-Methode (renbase. h)
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
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364528"
---
# <a name="cbaserenderersignaltimerfired-method"></a>Cbaserderderer. signaltimerfired-Methode

Die- `SignalTimerFired` Methode löscht den Zeit Geber Bezeichner, der für die Zeit Plan Rendering

## <a name="syntax"></a>Syntax


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Filter ruft diese Methode auf, wenn der rendertimer aktiviert wird (siehe [**cbaserenderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md)) oder wenn der Timer abgebrochen wird (siehe [**cbaserenderer:: cancelnotification**](cbaserenderer-cancelnotification.md)). Die-Methode setzt die Element Variable [**cbaserenderer:: m \_ DW-**](cbaserenderer-m-dwadvise.md) Member auf NULL zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




