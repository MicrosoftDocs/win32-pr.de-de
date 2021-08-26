---
description: Die GetVideoFormat-Methode ruft ein Videobeispiel ab, das das aktuelle Videoformat darstellt.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: CBaseControlVideo.GetVideoFormat-Methode (Ctlutil.h)
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
ms.openlocfilehash: e37a59b8d002a9c081de74c4974dca1f86d1c9d0a5f7f7b0caca11be6c026d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052770"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a>CBaseControlVideo.GetVideoFormat-Methode

Die `GetVideoFormat` -Methode ruft ein Videobeispiel ab, das das aktuelle Videoformat darstellt.

## <a name="syntax"></a>Syntax


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) zurück, die das aktuelle Videoformat enthält.

## <a name="remarks"></a>Hinweise

Um bestimmte Informationen über [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)zurück- und zu überprüfen, muss das Objekt das aktuelle Videoformat kennen. Sie ruft diese Informationen ab, indem diese reine virtuelle Methode, die abgeleitete Klassen überschreiben müssen, aufruft. Diese Memberfunktion wird von den folgenden [**CBaseControlVideo-Memberfunktionen**](cbasecontrolvideo.md) aufgerufen.

-   [**CBaseControlVideo::OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)
-   [**CBaseControlVideo::get \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**CBaseControlVideo::get \_ BitRate**](cbasecontrolvideo-get-bitrate.md)
-   [**CBaseControlVideo::get \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)
-   [**CBaseControlVideo::get \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)
-   [**CBaseControlVideo::get \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)
-   [**CBaseControlVideo::GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**CBaseControlVideo::GetVideoSize**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




