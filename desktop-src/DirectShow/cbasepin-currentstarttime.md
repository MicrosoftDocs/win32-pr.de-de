---
description: 'Die currentstarttime-Methode ruft die Segment Start Zeit ab, die von der cbasepin:: newsegment-Methode festgelegt wird.'
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: Cbasepin. currentstarttime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f413419992d66f8de3a28bb7e39368564ce0803
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358799"
---
# <a name="cbasepincurrentstarttime-method"></a>Cbasepin. currentstarttime-Methode

Die- `CurrentStartTime` Methode ruft die Segment Start Zeit ab, die von der [**cbasepin:: newsegment**](cbasepin-newsegment.md) -Methode festgelegt wird.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von [**cbasepin:: m \_ tSTART**](cbasepin-m-tstart.md)zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




