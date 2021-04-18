---
description: Die makepalette-Methode erstellt eine logische Palette aus der Farbtabelle in einem Videoformat.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Cimagepalette. makepalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364584"
---
# <a name="cimagepalettemakepalette-method"></a>Cimagepalette. makepalette-Methode

Mit der- `MakePalette` Methode wird eine logische Palette aus der Farbtabelle in einem Videoformat erstellt.

## <a name="syntax"></a>Syntax


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvideoinfo* 
</dt> <dd>

Zeiger auf eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur, die die Farbtabelle enthält.

</dd> <dt>

*szdevice* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Anzeige Geräts enthält, wie von der GDI-Funktion " **EnumDisplayDevices** " zurückgegeben. Legen Sie diesen Parameter auf **null** fest, um das Haupt Anzeigegerät zu verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, wird ein Handle für die Palette zurückgegeben. Andernfalls wird **null** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagepalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




