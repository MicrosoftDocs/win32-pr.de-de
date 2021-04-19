---
description: Die setmediatype-Methode legt den unkomprimierten Medientyp für die Gruppe fest.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'Iamtimelinegroup:: setmediatype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359731"
---
# <a name="iamtimelinegroupsetmediatype-method"></a>Iamtimelinegroup:: setmediatype-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetMediaType` Methode legt den unkomprimierten Medientyp für die Gruppe fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die das Format beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                             | Beschreibung                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                             |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>               | **Null** -Zeigerargument.<br/>           |
| <dl> <dt>**VFW \_ E \_ invalidmediatype**</dt> </dl> | Der angegebene Medientyp ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Medientypen werden unterstützt:

-   Unkomprimiertes RGB-Video
-   16 Bits pro Pixel, 555-Format (mediasubtype \_ RGB555)
-   24 Bits pro Pixel (mediasubtype \_ RGB24)
-   32 Bits pro Pixel, mit Alpha (mediasubtype \_ ARGB32, nicht mediasubtype \_ RGB32)
-   16-Bit-Stereo PCM-Audiodatei (mediasubtype \_ PCM)

Video Typen müssen für den \_ Formattyp und den [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) für den Format-Block Video Info Format verwenden. Das [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format wird nicht unterstützt. Außerdem werden Top-Down-Videoformate (*biheight* < 0) nicht unterstützt.

Um ein Komprimierungs Format für die Gruppe anzugeben, rufen Sie die [**iamtimelinegroup::**](iamtimelinegroup-setsmartrecompressformat.md) "-Methode auf.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelinegroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




