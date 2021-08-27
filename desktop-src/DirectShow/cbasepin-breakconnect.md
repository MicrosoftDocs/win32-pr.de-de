---
description: 'CBasePin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin von einer Verbindung frei.'
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: CBasePin.BreakConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c40c7614f94b2be5e5f588a706b4b0bd1eec92c3181ffbedcad3ae1e57183f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955229"
---
# <a name="cbasepinbreakconnect-method"></a>CBasePin.BreakConnect-Methode

Die `BreakConnect` -Methode gibt den Pin von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird während der Verbindungstrennung durch die [**CBasePin::D isconnect-Methode**](cbasepin-disconnect.md) aufgerufen. Sie wird auch während eines Verbindungsversuchs aufgerufen, wenn die [**CBasePin::CheckConnect-Methode**](cbasepin-checkconnect.md) fehlschlägt.

Diese Methode muss alle Ressourcen freigeben, die von der **CheckConnect-Methode** abgerufen wurden. Wenn **CheckConnect** beispielsweise Arbeitsspeicher zuweist, `BreakConnect` sollte den Arbeitsspeicher freigeben. Wenn **CheckConnect** den Verbindungsanschluss für eine Schnittstelle abfragt, `BreakConnect` sollte die Schnittstelle freigeben.

Beachten Sie, dass `BreakConnect` ohne einen entsprechenden Aufruf von **CompleteConnect** aufgerufen werden kann. Daher können Sie nicht davon ausgehen, dass **CompleteConnect** zuvor aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




