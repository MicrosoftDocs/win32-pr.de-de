---
description: Die Methode "schuldskipframe" bestimmt, ob der Filter eine angegebene Stichprobe löschen soll.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Cvideotransformfilter. schuldskipframe-Methode (vtrans. h)
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
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357561"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a>Cvideotransformfilter. schuldskipframe-Methode

Die- `ShouldSkipFrame` Methode bestimmt, ob der Filter eine angegebene Stichprobe löschen soll.

## <a name="syntax"></a>Syntax


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*kehren* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn der Filter dieses Beispiel löschen soll, oder " **false** ", wenn der Filter dieses Beispiel verarbeiten soll.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt " **true** " zurück, wenn die folgenden Bedingungen erfüllt sind:

-   Das Beispiel enthält Zeitstempel.
-   Die durchschnittliche Decodierungs Zeit beträgt mindestens 25% der Rahmen Dauer.
-   Der Renderer ist zurzeit mindestens ein Frame spät, wie er über Qualitäts Meldungen gemeldet wird.
-   Das überspringen zum nächsten Keyframe bewirkt nicht, dass der Frame frühzeitig mehr als einen Frame antrifft.

Im Rahmen dieser Berechnung zeichnet der Filter bei der Verarbeitung von Daten die folgenden Informationen auf:

-   Die durchschnittliche Decodierungs Zeit in den letzten 20 Frames (**m \_ itravgdecode**)
-   Die Anzahl der Frames seit dem letzten **Keyframe (m \_ nframessincekeyframe**).
-   Eine Schätzung der Anzahl von Frames zwischen **\_ Keyframes (m nkeyframeperiod**)

Nachdem der Filter einen Frame gelöscht hat, wird er fortgesetzt, bis er den nächsten Keyframe erreicht. Wenn diese Methode **true** zurückgibt, sendet Sie auch ein [**EC- \_ Qualitäts \_ Änderungs**](ec-quality-change.md) Ereignis an den Filter Graph-Manager.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cvideotransformfilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




