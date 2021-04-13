---
title: gluscaleimage-Funktion (glu. h)
description: Die Funktion "gluscaleimage" skaliert ein Bild auf eine beliebige Größe.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- gluscaleimage-Funktion OpenGL
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
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391501"
---
# <a name="gluscaleimage-function"></a>gluscaleimage-Funktion

Die Funktion " **gluscaleimage** " skaliert ein Bild auf eine beliebige Größe.

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

Das Format der Pixeldaten. Die folgenden symbolischen Werte sind gültig: GL \_ Color \_ Index, GL \_ Stencil \_ Index, GL- \_ tiefen \_ Komponente, GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Helligkeit und GL \_ Luminance \_ alpha.

</dd> <dt>

*widthin* 
</dt> <dd>

Die Breite des skalierten Quell Bilds.

</dd> <dt>

*Erhöhung* 
</dt> <dd>

Die Höhe des skalierten Quell Bilds.

</dd> <dt>

*typein* 
</dt> <dd>

Der *Datentyp für Datain*. Muss eines der folgenden sein: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int oder GL \_ float.

</dd> <dt>

*Datain* 
</dt> <dd>

Ein Zeiger auf das Quell Bild.

</dd> <dt>

*widthout* 
</dt> <dd>

Die Breite des Ziel Bilds.

</dd> <dt>

*"heightout"* 
</dt> <dd>

Die Höhe des Ziel Bilds.

</dd> <dt>

*meinen* 
</dt> <dd>

Der *Datentyp für dataout*. Muss eines der folgenden sein: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int oder GL \_ float.

</dd> <dt>

*dataout* 
</dt> <dd>

Ein Zeiger auf das Ziel Image.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert „0“.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein glu-Fehlercode (siehe [**gluerrorstring**](gluerrorstring.md)).

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluscaleimage** " skaliert ein Pixel Bild mithilfe der entsprechenden Pixel Speicher Modi, um Daten aus dem Quell Abbild zu entpacken und Daten in das Ziel Image zu packen.

Beim Verkleinern eines Bilds verwendet " **gluscaleimage** " einen Feld Filter, um ein Beispiel für das Quell Abbild zu erstellen und Pixel für das Ziel Image zu erstellen. Beim Vergrößern eines Bilds werden die Pixel des Quell Bilds linear interpoliert, um das Ziel Image zu erstellen.

Eine Beschreibung der zulässigen Werte für die Parameter " *Format*", " *typein*" und " *meinen* " finden Sie unter [**glread Pixels**](glreadpixels.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluerrorstring**](gluerrorstring.md)
</dt> </dl>

 

 





