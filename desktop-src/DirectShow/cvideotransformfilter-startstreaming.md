---
description: 'Die startstreaming-Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt. Diese Methode überschreibt die ctransformfilter:: startstreaming-Methode.'
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Cvideotransformfilter. startstreaming-Methode (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366910"
---
# <a name="cvideotransformfilterstartstreaming-method"></a>Cvideotransformfilter. startstreaming-Methode

Die- `StartStreaming` Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt. Diese Methode überschreibt die [**ctransformfilter:: startstreaming**](ctransformfilter-startstreaming.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode setzt alle Leistungsstatistiken zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cvideotransformfilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




