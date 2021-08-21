---
description: Die StartStreaming-Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: CTransformFilter.StartStreaming-Methode (Transfrm.h)
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
ms.openlocfilehash: 6d4a0c6e0e047819c208c8e592b971f013f9ed40d456a5b73ad64ea9153ddeaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953429"
---
# <a name="ctransformfilterstartstreaming-method"></a>CTransformFilter.StartStreaming-Methode

Die `StartStreaming` -Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




