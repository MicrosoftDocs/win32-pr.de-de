---
description: Die ondisplaychange-Methode stellt ein angezeigter EC- \_ Anzeige \_ Ereignis an den Filter Diagramm-Manager.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Cbaserenderer. ondisplaychange-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364543"
---
# <a name="cbaserendererondisplaychange-method"></a>Cbaserenderer. ondisplaychange-Methode

Die-Methode stellt ein angezeigter `OnDisplayChange` [**EC- \_ Anzeige \_**](ec-display-changed.md) Ereignis an den Filter Diagramm-Manager.

## <a name="syntax"></a>Syntax


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn das Ereignis gepostet wurde, andernfalls " **false** ".

## <a name="remarks"></a>Bemerkungen

Videorenderer sollten diese Methode als Reaktion auf WM \_ Display Change-Nachrichten aufruft. Wenn die eingabepin verbunden ist, sendet die Methode \_ ein \_ geändertes Ereignis der EC-Anzeige an den Filter Diagramm-Manager.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




