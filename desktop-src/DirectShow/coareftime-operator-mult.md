---
description: Dieser Operator multipliziert eine Verweis Zeit mit einem Wert.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Coaref time. Operator *-Methode (ctlutil. h)
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
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365684"
---
# <a name="coareftimeoperator-method"></a>Coaref time. Operator- \* Methode

Dieser Operator multipliziert eine Verweis Zeit mit einem Wert.

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

Gibt ein neues **coareftime** -Objekt zurück, das dem Produkt dieses Objekts und **l** entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coaref Time-Klasse**](coareftime.md)
</dt> </dl>

 

 




