---
title: gluScaleImage-Funktion (Glu.h)
description: Die gluScaleImage-Funktion skaliert ein Bild auf eine beliebige Größe.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- gluScaleImage-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a6bab8865dec475087743f658429fd633fc9bb1443da14bd1198e8a7c73b0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488740"
---
# <a name="gluscaleimage-function"></a>gluScaleImage-Funktion

Die **gluScaleImage-Funktion** skaliert ein Bild auf eine beliebige Größe.

## <a name="syntax"></a>Syntax


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Die folgenden symbolischen Werte sind gültig: GL \_ COLOR \_ INDEX, GL \_ STENCIL \_ INDEX, GL \_ DEPTH \_ COMPONENT, GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE und GL \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*widthin* 
</dt> <dd>

Die Breite des Quellbilds, das skaliert wird.

</dd> <dt>

*heightin* 
</dt> <dd>

Die Höhe des Quellbilds, das skaliert wird.

</dd> <dt>

*typein* 
</dt> <dd>

Der Datentyp für *datain*. Folgendes muss sein: GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT oder GL \_ FLOAT.

</dd> <dt>

*datain* 
</dt> <dd>

Ein Zeiger auf das Quellbild.

</dd> <dt>

*widthout* 
</dt> <dd>

Die Breite des Zielbilds.

</dd> <dt>

*heightout* 
</dt> <dd>

Die Höhe des Zielbilds.

</dd> <dt>

*Typeout* 
</dt> <dd>

Der Datentyp für *dataout*. Folgendes muss sein: GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT oder GL \_ FLOAT.

</dd> <dt>

*dataout* 
</dt> <dd>

Ein Zeiger auf das Zielimage.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert „0“.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein GLU-Fehlercode (siehe [**gluErrorString**](gluerrorstring.md)).

## <a name="remarks"></a>Hinweise

Die **gluScaleImage-Funktion** skaliert ein Pixelbild mithilfe der entsprechenden Pixelspeichermodi, um Daten aus dem Quellbild zu entpacken und Daten in das Zielbild zu packen.

Beim Verkleinern eines Bilds verwendet **gluScaleImage** einen Feldfilter, um das Quellbild zu beproben und Pixel für das Zielbild zu erstellen. Beim Vergrößern eines Bilds werden die Pixel aus dem Quellbild linear interpoliert, um das Zielbild zu erstellen.

Eine Beschreibung der zulässigen Werte für die Parameter *format*, *typein* und *typeout* finden Sie unter [**glReadPixels**](glreadpixels.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> </dl>

 

 





