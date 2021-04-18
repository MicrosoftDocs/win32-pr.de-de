---
description: Die checkvideoinfotype-Funktion überprüft einen Medientyp, der eine videoinfoheader-Format Struktur enthält, für bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Checkvideoinfotype-Funktion (checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371624"
---
# <a name="checkvideoinfotype-function"></a>Checkvideoinfotype-Funktion

Die- `CheckVideoInfoType` Funktion überprüft einen Medientyp, der eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Format Struktur für bestimmte häufige Fehler enthält, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.

> [!Note]  
> Diese Funktion garantiert nicht, dass der Medientyp gültig ist oder dass der Code, der die Struktur verwendet, sicher ist.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf die zu validierende [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                                | Beschreibung                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                  | **Null** -Zeiger Wert.<br/> |
| <dl> <dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> </dl> | Ungültiger Medientyp.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion ruft [**validatebitmapinfoheader**](validatebitmapinfoheader.md) auf, um die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur im Medientyp zu validieren. Wenn der Formattyp nicht Format \_ videoinfo ist, gibt die Funktion den VFW \_ E- \_ Typ \_ nicht \_ akzeptiert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video-und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




