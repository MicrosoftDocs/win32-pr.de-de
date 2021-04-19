---
description: Die deliverendflush-Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu beenden.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Cdynamicoutputpin. deliverendflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2666681dcd5637a8e919ced2c61d6536663d7b30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367546"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>Cdynamicoutputpin. deliverendflush-Methode

Die- `DeliverEndFlush` Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu beenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbaseoutputpin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) -Methode. Das Ereignis [**cdynamicoutputpin:: m \_ hstopevent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




