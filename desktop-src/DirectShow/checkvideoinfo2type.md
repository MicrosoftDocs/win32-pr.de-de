---
description: Die CheckVideoInfo2Type-Funktion überprüft einen Medientyp, der eine VIDEOINFOHEADER2-Format Struktur enthält, für bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: CheckVideoInfo2Type-Funktion (checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369136"
---
# <a name="checkvideoinfo2type-function"></a>CheckVideoInfo2Type-Funktion

Die- `CheckVideoInfo2Type` Funktion überprüft einen Medientyp, der eine [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format Struktur für bestimmte häufige Fehler enthält, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.

> [!Note]  
> Diese Funktion garantiert nicht, dass der Medientyp gültig ist oder dass der Code, der die Struktur verwendet, sicher ist.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckVideoInfo2Type(
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



| Rückgabecode                                                                                                | Beschreibung                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                  | **Null** -Zeiger Wert<br/> |
| <dl> <dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> </dl> | Ungültiger Medientyp.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion ruft [**validatebitmapinfoheader**](validatebitmapinfoheader.md) auf, um die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur im Medientyp zu validieren. Wenn der Formattyp nicht " **Format \_ VideoInfo2**" ist, gibt die Funktion " **VFW \_ E \_ Type \_ Not \_ Accepted**" zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video-und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




