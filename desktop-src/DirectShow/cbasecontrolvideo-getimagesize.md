---
description: Die getimagesize-Methode ruft Informationen zur Video Bild Größe ab.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Cbasecontrolvideo. getimagesize-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364502"
---
# <a name="cbasecontrolvideogetimagesize-method"></a>Cbasecontrolvideo. getimagesize-Methode

Die- `GetImageSize` Methode ruft Informationen zur Video Bild Größe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvideoinfo* 
</dt> <dd>

Zeiger auf eine [**videinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur, die ausgefüllt werden soll.

</dd> <dt>

*pbuffersize* 
</dt> <dd>

Ein Zeiger auf die Größe des Video Puffers.

</dd> <dt>

*psourcerect* 
</dt> <dd>

Zeiger auf die Rechteck Abmessungen des Quellvideos.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.



| Rückgabecode                                                                                  | Beschreibung                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>       | Fehler.<br/>                                                       |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiges Argument. Das Datenformat ist nicht kompatibel.<br/>           |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Unerwarteter Fehler. Mindestens ein Argument ist **null**.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>       | Erfolg.<br/>                                                       |



 

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion ist eine Hilfsfunktion zum Erstellen von Image-Renderings von DIB-Images im Speicher. Sie wird von der Basisklassen Implementierung von [**cbasecontrolvideo:: Get-/timage**](cbasecontrolvideo-getcurrentimage.md) aufgerufen, wenn ein **null**-_pvideoimage_ -Parameter an diese Member-Funktion übergeben wird. Folglich erstellt diese Member-Funktion eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur und gibt Sie zurück, wobei die Informationen in *pbuffersize* und *psourcerect* verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




