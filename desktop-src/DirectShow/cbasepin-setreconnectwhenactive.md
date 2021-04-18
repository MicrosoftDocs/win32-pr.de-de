---
description: Die Methode "streconnect-Active" gibt an, ob die PIN dynamische erneute Verbindungen unterstützt.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Cbasepin. cbasept-Active-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358203"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a>Cbasepin. abtreconnect. Active-Methode

Die- `SetReconnectWhenActive` Methode gibt an, ob die PIN dynamische erneute Verbindungen unterstützt.

## <a name="syntax"></a>Syntax


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bcanreconnect* 
</dt> <dd>

Boolescher Wert, der angibt, ob die PIN dynamisch erneut eine Verbindung herstellen kann. **True** gibt an, dass die PIN dynamisch erneut eine Verbindung herstellen kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Standardmäßig müssen Sie einen Filter vor dem erneuten Verbinden der Pins abbrechen. Wenn die PIN die Verbindung wiederherstellen kann, während der Filter aktiv ist, wird diese Methode mit dem Wert " **true**" aufgerufen. Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




