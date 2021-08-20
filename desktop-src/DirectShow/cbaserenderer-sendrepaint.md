---
description: Die SendRepaint-Methode sendet ein Repaint-Ereignis an den Filterdiagramm-Manager.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: CBaseRenderer.SendRepaint-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9057d1ff733c30da3b3b0d7e960607eadd033dcee0b26994478c6da9156a183e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954789"
---
# <a name="cbaserenderersendrepaint-method"></a>CBaseRenderer.SendRepaint-Methode

Die `SendRepaint` -Methode sendet ein repaint-Ereignis an den Filterdiagramm-Manager.

## <a name="syntax"></a>Syntax


```C++
void SendRepaint();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode sendet ein [**EC \_ REPAINT-Ereignis**](ec-repaint.md) an den Filterdiagramm-Manager, wenn die folgenden Bedingungen erfüllt sind:

-   Der Eingabepin ist verbunden.
-   Der Filter leert keine Daten.
-   Das Ende des Streams wurde nicht erreicht.
-   Das [**Flag CBaseRenderer::m \_ bAbort**](cbaserenderer-m-babort.md) ist **FALSE.**
-   Das [**CBaseRenderer::m \_ bRepaintStatus-Flag**](cbaserenderer-m-brepaintstatus.md) ist **TRUE.**

Abhängig vom Zustand des Diagramms kann das EC REPAINT-Ereignis dazu führen, dass der Upstreamfilter ein Beispiel erneut sendet, das Filterdiagramm an seine aktuelle Position sucht oder dass der Filterdiagramm-Manager kurz angehalten \_ wird. (Siehe [**EC \_ REPAINT**](ec-repaint.md).) Dieses Ereignis ist möglicherweise ineffizient, daher sollte es nur wenig verwendet werden. Videorenderer müssen die Anzeige jedoch manchmal aktualisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




