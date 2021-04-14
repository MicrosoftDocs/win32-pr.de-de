---
title: glCopyTexSubImage2D-Funktion (GL. h)
description: Die glCopyTexSubImage2D-Funktion kopiert ein untergeordnetes Bild eines zweidimensionalen Textur Bilds aus dem Framebuffer.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- glCopyTexSubImage2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391992"
---
# <a name="glcopytexsubimage2d-function"></a>glCopyTexSubImage2D-Funktion

Die **glCopyTexSubImage2D** -Funktion kopiert ein untergeordnetes Bild eines zweidimensionalen Textur Bilds aus dem Framebuffer.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Das Ziel, in das die Bilddaten geändert werden. Muss den Wert "GL \_ Texture \_ 2D" aufweisen.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebene. Ebene 0 ist das Basis Image. Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.

</dd> <dt>

*xoffset* 
</dt> <dd>

Der textOffset in der *x* -Richtung innerhalb des Textur Arrays.

</dd> <dt>

*yoffset* 
</dt> <dd>

Der texveroffset in der *y* -Richtung innerhalb des Textur Arrays.

</dd> <dt>

*x* 
</dt> <dd>

Die x-Ebenen-Koordinaten des Fensters der unteren linken Ecke der Zeile der zu kopierenden Pixel.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Ebenen-Koordinaten des Fensters der unteren linken Ecke der Zeile der zu kopierenden Pixel.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des unter Bilds des Textur Bilds. Das Angeben eines Textur unter Bilds mit einer Breite von NULL hat keine Auswirkungen.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des unter Bilds des Textur Bilds. Das Angeben eines Textur unter Bilds mit einer Breite von NULL hat keine Auswirkungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Ziel* war kein akzeptierter Wert.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Ebene* war kleiner als 0 (null) oder größer als *Log* 2 (*Max*), wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size ist.<br/>                                                                                                                                                                                          |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *xoffset* war kleiner als der *Rahmen oder (* *xoffset*  +  *Width*) war größer als (*w*  +  *Border*), *yoffset* war kleiner als *Border*, oder (*yoffset*  +  *height*) war größer als (*h*  +  -Rahmen), wobei *w* für die Breite von GL und der Rahmen der \_ \_ GL-Textur Rahmen ist  \_ \_ . Beachten Sie, dass *w* die doppelte *Rahmenbreite umfasst* .<br/> |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | " *Width* " war kleiner als " *Border* " oder " *y* " ist kleiner als " *Border*", wobei " *Border* " die Rahmenbreite des Textur Arrays ist.<br/>                                                                                                                                                                                           |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Das Textur Array wurde nicht durch einen vorherigen [**glTexImage1D**](glteximage1d.md) -Vorgang definiert.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                                                                                                                                                       |



## <a name="remarks"></a>Bemerkungen

Die **glCopyTexSubImage2D** -Funktion ersetzt einen rechteckigen Teil eines zweidimensionalen Textur Bilds durch Pixel aus dem aktuellen Framebuffer, nicht aus dem Hauptspeicher, wie es bei [**glTexSubImage2D**](gltexsubimage2d.md)der Fall ist.

Ein Rechteck aus Pixeln, beginnend mit *den x* -und *y* -Fenster Koordinaten und mit den Abmessungen *Width* und *height* , ersetzt den Teil des Textur Arrays durch *xoffset* + (*Width* -1), wobei die Indizes *yoffset* *durch* *yoffset* + (*Width* -1) auf der durch *Ebene* angegebenen MipMap-Ebene liegen. Das Ziel Rechteck im Textur Array darf keine texeln außerhalb des ursprünglich angegebenen Textur Arrays enthalten.

Die **glCopyTexSubImage2D** -Funktion verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glcopypixels**](glcopypixels.md), mit dem Unterschied, dass vor der abschließenden Konvertierung der Pixel alle Pixel Komponenten Werte an den Bereich \[ 0, 1 gebunden und in das \] interne Format der Textur für die Speicherung im Textur Array konvertiert werden. Die Pixel Reihenfolge wird mit niedrigeren *x* -Koordinaten bestimmt, die den unteren Texturkoordinaten entsprechen. Wenn eine der Pixel innerhalb einer angegebenen Zeile des aktuellen Frame Puffer außerhalb des Fensters liegt, das dem aktuellen renderingkontext zugeordnet ist, sind ihre Werte nicht definiert.

Wenn einer der Pixel innerhalb des angegebenen Rechtecks des aktuellen Frame Puffer außerhalb des dem aktuellen renderingkontext zugeordneten Lese Fensters liegt, sind die für diese Pixel erhaltenen Werte nicht definiert. An der *internalformat*-, *Width*-, *height*-oder *Border* -Parameter des angegebenen Textur Arrays oder an Texttyp außerhalb des angegebenen Textur unter Bilds wird keine Änderung vorgenommen.

Sie können **glCopyTexSubImage2D** -Aufrufe nicht in Anzeigelisten einschließen.

> [!Note]  
> Die **glCopyTexSubImage2D** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

Die Texturierung hat keine Auswirkung auf den Farb Index Modus. Die Funktionen " [**glpixelstore**](glpixelstore-functions.md) " und " [**glpixeltransfer**](glpixeltransfer.md) " beeinflussen die Textur Bilder genau so, wie Sie sich auf die Art und Weise auswirken, wie Pixel mithilfe von " [**gldrawpixels**](gldrawpixels.md)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glCopyTexSubImage2D** ab:

[**glgetteximage**](glgetteximage.md)

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ 2D

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

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





