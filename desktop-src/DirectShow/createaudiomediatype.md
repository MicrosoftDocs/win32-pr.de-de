---
description: Die Funktion "deateaudiomediatype" Initialisiert einen Medientyp aus einer WaveFormatEx-Struktur.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Funktion "kreateaudiomediatype" (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354719"
---
# <a name="createaudiomediatype-function"></a>Funktion "kreateaudiomediatype"

Die Funktion " **deateaudiomediatype** " Initialisiert einen Medientyp aus einer [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwfx* 
</dt> <dd>

Ein Zeiger auf die angegebene [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.

</dd> <dt>

*PMT* 
</dt> <dd>

Zeiger auf die zu initialisierende [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.

</dd> <dt>

*bsetformat* 
</dt> <dd>

Flag zum angeben, ob der Format Block initialisiert werden soll. Geben Sie **true** an, um es zu initialisieren, oder andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E \_ outof Memory" zurück, wenn der Arbeitsspeicher für die Formatierungsdaten nicht zugeordnet werden konnte. \_Andernfalls OK.

## <a name="remarks"></a>Bemerkungen

Wenn der *bsetformat* -Parameter **true** ist, ordnet die Methode den Speicher für den Format Block zu. Wenn der *PMT* -Parameter bereits einen zugeordneten Format Block enthält, tritt ein Speicherplatz auf. Um einen Speicherplatz zu vermeiden, rufen Sie " [**fremediatype**](freemediatype.md) " auf, bevor Sie diese Funktion aufrufen. Nachdem die Methode zurückgegeben wurde, können Sie **freemediatype** erneut aufzurufen, um den Format Block freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medientyp Funktionen**](media-type-functions.md)
</dt> </dl>

 

