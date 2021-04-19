---
description: Ruft das nächste Element aus der Warteschlange ab.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Cqueue. getqueueobject-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356025"
---
# <a name="cqueuegetqueueobject-method"></a>Cqueue. getqueueobject-Methode

Ruft das nächste Element aus der Warteschlange ab.

## <a name="syntax"></a>Syntax


```C++
T GetQueueObject();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein Objekt vom Typ **T** zurück (den Vorlagentyp).

## <a name="remarks"></a>Bemerkungen

Diese Methode wird blockiert, bis ein Element in der Warteschlange verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cqueue-Klasse**](cqueue.md)
</dt> </dl>

 

 




