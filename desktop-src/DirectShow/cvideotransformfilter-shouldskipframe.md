---
description: Die ShouldSkipFrame-Methode bestimmt, ob der Filter ein angegebenes Beispiel ablegen soll.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: CVideoTransformFilter.ShouldSkipFrame-Methode (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26a0c35be9914641abfa053cd1ee00f46bb09222aecbebc55d45900331a2ee81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075940"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a>CVideoTransformFilter.ShouldSkipFrame-Methode

Die `ShouldSkipFrame` -Methode bestimmt, ob der Filter ein angegebenes Beispiel ablegen soll.

## <a name="syntax"></a>Syntax


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pin* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn der Filter dieses Beispiel ablegen soll, oder **FALSE,** wenn der Filter dieses Beispiel verarbeiten soll.

## <a name="remarks"></a>Hinweise

Diese Methode gibt **TRUE zurück,** wenn die folgenden Bedingungen erfüllt sind:

-   Das Beispiel verfügt über Zeitstempel.
-   Die durchschnittliche Decodierungszeit beträgt mindestens 25 % der Framedauer.
-   Der Renderer hat derzeit mindestens einen Frame zu spät, wie durch Qualitätsmeldungen gemeldet.
-   Das Überspringen auf den nächsten Keyframe würde nicht dazu führen, dass der Frame früh mehr als einen Frame erreicht.

Für diese Berechnung zeichnet der Filter beim Verarbeiten von Daten die folgenden Informationen auf:

-   Die durchschnittliche Decodierungszeit in den letzten 20 Frames (**m \_ itrAvgDecode**)
-   Die Anzahl der Frames seit dem letzten Keyframe (**m \_ nFramesSinceKeyFrame**)
-   Eine Schätzung, wie viele Frames sich zwischen Keyframes befinden (**m \_ nKeyFramePeriod**)

Sobald der Filter einen Frame abstürzt, werden Frames so lange abfällt, bis er den nächsten Keyframe erreicht. Wenn diese Methode **TRUE zurückgibt,** sendet sie auch ein [**EC QUALITY \_ \_ CHANGE-Ereignis**](ec-quality-change.md) an den Filter Graph Manager.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans.h (einschließlich Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CVideoTransformFilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




