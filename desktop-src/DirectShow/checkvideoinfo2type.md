---
description: Die CheckVideoInfo2Type-Funktion überprüft einen Medientyp, der eine VIDEOINFOHEADER2-Formatstruktur enthält, auf bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige Überläufe verursachen können.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: CheckVideoInfo2Type-Funktion (Checkbmi.h)
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
ms.openlocfilehash: 48d9deab4d87868cbc9e5418ccd6b7e2c7e9ecf93350ad70cb6c934d365e4655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074184"
---
# <a name="checkvideoinfo2type-function"></a>CheckVideoInfo2Type-Funktion

Die Funktion überprüft einen Medientyp, der eine `CheckVideoInfo2Type` [**VIDEOINFOHEADER2-Formatstruktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) enthält, auf bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige Überläufe verursachen können.

> [!Note]  
> Diese Funktion garantiert nicht, dass der Medientyp gültig ist oder dass Code, der die -Struktur verwendet, sicher ist.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf die [**zu überprüfende AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg<br/>                |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>                  | **NULL-Zeigerwert**<br/> |
| <dl> <dt>**VFW \_ \_ E-TYP \_ NICHT \_ AKZEPTIERT**</dt> </dl> | Ungültiger Medientyp<br/>     |



 

## <a name="remarks"></a>Hinweise

Diese Funktion ruft [**ValidateBitmapInfoHeader auf,**](validatebitmapinfoheader.md) um die [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) im Medientyp zu überprüfen. Wenn der Formattyp nicht **FORMAT \_ VideoInfo2 ist,** gibt die Funktion **VFW \_ E TYPE NOT ACCEPTED \_ \_ \_ zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Checkbmi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Video- und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




