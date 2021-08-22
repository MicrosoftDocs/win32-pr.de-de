---
description: Die Inaktive Methode fährt den Arbeitsthread herunter, der Daten vom Ausgabepin pullt. Diese Methode decommitiert auch die Zuweisung.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: CPullPin.Inactive-Methode (Pullpin.h)
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
ms.openlocfilehash: 56307362651761dbe2bc5c0242a24f189cf14d1e820df6a5ba21bdeb9c7deb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565370"
---
# <a name="cpullpininactive-method"></a>CPullPin.Inactive-Methode

Die `Inactive` -Methode fährt den Arbeitsthread herunter, der Daten vom Ausgabepin pullt. Diese Methode decommitiert auch die Zuweisung.

## <a name="syntax"></a>Syntax


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode auf, wenn der besitzende Filter inaktiv wird. (Wenn Ihr Eingabepin von [**CBasePin**](cbasepin.md)stammt, überschreiben Sie die [**CBasePin::Inactive-Methode.)**](cbasepin-inactive.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




