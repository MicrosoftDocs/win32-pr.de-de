---
description: Die notready-Methode signalisiert, dass ein Zustandsübergang noch nicht beendet ist.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Cbaserderderer. notready-Methode (renbase. h)
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
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367195"
---
# <a name="cbaserenderernotready-method"></a>Cbaserderderer. notready-Methode

Die- `NotReady` Methode signalisiert, dass ein Zustandsübergang noch nicht beendet ist.

## <a name="syntax"></a>Syntax


```C++
void NotReady();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode bewirkt, dass die [**cbaserenderer:: GetState**](cbaserenderer-getstate.md) -Methode VFW \_ S \_ State Intermediate zurückgibt \_ , wodurch angegeben wird, dass der Filter weiterhin in seinen aktuellen Zustand übergeht. Der Filter ruft diese Methode auf, wenn ein Zustandsübergang aussteht. (Dies tritt auf, wenn der Filter angehalten wird, bis er ein Beispiel empfängt.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> <dt>

[**Prüfbereit**](cbaserenderer-checkready.md)
</dt> <dt>

[**Bereit**](cbaserenderer-ready.md)
</dt> </dl>

 

 




