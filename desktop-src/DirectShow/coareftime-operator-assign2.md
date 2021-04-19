---
description: Der-Operator weist eine neue Verweis Zeit zu und verwendet den ' rt [REF] '-Parameter.
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: Coaref time. Operator = Method (ctlutil. h)-RT [REF]-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106364017"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a>Coaref time. Operator = Method (ctlutil. h)-RT [REF]-Parameter

Dieser Operator weist eine neue Bezugszeit zu.

## <a name="syntax"></a>Syntax


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RT* \[ atur\]
</dt> <dd>

Verweis auf einen [**Verweis \_ Zeitwert**](reference-time.md) , der die neue Verweis Zeit in 100-Nanosecond-Einheiten angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Verweis auf das-Objekt zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung                    | Wert                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Ctlutil. h (Include Streams. h)                                                                                   |
| Bibliothek | "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coaref Time-Klasse**](coareftime.md)
</dt> </dl>

 

 




