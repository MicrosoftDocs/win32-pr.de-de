---
description: Die Pause-Methode signalisiert, dass der streamingingthread aktiv wird.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Csourcestream. Pause-Methode (Quelle. h)
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
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371441"
---
# <a name="csourcestreampause-method"></a>Csourcestream. Pause-Methode

Die- `Pause` Methode signalisiert, dass der streamingingthread aktiv wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ OK oder E \_ unerwartet zurück.

## <a name="remarks"></a>Bemerkungen

Die [**csourcestream:: Active**](csourcestream-active.md) -Methode ruft diese Methode auf. Wenn die [**csourcestream:: ThreadProc**](csourcestream-threadproc.md) -Methode diese Anforderung empfängt, ruft Sie die [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




