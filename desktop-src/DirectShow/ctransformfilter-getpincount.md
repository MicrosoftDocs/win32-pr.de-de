---
description: Die getpincount-Methode ruft die Anzahl der Pins für den Filter ab.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Ctransformfilter. getpincount-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371680"
---
# <a name="ctransformfiltergetpincount-method"></a>Ctransformfilter. getpincount-Methode

Die- `GetPinCount` Methode ruft die Anzahl der Pins für den Filter ab.

## <a name="syntax"></a>Syntax


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 2 zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasefilter:: getpincount**](cbasefilter-getpincount.md) -Methode. Die **ctransformfilter** -Klasse unterstützt genau eine Eingabe-PIN und eine Ausgabe-PIN.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




