---
description: Die Methode canreconnect-aktiv fragt ab, ob die PIN dynamische erneute Verbindungen unterstützt.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Cbasepin. canreconnect-Active-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367724"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>Cbasepin. canreconnect-Active-Methode

Die- `CanReconnectWhenActive` Methode fragt ab, ob die PIN dynamische erneute Verbindungen unterstützt.

## <a name="syntax"></a>Syntax


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob die PIN dynamisch erneut eine Verbindung herstellen kann. **True** gibt an, dass die PIN dynamisch erneut eine Verbindung herstellen kann.

## <a name="remarks"></a>Bemerkungen

Standardmäßig müssen Sie einen Filter vor dem erneuten Verbinden der Pins abbrechen. Wenn eine PIN eine dynamische erneute Verbindung unterstützt, kann Sie die Verbindung wiederherstellen, während der Filter aktiv ist. Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




