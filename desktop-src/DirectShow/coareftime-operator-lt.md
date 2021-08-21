---
description: Dieser Operator testet, ob eine Verweiszeit kleiner als eine andere ist.
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: COARefTime.operator<-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d98c80e33cebabb868785d1df4d78ca038963683af5d778386ba0d85432e0e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073834"
---
# <a name="coareftimeoperator-method"></a>COARefTime.operator<-Methode

Dieser Operator testet, ob eine Verweiszeit kleiner als eine andere ist.

## <a name="syntax"></a>Syntax


```C++
BOOL operator<(
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

Gibt **TRUE** zurück, wenn dieses Objekt streng kleiner als *rt* ist. Andernfalls gibt **FALSE** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COARefTime-Klasse**](coareftime.md)
</dt> </dl>

 

 




