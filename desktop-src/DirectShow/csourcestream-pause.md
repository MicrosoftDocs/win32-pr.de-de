---
description: Die Pause-Methode signalisiert dem Streamingthread, dass er aktiv wird.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: CSourceStream.Pause-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454f6e64461c036e9e3d9ef2f13033e5a210d783f3f6b734b7137a99b16402c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079310"
---
# <a name="csourcestreampause-method"></a>CSourceStream.Pause-Methode

Die `Pause` -Methode signalisiert dem Streamingthread, dass er aktiv wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E UNEXPECTED \_ zurück.

## <a name="remarks"></a>Hinweise

Die [**CSourceStream::Active-Methode**](csourcestream-active.md) ruft diese Methode auf. Wenn die [**CSourceStream::ThreadProc-Methode**](csourcestream-threadproc.md) diese Anforderung empfängt, ruft sie die [**CSourceStream::D oBufferProcessingLoop-Methode**](csourcestream-dobufferprocessingloop.md) auf.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




