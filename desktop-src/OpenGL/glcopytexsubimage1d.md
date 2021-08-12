---
title: glCopyTexSubImage1D-Funktion (Gl.h)
description: Die glCopyTexSubImage1D-Funktion kopiert ein Unterbild eines eindimensionalen Texturbilds aus dem Framepuffer.
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
ms.openlocfilehash: 38c35e28a37608ebbbdbaf331e2837f83022768cf4eb4033cad2a482d477b37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617135"
---
# <a name="glcopytexsubimage1d-function"></a>glCopyTexSubImage1D-Funktion

Die **glCopyTexSubImage1D-Funktion** kopiert ein Unterbild eines eindimensionalen Texturbilds aus dem Framepuffer.

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

Das Ziel, in das die Bilddaten geändert werden. Muss den Wert GL \_ TEXTURE \_ 1D aufweisen.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebenennummer. Ebene 0 ist das Basisimage. Ebene *n* ist das Bild der *n-ten* Mipmapverringerung.

</dd> <dt>

*xoffset* 
</dt> <dd>

Der Texeloffset innerhalb des Texturarrays.

</dd> <dt>

*x* 
</dt> <dd>

Die X-Ebenenkoordinate des Fensters der unteren linken Ecke der Zu kopierenden Pixelzeile.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Ebenenkoordinate des Fensters der unteren linken Ecke der Zu kopierenden Pixelzeile.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Unterbilds des Texturbilds. Das Angeben eines Texturunterbilds mit einer Breite von null hat keine Auswirkungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* war kein akzeptierter Wert.<br/>                                                                                                                                                                               |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *level* war kleiner als 0 (null) oder *ebene* ist größer als *log* 2(*max*), wobei *max* der zurückgegebene Wert von GL MAX TEXTURE \_ SIZE \_ \_ ist.<br/>                                                                                 |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *xoffset* war kleiner als *border* oder (*xoffset*  +  *width*) was greater than (*w*  +  *border*), wobei *w* gleich GL TEXTURE WIDTH \_ und \_ *border* gl TEXTURE \_ BORDER \_ ist. Beachten Sie, dass *w* die doppelte *Rahmenbreite* enthält.<br/> |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *width* war kleiner als *border* oder *y* war kleiner als *border*, wobei *border* die Rahmenbreite des Texturarrays ist.<br/>                                                                                            |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Das Texturarray wurde nicht durch einen vorherigen [**glTexImage1D-Vorgang**](glteximage1d.md) definiert.<br/>                                                                                                                   |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                                                        |



## <a name="remarks"></a>Hinweise

Die **glCopyTexSubImage1D-Funktion** ersetzt einen Teil eines eindimensionalen Texturbilds mitHilfe von Pixeln aus dem aktuellen Framepuffer anstelle des Hauptspeichers, wie dies bei [**glTexSubImage1D**](gltexsubimage1d.md)der Fall ist.

Eine Zeile mit Pixeln, die mit den durch *x* und *y* angegebenen Fensterkoordinaten beginnt, und mit der Längenbreite ersetzt den Teil des Texturarrays durch die Indizes *xoffset* bis *xoffset* + (*breite* – 1).  Das Ziel im Texturarray darf keine Texel außerhalb des ursprünglich angegebenen Texturarrays enthalten.

Die **glCopyTexSubImage1D-Funktion** verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glCopyPixels,**](glcopypixels.md) mit der Ausnahme, dass vor der endgültigen Konvertierung der Pixel alle Pixelkomponentenwerte an den Bereich 0,1 klammern und in \[ das interne Format der Textur für die Speicherung im \] Texturarray konvertiert werden. Die Pixelreihenfolge wird mit niedrigeren *x* Koordinaten bestimmt, die niedrigeren Texturkoordinaten entsprechen. Wenn sich eines der Pixel innerhalb einer angegebenen Zeile des aktuellen Framepuffers außerhalb des Fensters befindet, das dem aktuellen Renderingkontext zugeordnet ist, sind deren Werte nicht definiert.

Es wird keine Änderung am *internalFormat-,* *Width-* oder *Border-Parameter* des angegebenen Texturarrays oder an Texelwerten außerhalb des angegebenen Texturunterbilds vorgenommen.

Aufrufe von **glCopyTexSubImage1D** können nicht in Anzeigelisten eingeschlossen werden.

> [!Note]  
> Die **glCopyTexSubImage1D-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

Texturierung hat keine Auswirkungen im Farbindexmodus. Die Funktionen [**glPixelStore**](glpixelstore-functions.md) und [**glPixelTransfer**](glpixeltransfer.md) wirken sich auf Texturbilder genau so aus, wie sie sich darauf auswirken, wie Pixel mithilfe von [**glDrawPixels**](gldrawpixels.md)gezeichnet werden.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glCopyTexSubImage1D** ab:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) mit argument GL \_ TEXTURE \_ 1D

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





