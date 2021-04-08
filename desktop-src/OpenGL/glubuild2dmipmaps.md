---
title: gluBuild2DMipmaps-Funktion (glu. h)
description: Die gluBuild2DMipmaps-Funktion erstellt 2-D-Mipmaps.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- gluBuild2DMipmaps-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949579"
---
# <a name="glubuild2dmipmaps-function"></a>gluBuild2DMipmaps-Funktion

Die **gluBuild2DMipmaps** -Funktion erstellt 2-D-Mipmaps.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Ziel Textur. Muss "GL \_ Texture \_ 2D" lauten.

</dd> <dt>

*components* 
</dt> <dd>

Die Anzahl der Farbkomponenten in der Textur. Muss 1, 2, 3 oder 4 sein.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Textur Bilds.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Textur Bilds.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Muss einer der folgenden sein: GL \_ Color \_ Index, GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance oder GL \_ Luminance \_ alpha.

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp für *Daten*. Muss eines der folgenden sein: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int oder GL \_ float.

</dd> <dt>

*data* 
</dt> <dd>

Ein Zeiger auf die Bilddaten im Arbeitsspeicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **gluBuild2DMipmaps** -Funktion Ruft das Eingabebild ab und generiert alle MipMap-Bilder (mit " [**gluscaleimage**](gluscaleimage.md)"), sodass das Eingabebild als ein mipzugeordnetes Textur Bild verwendet werden kann. Um jedes Abbild zu laden, wenden Sie [**glTexImage2D**](glteximage2d.md)an. Wenn die Dimensionen des Eingabe Bilds keine Kräfte von zwei sind, wird das Bild so skaliert, dass sowohl die Breite als auch die Höhe die Kräfte von zwei sind, bevor die Mipmaps generiert werden.

Der Rückgabewert 0 (null) gibt den Erfolg an. Andernfalls wird ein glu-Fehlercode zurückgegeben (siehe [**gluerrorstring**](gluerrorstring.md)).

Eine Beschreibung der zulässigen Werte für den *Format* -Parameter finden Sie unter **glTexImage2D**. Eine Beschreibung der zulässigen Werte für *Type* finden Sie unter [**gldrawpixels**](gldrawpixels.md).

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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluscaleimage**](gluscaleimage.md)
</dt> </dl>

 

 





