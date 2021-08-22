---
description: Die NotReady-Methode signalisiert, dass ein Zustandsübergang noch nicht abgeschlossen ist.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: CBaseRenderer.NotReady-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52fddcbd92544a109340697e5865f87e6c5f74a14b01543e768495b7717d8f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954829"
---
# <a name="cbaserenderernotready-method"></a>CBaseRenderer.NotReady-Methode

Die `NotReady` -Methode signalisiert, dass ein Zustandsübergang noch nicht abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
void NotReady();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode bewirkt, dass die [**CBaseRenderer::GetState-Methode**](cbaserenderer-getstate.md) VFW \_ S STATE INTERMEDIATE \_ zurückgibt, was \_ angibt, dass der Filter noch in den aktuellen Zustand übergehen wird. Der Filter ruft diese Methode auf, wenn ein Zustandsübergang aussteht. (Dies tritt auf, wenn der Filter angehalten wird, bis er ein Beispiel empfängt.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> <dt>

[**CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**Bereit**](cbaserenderer-ready.md)
</dt> </dl>

 

 




