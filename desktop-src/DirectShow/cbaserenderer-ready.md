---
description: Die Ready-Methode signalisiert, dass ein Zustandsübergang abgeschlossen ist.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Cbaserderderer. Ready-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369280"
---
# <a name="cbaserendererready-method"></a>Cbaserderderer. Ready-Methode

Die- `Ready` Methode signalisiert, dass ein Zustandsübergang beendet ist.

## <a name="syntax"></a>Syntax


```C++
void Ready();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode bewirkt, dass die [**cbasergetderer:: GetState**](cbaserenderer-getstate.md) -Methode "S OK" zurückgibt \_ , was bedeutet, dass der Filter den Übergang in seinen aktuellen Zustand abgeschlossen hat. Der Filter ruft diese Methode immer dann auf, wenn Sie einen Zustandsübergang abschließt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> <dt>

[**Cbaserererderer:: checkready**](cbaserenderer-checkready.md)
</dt> <dt>

[**Cbaserderderer:: notready**](cbaserenderer-notready.md)
</dt> </dl>

 

 




