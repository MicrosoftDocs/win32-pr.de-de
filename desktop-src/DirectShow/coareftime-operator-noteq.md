---
description: Dieser Operator testet auf Ungleichheit zwischen zwei Verweis Zeiten.
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: Coaref time. Operator! =-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e93934d7b31715422f2cc091e606b681a57e7f61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367698"
---
# <a name="coareftimeoperator-method"></a>Coaref time. Operator! =-Methode

Dieser Operator testet auf Ungleichheit zwischen zwei Verweis Zeiten.

## <a name="syntax"></a>Syntax


```C++
BOOL operator!=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RT* \[ atur\]
</dt> <dd>

Verweis auf das **coareftime** -Objekt, das verglichen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die beiden-Objekte nicht gleich sind. Andernfalls wird **false** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coaref Time-Klasse**](coareftime.md)
</dt> </dl>

 

 




