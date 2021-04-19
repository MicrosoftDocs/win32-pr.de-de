---
description: Die startstreaming-Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: Ctransformfilter. startstreaming-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50df2db2aada7f96744af5e553f474818594d399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361401"
---
# <a name="ctransformfilterstartstreaming-method"></a>Ctransformfilter. startstreaming-Methode

Die- `StartStreaming` Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode führt keine Aktion in der Basisklasse durch, aber die abgeleitete Klasse kann Sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




