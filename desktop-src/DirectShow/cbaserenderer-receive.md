---
description: Die Receive-Methode empfängt das nächste Medien Beispiel im Stream.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Cbaserderderer. Receive-Methode (renbase. h)
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
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372517"
---
# <a name="cbaserendererreceive-method"></a>Cbaserderderer. Receive-Methode

Die- `Receive` Methode empfängt das nächste Medien Beispiel im Stream.

## <a name="syntax"></a>Syntax


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN ruft diese Methode auf, wenn Sie ein Beispiel aus dem upstreamfilter empfängt.

Wenn der Filter ausgeführt wird, führt diese Methode die folgenden Schritte aus:

1.  Plant das Beispiel für das Rendering ([**cbaserenderer::P**](cbaserenderer-preparereceive.md)Analyse).
2.  Wartet auf die geplante Zeit ([**cbaserenderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md)).
3.  Rendert das Beispiel ([**cbaserenderer:: Rendering**](cbaserenderer-render.md)).
4.  Gibt das Beispiel ([**cbaserderderer:: clearpdingsample**](cbaserenderer-clearpendingsample.md)) frei.

Wenn der Filter angehalten ist, führt die-Methode die folgenden Schritte aus:

1.  Benachrichtigt die abgeleitete-Klasse, dass eine Stichprobe verfügbar ist ([**cbasererderderer:: onreceivefirstsample**](cbaserenderer-onreceivefirstsample.md)).
2.  Wartet auf die geplante Zeit.
3.  Rendert das Beispiel.
4.  Gibt das Beispiel frei.

Obwohl die-Methode angehalten wurde, wartet Sie in Schritt 2, bis der Filter in den Status wird ausgeführt wechselt. An diesem Punkt plant der Filter das Beispiel.

In der Basisklasse führt die **onreceivefirstsample** -Methode keine Aktion aus. Diese kann von der abgeleiteten Klasse überschrieben werden. Wenn ein Videorenderer z. b. angehalten wird, wird das erste Beispiel als Bild angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




