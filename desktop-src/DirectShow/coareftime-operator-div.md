---
description: Dieser Operator dividiert eine Verweiszeit durch einen -Wert.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: COARefTime.operator/-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ff5f23691a3c4c44fdb9b93006834913648391ed473cf84906dff3eb8afb21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566020"
---
# <a name="coareftimeoperator-method"></a>COARefTime.operator/-Methode

Dieser Operator dividiert eine Verweiszeit durch einen -Wert.

## <a name="syntax"></a>Syntax


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*l* 
</dt> <dd>

Divisor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein neues **COARefTime-Objekt** zurück, das dem Quotienten dieses Objekts und **l entspricht.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COARefTime-Klasse**](coareftime.md)
</dt> </dl>

 

 




