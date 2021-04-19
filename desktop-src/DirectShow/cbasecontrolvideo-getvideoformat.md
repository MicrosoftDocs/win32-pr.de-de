---
description: Die getvideoformat-Methode ruft ein Video Beispiel ab, das das aktuelle Videoformat darstellt.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Cbasecontrolvideo. getvideoformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370780"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a>Cbasecontrolvideo. getvideoformat-Methode

Die- `GetVideoFormat` Methode ruft ein Video Beispiel ab, das das aktuelle Videoformat darstellt.

## <a name="syntax"></a>Syntax


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur zurück, die das aktuelle Videoformat enthält.

## <a name="remarks"></a>Bemerkungen

Um bestimmte Informationen über [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)zurückzugeben und zu überprüfen, muss das Objekt das aktuelle Videoformat kennen. Diese Informationen werden abgerufen, indem diese reine virtuelle Methode aufgerufen wird, die von abgeleiteten Klassen überschrieben werden muss. Diese Member-Funktion wird von den folgenden [**cbasecontrolvideo**](cbasecontrolvideo.md) -Element Funktionen aufgerufen.

-   [**Cbasecontrolvideo:: onvideosizechange**](cbasecontrolvideo-onvideosizechange.md)
-   [**Cbasecontrolvideo:: \_ avgtimeperframe abrufen**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**Cbasecontrolvideo:: get- \_ Bitrate**](cbasecontrolvideo-get-bitrate.md)
-   [**Cbasecontrolvideo:: get \_ biterrorrate**](cbasecontrolvideo-get-biterrorrate.md)
-   [**Cbasecontrolvideo:: get \_ videowidth**](cbasecontrolvideo-get-videowidth.md)
-   [**Cbasecontrolvideo:: get \_ videoheight**](cbasecontrolvideo-get-videoheight.md)
-   [**Cbasecontrolvideo:: getvideopaletteentries**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**Cbasecontrolvideo:: getvideosize**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




