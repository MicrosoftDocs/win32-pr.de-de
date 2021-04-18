---
description: Die Methode "Methode" aktiviert oder deaktiviert Repaint-Ereignisse.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Cbasererererer. abtrepaintstatus-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364465"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>Cbasererererer. abtrepaintstatus-Methode

Die- `SetRepaintStatus` Methode aktiviert oder deaktiviert Repaint-Ereignisse.

## <a name="syntax"></a>Syntax


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*brepaint* 
</dt> <dd>

Boolescher Wert, der angibt, ob Repaint-Ereignisse aktiviert sind. **True** gibt an, dass der Filter [**EC \_ Repaint**](ec-repaint.md) -Ereignisse an den Filter Graph-Manager sendet. Andernfalls werden keine EC- \_ Repaint-Ereignisse gesendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode stellt sicher, dass der Filter Graph-Manager nicht mit redundanten EC Repaint-Ereignissen überflutet wird \_ . Nachdem der Filter ein [**EC \_ Repaint**](ec-repaint.md) -Ereignis gesendet hat, wird diese Methode mit dem Wert " **true**" aufgerufen. Der Filter sendet keine weiteren EC \_ Repaint-Ereignisse, bis mehr Daten empfangen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




