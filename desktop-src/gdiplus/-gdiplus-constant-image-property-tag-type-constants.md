---
description: Sie können Bild Metadaten mithilfe eines PropertyItem-Objekts speichern und abrufen. Der Typdatenmember eines PropertyItem-Objekts gibt den Datentyp der Werte an, die im wertdatenmember desselben PropertyItem-Objekts gespeichert werden.
ms.assetid: d05cdf42-4b30-45ce-85a1-025d4f4e9d13
title: Bildeigenschaften-Tagtyp Konstanten (gdiplusimaging. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1870ad117d8c6f84af9e48f88e94f812c59467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996482"
---
# <a name="image-property-tag-type-constants"></a>Bildeigenschaften-Tagtyp Konstanten

Sie können Bild Metadaten mithilfe eines [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekts speichern und abrufen. Der **Typdatenmember** eines **PropertyItem** -Objekts gibt den Datentyp der Werte an, die im wertdatenmember desselben **PropertyItem** -Objekts gespeichert werden.

Die folgenden Konstanten, die in "gdiplusimaging. h" definiert sind, können dem **Typdatenmember** eines [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekts zugewiesen werden.



| Konstante                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>         | Gibt an, dass das Format 4 Bits pro Pixel ist und indizierte Farben verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="PropertyTagTypeASCII"></span><span id="propertytagtypeascii"></span><span id="PROPERTYTAGTYPEASCII"></span><dl> <dt>**Propertytagtybäuercii**</dt> </dl>                 | Gibt an, dass der **wertdatenmember** eine NULL-terminierte ASCII-Zeichenfolge ist. Wenn Sie den **Typdatenmember** eines [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekts auf propertytagtybäuercii festlegen, sollten Sie das **length** -Datenmember auf die Länge der Zeichenfolge einschließlich des NULL-Terminator festlegen. Beispielsweise würde die Zeichenfolge `HELLO` eine Länge von 6 haben.<br/> |
| <span id="PropertyTagTypeByte"></span><span id="propertytagtypebyte"></span><span id="PROPERTYTAGTYPEBYTE"></span><dl> <dt>**Propertytagtypebyte**</dt> </dl>                     | Gibt an, dass der **wertdatenmember ein Bytearray** ist.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PropertyTagTypeLong"></span><span id="propertytagtypelong"></span><span id="PROPERTYTAGTYPELONG"></span><dl> <dt>**Propertytagtypelong**</dt> </dl>                     | Gibt an, dass der **wertdatenmember** ein Array von ganzen Zahlen (32 Bit) ohne Vorzeichen ist.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PropertyTagTypeRational"></span><span id="propertytagtyperational"></span><span id="PROPERTYTAGTYPERATIONAL"></span><dl> <dt>**Propertytagtyperational**</dt> </dl>     | Gibt an, dass der **wertdatenmember** ein Array von Paaren von langen ganzen Zahlen ohne Vorzeichen ist. Jedes Paar stellt einen Bruchteil dar. die erste ganze Zahl ist der Zähler und die zweite ganze Zahl der Nenner.<br/>                                                                                                                                                                       |
| <span id="PropertyTagTypeShort"></span><span id="propertytagtypeshort"></span><span id="PROPERTYTAGTYPESHORT"></span><dl> <dt>**Propertytagtypeshort**</dt> </dl>                 | Gibt an, dass der **wertdatenmember** ein Array von ganzen Zahlen ohne Vorzeichen (16-Bit) ist.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="PropertyTagTypeSLONG"></span><span id="propertytagtypeslong"></span><span id="PROPERTYTAGTYPESLONG"></span><dl> <dt>**Propertytagtypeslong**</dt> </dl>                 | Gibt an, dass der **wertdatenmember** ein Array von ganzzahligen Long-Werten (32 Bit) ist.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="PropertyTagTypeSRational"></span><span id="propertytagtypesrational"></span><span id="PROPERTYTAGTYPESRATIONAL"></span><dl> <dt>**Propertytagtypesrational**</dt> </dl> | Gibt an, dass der **wertdatenmember** ein Array von Paaren von langen ganzen Zahlen mit Vorzeichen ist. Jedes Paar stellt einen Bruchteil dar. die erste ganze Zahl ist der Zähler und die zweite ganze Zahl der Nenner.<br/>                                                                                                                                                                         |
| <span id="PropertyTagTypeUndefined"></span><span id="propertytagtypeundefined"></span><span id="PROPERTYTAGTYPEUNDEFINED"></span><dl> <dt>**Propertytagtypeundefiniert**</dt> </dl> | Gibt an, dass der **wertdatenmember ein Bytearray** ist, das Werte eines beliebigen Datentyps enthalten kann. <br/>                                                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Gdiplusimaging. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Bildeigenschaften-tagkonstanten](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[Image File Format-Spezifikationen](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Lesen und Schreiben von Metadaten](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 
