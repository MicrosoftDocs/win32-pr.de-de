---
description: Die sendrepaint-Methode sendet ein Repaint-Ereignis an den Filter Graph-Manager.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Cbaserderderer. sendrepaint-Methode (renbase. h)
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
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365495"
---
# <a name="cbaserenderersendrepaint-method"></a>Cbaserderderer. sendrepaint-Methode

Die- `SendRepaint` Methode sendet ein Repaint-Ereignis an den Filter Graph-Manager.

## <a name="syntax"></a>Syntax


```C++
void SendRepaint();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode sendet ein [**EC \_ Repaint**](ec-repaint.md) -Ereignis an den Filter Graph-Manager, wenn die folgenden Bedingungen zutreffen:

-   Die eingabepin ist verbunden.
-   Der Filter gibt keine Daten aus.
-   Das Ende des Streams wurde nicht erreicht.
-   Das [**cbaserderderer:: m \_ babort**](cbaserenderer-m-babort.md) -Flag ist **false**.
-   Das Flag " [**cbaserderderer:: m \_ brepaintstatus**](cbaserenderer-m-brepaintstatus.md) " ist " **true**".

Abhängig vom Status des Diagramms kann das EC \_ Repaint-Ereignis bewirken, dass der upstreamfilter eine Stichprobe erneut sendet, das Filter Diagramm, um den aktuellen Speicherort zu suchen, oder den Filter-Graph-Manager, um vorübergehend anzuhalten. (Siehe [**EC \_ Repaint**](ec-repaint.md).) Dieses Ereignis ist potenziell ineffizient und sollte daher sparsam verwendet werden. Videorenderer müssen jedoch manchmal die Anzeige aktualisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




