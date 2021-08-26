---
description: Dieser Operator multipliziert eine Verweiszeit mit einem Wert.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: COARefTime.operator*-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57060f3b0436422c34ba947c0025cc6796d534e16ff64be029e68ab140faa4af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079350"
---
# <a name="coareftimeoperator-method"></a>COARefTime.operator-Methode \*

Dieser Operator multipliziert eine Verweiszeit mit einem Wert.

## <a name="syntax"></a>Syntax


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*l* 
</dt> <dd>

Multiplikator.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein neues **COARefTime-Objekt** zurück, das dem Produkt dieses Objekts und **l** entspricht.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COARefTime-Klasse**](coareftime.md)
</dt> </dl>

 

 




