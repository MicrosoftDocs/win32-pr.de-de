---
description: Dieser Operator testet, ob eine Verweis Zeit kleiner als oder gleich einem anderen ist.
ms.assetid: ae7449b7-d319-4e76-892f-0f9ae63ddf94
title: Coaref time. Operator>=-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69b345f42c854e939c21a028827889a03e0ce735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365519"
---
# <a name="coareftimeoperator-method"></a>Coaref time. Operator>=-Methode

Dieser Operator testet, ob eine Verweis Zeit kleiner als oder gleich einem anderen ist.

## <a name="syntax"></a>Syntax


```C++
BOOL operator>=(
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

Gibt **true** zurück, wenn dieses Objekt kleiner oder gleich *RT* ist. Andernfalls wird **false** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coaref Time-Klasse**](coareftime.md)
</dt> </dl>

 

 




