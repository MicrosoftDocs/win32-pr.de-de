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
ms.openlocfilehash: a9a099b1001c2b8c30398ca350e05d15562a8bc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099438"
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

## <a name="remarks"></a>Bemerkungen

Diese Methode wird während der Verbindungstrennung durch die [**CBasePin::D isconnect-Methode**](cbasepin-disconnect.md) aufgerufen. Sie wird auch während eines Verbindungsversuchs aufgerufen, wenn die [**CBasePin::CheckConnect-Methode**](cbasepin-checkconnect.md) fehlschlägt.

Diese Methode muss alle Ressourcen freigeben, die von der **CheckConnect-Methode** abgerufen wurden. Wenn z. B. **CheckConnect** Arbeitsspeicher zuweist, `BreakConnect` sollte den Arbeitsspeicher freigeben. Wenn **CheckConnect** den Verbindungsanschluss für eine Schnittstelle abfragt, `BreakConnect` sollte die Schnittstelle freigeben.

Beachten Sie, dass `BreakConnect` ohne einen entsprechenden Aufruf von **CompleteConnect** aufgerufen werden kann. Daher können Sie nicht davon ausgehen, dass **CompleteConnect** zuvor aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




