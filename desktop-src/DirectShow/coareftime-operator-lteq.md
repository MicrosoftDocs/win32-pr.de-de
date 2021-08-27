---
description: Dieser Operator testet, ob eine Verweiszeit größer oder gleich einer anderen ist.
ms.assetid: 1182db5b-2d58-4abb-b9ec-f14c3de5a942
title: COARefTime.operator<= methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 448f36a9c746c22878d8bb0e48028dff211962cbf49827eab3c14f2b4af6b38c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087280"
---
# <a name="coareftimeoperator-method"></a>COARefTime.operator<= methode

Dieser Operator testet, ob eine Verweiszeit größer oder gleich einer anderen ist.

## <a name="syntax"></a>Syntax


```C++
BOOL operator<=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Verweis auf das **zu vergleichende COARefTime-Objekt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn dieses Objekt größer oder gleich *rt ist.* Andernfalls wird **FALSE zurückgegeben.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COARefTime-Klasse**](coareftime.md)
</dt> </dl>

 

 




