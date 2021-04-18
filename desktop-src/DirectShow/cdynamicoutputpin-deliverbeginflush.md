---
description: Die deliverbeginflush-Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu starten.
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Cdynamicoutputpin. deliverbeginflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242394a327b63fcc901b08f572096bf2f42238b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371120"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a>Cdynamicoutputpin. deliverbeginflush-Methode

Die- `DeliverBeginFlush` Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu starten.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbaseoutputpin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) -Methode. Das Ereignis [**cdynamicoutputpin:: m \_ hstopevent**](cdynamicoutputpin-m-hstopevent.md) wird festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




