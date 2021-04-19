---
description: Die Duration-Methode ruft die Dauer des Streams ab.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Cpullpin. Duration-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367740"
---
# <a name="cpullpinduration-method"></a>Cpullpin. Duration-Methode

Die- `Duration` Methode ruft die Dauer des Streams ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptduration* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Dauer (in Bytes multipliziert mit 10 Millionen) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die Dauer ist unbestimmt, bis die [**cpullpin:: Connect**](cpullpin-connect.md) -Methode aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




