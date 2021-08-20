---
description: Die OnDisplayChange-Methode veröffentlicht ein EC \_ DISPLAY \_ CHANGED-Ereignis an den Filtergraph-Manager.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: CBaseRenderer.OnDisplayChange-Methode (Renbase.h)
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
ms.openlocfilehash: 3f7fc5d733d90ab88f1114558947b6e72958c1d8b18d507ce612c1865fc400e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016878"
---
# <a name="cbaserendererondisplaychange-method"></a>CBaseRenderer.OnDisplayChange-Methode

Die `OnDisplayChange` -Methode veröffentlicht ein [**EC DISPLAY \_ \_ CHANGED-Ereignis**](ec-display-changed.md) an den Filterdiagramm-Manager.

## <a name="syntax"></a>Syntax


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn das Ereignis gesendet wurde, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Videorenderer sollten diese Methode als Reaktion auf WM \_ DISPLAYCHANGE-Meldungen aufrufen. Wenn der Eingabepin verbunden ist, sendet die Methode ein EC \_ DISPLAY \_ CHANGED-Ereignis an den Filtergraph-Manager.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




