---
title: gluBuild1DMipmaps-Funktion (Glu.h)
description: Die gluBuild1DMipmaps-Funktion erstellt 1D-Mipmaps.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- gluBuild1DMipmaps-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c2b76a37fa7088835ad0238065b0647ff0beb973c1c3ffa1b892f6e0958d97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489690"
---
# <a name="glubuild1dmipmaps-function"></a>gluBuild1DMipmaps-Funktion

Die **gluBuild1DMipmaps-Funktion** erstellt 1D-Mipmaps.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Zieltextur. Muss GL \_ TEXTURE \_ 1D sein.

</dd> <dt>

*components* 
</dt> <dd>

Die Anzahl der Farbkomponenten in der Textur. Muss 1, 2, 3 oder 4 sein.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Texturbilds.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Die folgenden Werte sind gültig: GL \_ COLOR \_ INDEX, GL \_ RED, GL \_ \_ GREEN, GL BLUE, GL \_ ALPHA, GL \_ RGB, \_ GL RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE oder GL \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp für *die Daten*. Die folgenden Werte sind gültig: GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT oder GL \_ FLOAT.

</dd> <dt>

*data* 
</dt> <dd>

Ein Zeiger auf die Bilddaten im Arbeitsspeicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **Funktion gluBuild1DMipmaps** ruft das Eingabebild ab und generiert alle Mipmapbilder (mithilfe [**von gluScaleImage),**](gluscaleimage.md)sodass das Eingabebild als mipmappeniertes Texturbild verwendet werden kann. Die [**glTexImage1D-Funktion**](glteximage1d.md) wird dann aufgerufen, um jedes der Bilder zu laden. Wenn die Breite des Eingabebilds keine Zweierstärke ist, wird das Bild auf die nächste Zweierstärke skaliert, bevor die Mipmaps generiert werden.

Der Rückgabewert 0 (null) gibt den Erfolg an. Andernfalls wird ein GLU-Fehlercode zurückgegeben (siehe [**gluErrorString**](gluerrorstring.md)).

Eine Beschreibung der zulässigen Werte für den *Formatparameter* finden Sie unter **glTexImage1D**. Eine Beschreibung der zulässigen Werte für den *Typparameter* finden Sie unter [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





