---
title: glCopyTexSubImage1D-Funktion (GL. h)
description: Die glCopyTexSubImage1D-Funktion kopiert ein unter Bild eines eindimensionalen Textur Bilds aus dem Framebuffer.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- glCopyTexSubImage1D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956700"
---
# <a name="glcopytexsubimage1d-function"></a>glCopyTexSubImage1D-Funktion

Die **glCopyTexSubImage1D** -Funktion kopiert ein unter Bild eines eindimensionalen Textur Bilds aus dem Framebuffer.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Das Ziel, in das die Bilddaten geändert werden. Muss den Wert "GL \_ Texture \_ 1D" aufweisen.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebene. Ebene 0 ist das Basis Image. Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.

</dd> <dt>

*xoffset* 
</dt> <dd>

Der texveroffset innerhalb des Textur Arrays.

</dd> <dt>

*x* 
</dt> <dd>

Die x-Ebenen-Koordinate der unteren linken Ecke der Zeile der zu kopierenden Pixel.

</dd> <dt>

*y* 
</dt> <dd>

Die y-ebenenkoordinate des Fensters der unteren linken Ecke der Zeile der zu kopierenden Pixel.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des unter Bilds des Textur Bilds. Das Angeben eines Textur unter Bilds mit einer Breite von NULL hat keine Auswirkungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Ziel* war kein akzeptierter Wert.<br/>                                                                                                                                                                               |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Ebene* war kleiner als 0 (null), oder die *Ebene* ist größer als *Log* 2 (*Max*), wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size ist.<br/>                                                                                 |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *xoffset* war kleiner als der *Rahmen oder (* *xoffset*  +  *Width*) war größer als (*w*-Rahmen  +  ), wobei *w* die Breite von GL und der Rahmen der \_ \_ GL-Textur Rahmen ist  \_ \_ . Beachten Sie, dass *w* die doppelte *Rahmenbreite umfasst* .<br/> |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | " *Width* " war kleiner als " *Border* " oder " *y* " ist kleiner als " *Border*", wobei " *Border* " die Rahmenbreite des Textur Arrays ist.<br/>                                                                                            |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Das Textur Array wurde nicht durch einen vorherigen [**glTexImage1D**](glteximage1d.md) -Vorgang definiert.<br/>                                                                                                                   |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                                                        |



## <a name="remarks"></a>Bemerkungen

Die **glCopyTexSubImage1D** -Funktion ersetzt einen Teil eines eindimensionalen Textur Bilds mithilfe von Pixeln aus dem aktuellen Framebuffer, nicht aus dem Hauptspeicher, wie es bei [**glTexSubImage1D**](gltexsubimage1d.md)der Fall ist.

Eine Zeile mit Pixeln, beginnend mit den durch *x* und *y* angegebenen Fenster Koordinaten und mit der Längen *Breite* , ersetzt den Teil des Textur *Arrays durch xoffset +* (  *Width* -1). Das Ziel im Textur Array darf keine texeln außerhalb des ursprünglich angegebenen Textur Arrays enthalten.

Die **glCopyTexSubImage1D** -Funktion verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glcopypixels**](glcopypixels.md) , mit dem Unterschied, dass vor der abschließenden Konvertierung der Pixel alle Pixel Komponenten Werte an den Bereich \[ 0, 1 gebunden \] und in das interne Format der Textur für die Speicherung im Textur Array konvertiert werden. Die Pixel Reihenfolge wird mit niedrigeren *x* -Koordinaten bestimmt, die den unteren Texturkoordinaten entsprechen. Wenn eine der Pixel innerhalb einer angegebenen Zeile des aktuellen Frame Puffer außerhalb des Fensters liegt, das dem aktuellen renderingkontext zugeordnet ist, sind ihre Werte nicht definiert.

Der *internalformat*-, *Width*-oder Border-Parameter des angegebenen Textur Arrays oder der *Border* -Wert außerhalb des angegebenen Textur unter Bilds wird nicht geändert.

Sie können **glCopyTexSubImage1D** -Aufrufe nicht in Anzeigelisten einschließen.

> [!Note]  
> Die **glCopyTexSubImage1D** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

Die Texturierung hat keine Auswirkung auf den Farb Index Modus. Die Funktionen " [**glpixelstore**](glpixelstore-functions.md) " und " [**glpixeltransfer**](glpixeltransfer.md) " beeinflussen die Textur Bilder genau so, wie Sie sich auf die Art und Weise auswirken, wie Pixel mithilfe von " [**gldrawpixels**](gldrawpixels.md)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glCopyTexSubImage1D** ab:

[**glgetteximage**](glgetteximage.md)

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Texture \_ 1D

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glnebel**](glfog.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**gltexd**](gltexenv-functions.md)
</dt> <dt>

[**gltexgen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





