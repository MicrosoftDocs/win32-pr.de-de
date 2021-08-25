---
description: Die CreateAudioMediaType-Funktion initialisiert einen Medientyp aus einer WAVEFORMATEX-Struktur.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: CreateAudioMediaType-Funktion (Mtype.h)
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
ms.openlocfilehash: 2eb9dc01a398a498252cca2f1f3af012608f8e0ca80c62800c56e4026c0b0a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908820"
---
# <a name="createaudiomediatype-function"></a>CreateAudioMediaType-Funktion

Die **CreateAudioMediaType-Funktion** initialisiert einen Medientyp aus einer [**WAVEFORMATEX-Struktur.**](/previous-versions/dd757713(v=vs.85))

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

Zeiger auf die angegebene [**WAVEFORMATEX-Struktur.**](/previous-versions/dd757713(v=vs.85))

</dd> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf die [**zu initialisierende AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> <dt>

*bSetFormat* 
</dt> <dd>

Flag, das angibt, ob der Formatblock initialisiert werden soll. Geben Sie **TRUE** an, um sie zu initialisieren, andernfalls **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ OUTOFMEMORY zurück, wenn den Formatdaten kein Arbeitsspeicher zugeordnet werden konnte. \_Andernfalls S OK.

## <a name="remarks"></a>Hinweise

Wenn der *bSetFormat-Parameter* **TRUE ist,** ordnet die Methode den Arbeitsspeicher für den Formatblock zu. Wenn der *pmt-Parameter* bereits einen zugeordneten Formatblock enthält, tritt ein Arbeitsspeicherverlust auf. Um einen Arbeitsspeicherverlust zu vermeiden, rufen [**Sie FreeMediaType auf,**](freemediatype.md) bevor Sie diese Funktion aufrufen. Nachdem die Methode zurückgegeben wurde, rufen **Sie FreeMediaType erneut** auf, um den Formatblock frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medientypfunktionen**](media-type-functions.md)
</dt> </dl>

 

