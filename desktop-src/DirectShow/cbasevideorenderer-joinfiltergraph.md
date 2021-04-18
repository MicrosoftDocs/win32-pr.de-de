---
description: Die joinfiltergraph-Methode sendet \_ eine Ereignis Benachrichtigung für das EC-Fenster, \_ Wenn ein Filter aus dem Filter Diagramm entfernt wird.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Cbasevideorenderer. joinfiltergraph-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365680"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>Cbasevideorenderer. joinfiltergraph-Methode

Die- `JoinFilterGraph` Methode sendet eine Ereignis Benachrichtigung für das [**EC- \_ \_ Fenster**](ec-window-destroyed.md) , wenn ein Filter aus dem Filter Diagramm entfernt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PGraph* 
</dt> <dd>

Zeiger auf das Filter Diagramm, das verknüpft werden soll.

</dd> <dt>

*PName* \[ in\]
</dt> <dd>

Zeiger auf den Namen des hinzugefügten Filters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion überschreibt die [**cbasefilter:: joinfiltergraph**](cbasefilter-joinfiltergraph.md) -Member-Funktion. Wenn der Filter das Filter Diagramm verlässt (*PGraph* ist **null**), wird eine Ereignis Benachrichtigung für ein [**EC- \_ Fenster \_**](ec-window-destroyed.md) gesendet, sodass der Ressourcen-Manager den Renderer nicht als Fokus Objekt speichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




