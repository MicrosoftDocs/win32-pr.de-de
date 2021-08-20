---
description: Die CheckVideoInfoType-Funktion überprüft einen Medientyp, der eine VIDEOINFOHEADER-Formatstruktur enthält, auf bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige Überläufe verursachen können.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: CheckVideoInfoType-Funktion (Checkbmi.h)
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
ms.openlocfilehash: 4463a1edb2002f64e983a38eb4a0ace5b5289b4d47ac43c8ea27bf165138ff95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539540"
---
# <a name="checkvideoinfotype-function"></a>CheckVideoInfoType-Funktion

Die Funktion überprüft einen Medientyp, der eine `CheckVideoInfoType` [**VIDEOINFOHEADER-Formatstruktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) enthält, auf bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige Überläufe verursachen können.

> [!Note]  
> Diese Funktion garantiert nicht, dass der Medientyp gültig ist oder dass Code, der die -Struktur verwendet, sicher ist.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf die [**zu überprüfende AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>                  |  NULL-Zeigerwert.<br/> |
| <dl> <dt>**VFW \_ \_ E-TYP \_ NICHT \_ AKZEPTIERT**</dt> </dl> | Ungültiger Medientyp.<br/>     |



 

## <a name="remarks"></a>Hinweise

Diese Funktion ruft [**ValidateBitmapInfoHeader auf,**](validatebitmapinfoheader.md) um die [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) im Medientyp zu überprüfen. Wenn der Formattyp nicht FORMAT \_ VideoInfo ist, gibt die Funktion VFW \_ E TYPE NOT ACCEPTED \_ \_ \_ zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Checkbmi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video- und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




