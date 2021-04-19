---
description: Die inaktive Methode beendet den Arbeits Thread, der Daten aus der Ausgabe-PIN abruft. Mit dieser Methode wird auch der Zuweiser decommittet.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Cpullpin. inaktive Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367739"
---
# <a name="cpullpininactive-method"></a>Cpullpin. inaktive Methode

Die- `Inactive` Methode beendet den Arbeits Thread, der Daten aus der Ausgabe-PIN abruft. Mit dieser Methode wird auch der Zuweiser decommittet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode auf, wenn der besitzende Filter inaktiv wird. (Wenn Ihre Eingabe-PIN von [**cbasepin**](cbasepin.md)abgeleitet ist, überschreiben Sie die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




