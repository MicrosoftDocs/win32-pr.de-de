---
title: gluBuild1DMipmaps-Funktion (glu. h)
description: Die gluBuild1DMipmaps-Funktion erstellt 1-D-Mipmaps.
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
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338529"
---
# <a name="glubuild1dmipmaps-function"></a>gluBuild1DMipmaps-Funktion

Die **gluBuild1DMipmaps** -Funktion erstellt 1-D-Mipmaps.

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

Die Ziel Textur. Muss "GL \_ Texture \_ 1D" lauten.

</dd> <dt>

*components* 
</dt> <dd>

Die Anzahl der Farbkomponenten in der Textur. Muss 1, 2, 3 oder 4 sein.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Textur Bilds.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Die folgenden Werte sind gültig: GL \_ Color \_ Index, GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance oder GL \_ Luminance \_ alpha.

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp für *Daten*. Die folgenden Werte sind gültig: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int oder GL \_ float.

</dd> <dt>

*data* 
</dt> <dd>

Ein Zeiger auf die Bilddaten im Arbeitsspeicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **gluBuild1DMipmaps** -Funktion Ruft das Eingabebild ab und generiert alle MipMap-Bilder (mit " [**gluscaleimage**](gluscaleimage.md)"), sodass das Eingabebild als ein mipzugeordnetes Textur Bild verwendet werden kann. Die [**glTexImage1D**](glteximage1d.md) -Funktion wird dann aufgerufen, um die einzelnen Bilder zu laden. Wenn die Breite des Eingabe Bilds keine Potenz von zwei ist, wird das Bild auf die nächste Potenz von zwei skaliert, bevor die Mipmaps generiert werden.

Der Rückgabewert 0 (null) gibt den Erfolg an. Andernfalls wird ein glu-Fehlercode zurückgegeben (siehe [**gluerrorstring**](gluerrorstring.md)).

Eine Beschreibung der zulässigen Werte für den *Format* -Parameter finden Sie unter **glTexImage1D**. Eine Beschreibung der zulässigen Werte für den *Typparameter* finden Sie unter [**gldrawpixels**](gldrawpixels.md).

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluscaleimage**](gluscaleimage.md)
</dt> </dl>

 

 





