---
description: Sie können Bildmetadaten mithilfe eines PropertyItem-Objekts speichern und abrufen. Der Typdatenmember eines PropertyItem-Objekts gibt den Datentyp der Werte an, die im Wertdatenmember desselben PropertyItem-Objekts gespeichert sind.
ms.assetid: d05cdf42-4b30-45ce-85a1-025d4f4e9d13
title: Typkonstanten für Bildeigenschaftentags (Gdiplusimaging.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb565972b2dc8b8962e367c7d2f3c09b4f857382156538a83f7d6ee338c66ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977600"
---
# <a name="image-property-tag-type-constants"></a>Tagtypkonstanten für Bildeigenschaften

Sie können Bildmetadaten mithilfe eines [**PropertyItem-Objekts**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) speichern und abrufen. Der **Typdatenmember** eines **PropertyItem-Objekts** gibt den Datentyp der Werte an, die im Wertdatenmember desselben **PropertyItem-Objekts** gespeichert sind.

Die folgenden Konstanten, die in Gdiplusimaging.h definiert sind, können dem **Typdatenmember** eines [**PropertyItem-Objekts**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) zugewiesen werden.



| Konstante                                                                                                                                                                                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>         | Gibt an, dass das Format 4 Bits pro Pixel ist und indizierte Farben verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="PropertyTagTypeASCII"></span><span id="propertytagtypeascii"></span><span id="PROPERTYTAGTYPEASCII"></span><dl> <dt>**PropertyTagTypeASCII**</dt> </dl>                 | Gibt an, dass der **Wertdatenmember** eine AUF NULL endende ASCII-Zeichenfolge ist. Wenn Sie den **Typdatenmember** eines [**PropertyItem-Objekts**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) auf PropertyTagTypeASCII festlegen, sollten Sie den **Length-Datenmember** auf die Länge der Zeichenfolge einschließlich des NULL-Abschlusszeichens festlegen. Die Zeichenfolge hat beispielsweise `HELLO` eine Länge von 6.<br/> |
| <span id="PropertyTagTypeByte"></span><span id="propertytagtypebyte"></span><span id="PROPERTYTAGTYPEBYTE"></span><dl> <dt>**PropertyTagTypeByte**</dt> </dl>                     | Gibt an, dass der **Wertdatenmember** ein Bytearray ist.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PropertyTagTypeLong"></span><span id="propertytagtypelong"></span><span id="PROPERTYTAGTYPELONG"></span><dl> <dt>**PropertyTagTypeLong**</dt> </dl>                     | Gibt an, dass der **Wertdatenmember** ein Array von ganzen Zahlen ohne Vorzeichen (32 Bit) ist.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PropertyTagTypeRational"></span><span id="propertytagtyperational"></span><span id="PROPERTYTAGTYPERATIONAL"></span><dl> <dt>**PropertyTagTypeRational**</dt> </dl>     | Gibt an, dass der **Wertdatenmember** ein Array von Paaren von langen ganzen Zahlen ohne Vorzeichen ist. Jedes Paar stellt einen Bruch dar. Die erste ganze Zahl ist der Zähler, und die zweite ganze Zahl ist der Nenner.<br/>                                                                                                                                                                       |
| <span id="PropertyTagTypeShort"></span><span id="propertytagtypeshort"></span><span id="PROPERTYTAGTYPESHORT"></span><dl> <dt>**PropertyTagTypeShort**</dt> </dl>                 | Gibt an, dass der **Wertdatenmember** ein Array von 16-Bit-Ganzzahlen ohne Vorzeichen ist.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="PropertyTagTypeSLONG"></span><span id="propertytagtypeslong"></span><span id="PROPERTYTAGTYPESLONG"></span><dl> <dt>**PropertyTagTypeSLONG**</dt> </dl>                 | Gibt an, dass der **Wertdatenmember** ein Array von ganzen Zahlen mit Vorzeichen (32 Bit) ist.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="PropertyTagTypeSRational"></span><span id="propertytagtypesrational"></span><span id="PROPERTYTAGTYPESRATIONAL"></span><dl> <dt>**PropertyTagTypeSRational**</dt> </dl> | Gibt an, dass der **Wertdatenmember** ein Array von Paaren von langen ganzen Zahlen mit Vorzeichen ist. Jedes Paar stellt einen Bruch dar. Die erste ganze Zahl ist der Zähler, und die zweite ganze Zahl ist der Nenner.<br/>                                                                                                                                                                         |
| <span id="PropertyTagTypeUndefined"></span><span id="propertytagtypeundefined"></span><span id="PROPERTYTAGTYPEUNDEFINED"></span><dl> <dt>**PropertyTagTypeUndefined**</dt> </dl> | Gibt an, dass der **Wertdatenmember** ein Bytearray ist, das Werte eines beliebigen Datentyps enthalten kann. <br/>                                                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Gdiplusimaging.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Tagkonstanten für Bildeigenschaften](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[Image File Format-Spezifikationen](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Lesen und Schreiben von Metadaten](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 
