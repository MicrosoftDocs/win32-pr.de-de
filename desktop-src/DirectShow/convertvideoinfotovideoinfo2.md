---
description: Die ConvertVideoInfoToVideoInfo2-Funktion konvertiert einen Medientyp, der VIDEOINFOHEADER verwendet, in einen Medientyp, der VIDEOINFOHEADER2 verwendet.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: ConvertVideoInfoToVideoInfo2-Funktion (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f1865652edf01a612ba7d1a46520f92a8461c9ba53a80395e27e6252e0018ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073764"
---
# <a name="convertvideoinfotovideoinfo2-function"></a>ConvertVideoInfoToVideoInfo2-Funktion

Die `ConvertVideoInfoToVideoInfo2` Funktion konvertiert einen Medientyp, der [**VIDEOINFOHEADER verwendet,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) in einen Medientyp, der [**VIDEOINFOHEADER2 verwendet.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)

## <a name="syntax"></a>Syntax


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf die [**zu konvertierende AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Die -Struktur muss den Formattyp FORMAT \_ VideoInfo haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ OUTOFMEMORY zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion weist eine neue **VIDEOINFOHEADER2-Struktur** zu, kopiert die Member der **VIDEOINFOHEADER-Struktur** in sie und ersetzt die alte -Struktur durch die neue -Struktur im Formatblock des Medientyps.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video- und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




