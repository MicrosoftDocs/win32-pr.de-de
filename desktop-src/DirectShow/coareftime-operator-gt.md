---
description: Dieser Operator testet, ob eine Verweiszeit größer als eine andere ist.
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: COARefTime.operator>-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fd2da8b95345813682994f18a444f090c65c1f906219afb9a64bf5584679b194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652190"
---
# <a name="coareftimeoperator-method"></a>COARefTime.operator>-Methode

Dieser Operator testet, ob eine Verweiszeit größer als eine andere ist.

## <a name="syntax"></a>Syntax


```C++
BOOL operator>(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Verweis auf das zu vergleichende **COARefTime-Objekt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn dieses Objekt streng größer als *rt* ist. Andernfalls gibt **FALSE** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COARefTime-Klasse**](coareftime.md)
</dt> </dl>

 

 




