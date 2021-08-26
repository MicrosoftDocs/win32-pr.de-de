---
description: Die MakePalette-Methode erstellt eine logische Palette aus der Farbtabelle in einem Videoformat.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: CImagePalette.MakePalette-Methode (Winutil.h)
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
ms.openlocfilehash: f270797c224617c02b14752b15bbdb54b64a7457670e0b26bae54c39a93657eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055390"
---
# <a name="cimagepalettemakepalette-method"></a>CImagePalette.MakePalette-Methode

Die `MakePalette` -Methode erstellt eine logische Palette aus der Farbtabelle in einem Videoformat.

## <a name="syntax"></a>Syntax


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Zeiger auf eine [**VIDEOINFOHEADER-Struktur,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) die die Farbtabelle enthält.

</dd> <dt>

*szDevice* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Anzeigegeräts enthält, wie von der **GDI-Funktion EnumDisplayDevices** zurückgegeben. Um das Hauptanzeigegerät zu verwenden, legen Sie diesen Parameter auf **NULL** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, gibt ein Handle an die Palette zurück. Andernfalls gibt **NULL** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImagePalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




