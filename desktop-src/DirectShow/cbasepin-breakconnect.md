---
description: Die breakconnect-Methode gibt die PIN von einer Verbindung frei.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Cbasepin. breakconnect-Methode (amfilter. h)
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
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354793"
---
# <a name="cbasepinbreakconnect-method"></a>Cbasepin. breakconnect-Methode

Die- `BreakConnect` Methode gibt die PIN von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird während der PIN-Trennung durch die [**cbasepin::D isconnect**](cbasepin-disconnect.md) -Methode aufgerufen. Sie wird auch während eines Verbindungsversuchs aufgerufen, wenn die [**cbasepin:: checkConnect**](cbasepin-checkconnect.md) -Methode fehlschlägt.

Diese Methode muss alle Ressourcen freigeben, die von der **checkConnect** -Methode abgerufen wurden. Wenn **checkConnect** z. b. Arbeitsspeicher belegt, `BreakConnect` sollte den Arbeitsspeicher freigeben. Wenn **Check Connect** die Verbindungs-PIN für eine Schnittstelle abfragt, `BreakConnect` sollte die Schnittstelle freigeben.

Beachten Sie, dass `BreakConnect` ohne einen entsprechenden Aufruf von **completeconnect** aufgerufen werden kann. Daher können Sie nicht davon ausgehen, dass **completeconnect** bereits zuvor aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




