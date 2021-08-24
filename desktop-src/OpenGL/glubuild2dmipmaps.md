---
title: gluBuild2DMipmaps-Funktion (Glu.h)
description: Die gluBuild2DMipmaps-Funktion erstellt 2D-Mipmaps.
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
ms.openlocfilehash: f27dcf3d0e95b0b52d5b7f4c4ce0e5692f3fc856b81d9c1d82c9661a70e2f818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489650"
---
# <a name="glubuild2dmipmaps-function"></a>gluBuild2DMipmaps-Funktion

Die **gluBuild2DMipmaps-Funktion** erstellt 2D-Mipmaps.

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

Die Zieltextur. Muss GL \_ TEXTURE \_ 2D sein.

</dd> <dt>

*components* 
</dt> <dd>

Die Anzahl der Farbkomponenten in der Textur. Muss 1, 2, 3 oder 4 sein.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Texturbilds.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Texturbilds.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Es muss eine der folgenden Werte vorhanden sein: GL \_ COLOR \_ INDEX, GL \_ RED, GL \_ \_ GREEN, GL BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE oder GL \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp für *die Daten*. Folgendes muss sein: GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT oder GL \_ FLOAT.

</dd> <dt>

*data* 
</dt> <dd>

Ein Zeiger auf die Bilddaten im Arbeitsspeicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluBuild2DMipmaps-Funktion** ruft das Eingabebild ab und generiert alle Mipmapbilder [**(mithilfe von gluScaleImage),**](gluscaleimage.md)damit das Eingabebild als mipmappeniertes Texturbild verwendet werden kann. Rufen Sie [**glTexImage2D**](glteximage2d.md)auf, um die einzelnen Bilder zu laden. Wenn die Abmessungen des Eingabebilds keine Zweierstärken sind, wird das Bild so skaliert, dass sowohl die Breite als auch die Höhe die Zweierleistung sind, bevor die Mipmaps generiert werden.

Der Rückgabewert 0 (null) gibt den Erfolg an. Andernfalls wird ein GLU-Fehlercode zurückgegeben (siehe [**gluErrorString**](gluerrorstring.md)).

Eine Beschreibung der zulässigen Werte für den *Formatparameter* finden Sie unter **glTexImage2D**. Eine Beschreibung der zulässigen Werte für *den Typ finden Sie* unter [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





