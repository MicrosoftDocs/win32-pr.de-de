---
description: Die SetRepaintStatus-Methode aktiviert oder deaktiviert Neupaintereignisse.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: CBaseRenderer.SetRepaintStatus-Methode (Renbase.h)
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
ms.openlocfilehash: 748d0091bd3d2eae11773a9f94b62ceeb92b2d3ca64049f1a1981e38bf222e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016848"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>CBaseRenderer.SetRepaintStatus-Methode

Die `SetRepaintStatus` -Methode aktiviert oder deaktiviert Neupaintereignisse.

## <a name="syntax"></a>Syntax


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bRepaint* 
</dt> <dd>

Boolescher Wert, der angibt, ob neu gepaint-Ereignisse aktiviert sind. True **gibt an,** dass der Filter [**EC \_ REPAINT-Ereignisse**](ec-repaint.md) an den Filterdiagramm-Manager gesendet hat. Andernfalls werden keine EC \_ REPAINT-Ereignisse gesendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode stellt sicher, dass der Filterdiagramm-Manager nicht mit redundanten EC \_ REPAINT-Ereignissen überflutet wird. Nachdem der Filter ein [**EC \_ REPAINT-Ereignis**](ec-repaint.md) sendet, ruft er diese Methode mit dem Wert **TRUE auf.** Der Filter sendet erst dann mehr EC \_ REPAINT-Ereignisse, wenn er mehr Daten empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




