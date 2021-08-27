---
description: Die Receive-Methode empfängt das nächste Medienbeispiel im Stream.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: CBaseRenderer.Receive-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe440b7ac0c7b05c2d3cf9d7ca2019a788e272b7aca6acd6a747738a255ca39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131440"
---
# <a name="cbaserendererreceive-method"></a>CBaseRenderer.Receive-Methode

Die `Receive` -Methode empfängt das nächste Medienbeispiel im Stream.

## <a name="syntax"></a>Syntax


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Der Eingabepin ruft diese Methode auf, wenn sie ein Beispiel vom Upstreamfilter empfängt.

Wenn der Filter ausgeführt wird, führt diese Methode die folgenden Schritte aus:

1.  Plant das Beispiel für das Rendering ([**CBaseRenderer::P repareReceive**](cbaserenderer-preparereceive.md)).
2.  Wartet auf die geplante Zeit ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).
3.  Rendert das Beispiel ([**CBaseRenderer::Render**](cbaserenderer-render.md)).
4.  Gibt das Beispiel frei ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).

Wenn der Filter angehalten wird, führt die -Methode die folgenden Schritte aus:

1.  Benachrichtigt die abgeleitete Klasse, dass ein Beispiel verfügbar ist ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).
2.  Wartet auf die geplante Zeit.
3.  Rendert das Beispiel.
4.  Gibt das Beispiel frei.

Während die Methode angehalten wurde, wartet sie in Schritt 2, bis der Filter in den Ausführungszustand wechselt. An diesem Punkt plant der Filter das Beispiel.

In der Basisklasse führt die **OnReceiveFirstSample-Methode** nichts aus. Die abgeleitete Klasse kann sie überschreiben. Wenn beispielsweise ein Videorenderer angehalten wird, wird das erste Beispiel als Standbild angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




