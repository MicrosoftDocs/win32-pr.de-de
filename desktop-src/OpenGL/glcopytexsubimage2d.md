---
title: glCopyTexSubImage2D-Funktion (Gl.h)
description: Die glCopyTexSubImage2D-Funktion kopiert ein Unterbild eines zweidimensionalen Texturbilds aus dem Framepuffer.
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
ms.openlocfilehash: f2a6a5dbf175408ba8421a28e9ee7b7b80876849701b849935a3a4aba9b13e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617056"
---
# <a name="glcopytexsubimage2d-function"></a>glCopyTexSubImage2D-Funktion

Die **glCopyTexSubImage2D-Funktion** kopiert ein Unterbild eines zweidimensionalen Texturbilds aus dem Framepuffer.

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

Das Ziel, in das die Bilddaten geändert werden. Muss den Wert GL \_ TEXTURE \_ 2D aufweisen.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebenennummer. Ebene 0 ist das Basisimage. Ebene *n* ist das *n-te* Mipmap-Reduzierungsbild.

</dd> <dt>

*xoffset* 
</dt> <dd>

Der Texeloffset in *x-Richtung* innerhalb des Texturarrays.

</dd> <dt>

*yoffset* 
</dt> <dd>

Der Texeloffset in *y-Richtung* innerhalb des Texturarrays.

</dd> <dt>

*x* 
</dt> <dd>

Die x-Ebenenkoordinaten des Fensters in der unteren linken Ecke der zu kopierenden Pixelzeile.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Ebenenkoordinaten des Fensters in der unteren linken Ecke der zu kopierenden Pixelzeile.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Unterbilds des Texturbilds. Die Angabe eines Texturunterbilds mit einer Breite von 0 (null) hat keine Auswirkungen.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Unterbilds des Texturbilds. Die Angabe eines Texturunterbilds mit einer Breite von 0 (null) hat keine Auswirkungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* war kein akzeptierter Wert.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *level* war kleiner als 0 (null) oder größer als *Protokoll* 2 (*max),* wobei *max* der zurückgegebene Wert von GL \_ MAX TEXTURE SIZE \_ \_ ist.<br/>                                                                                                                                                                                          |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *xoffset* war kleiner als border *oder* (*xoffset*  +  *width*)was greater than (*w*  +  *border*), *yoffset* was less than *border*, or (*yoffset* height ) was greater than ( h border ), where w is GL TEXTURE WIDTH and  +    +    \_ \_ *border* is GL TEXTURE \_ \_ BORDER. Beachten Sie, *dass w* die doppelte *Rahmenbreite* enthält.<br/> |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *width* war kleiner als *border oder* *y* kleiner als *border,* wobei *border* die Rahmenbreite des Texturarrays ist.<br/>                                                                                                                                                                                           |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Das Texturarray wurde nicht durch einen vorherigen [**glTexImage1D-Vorgang**](glteximage1d.md) definiert.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/>                                                                                                                                                                                       |



## <a name="remarks"></a>Hinweise

Die **glCopyTexSubImage2D-Funktion** ersetzt einen rechteckigen Teil eines zweidimensionalen Texturbilds durch Pixel aus dem aktuellen Framepuffer und nicht aus dem Hauptspeicher, wie es bei [**glTexSubImage2D**](gltexsubimage2d.md)der Fall ist.

Ein Rechteck aus  Pixeln, das mit den x-  und  y-Fensterkoordinaten und mit den Abmessungen Breite und Höhe beginnt, ersetzt den Teil des Texturarrays durch die Indizes *xoffset* bis xoffset + (*width* - 1), mit den Indizes  *yoffset* bis *yoffset* + (*width* - 1) auf der *mipmap-Ebene,* die durch ebene angegeben *wird.* Das Zielrechteck im Texturarray darf keine Texel außerhalb des ursprünglich angegebenen Texturarrays enthalten.

Die **glCopyTexSubImage2D-Funktion** verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glCopyPixels,**](glcopypixels.md)mit der Ausnahme, dass vor der endgültigen Konvertierung der Pixel alle Pixelkomponentenwerte an den Bereich 0,1 geklammert und zur Speicherung im Texturarray in das interne Format der Textur konvertiert \[ \] werden. Die Pixel reihenfolge wird mit niedrigeren *x Koordinaten* bestimmt, die niedrigeren Texturkoordinaten entspricht. Wenn einer der Pixel innerhalb einer angegebenen Zeile des aktuellen Framepuffers außerhalb des Fensters liegt, das dem aktuellen Renderingkontext zugeordnet ist, sind ihre Werte nicht definiert.

Wenn sich eines der Pixel innerhalb des angegebenen Rechtecks des aktuellen Framepuffers außerhalb des Dem aktuellen Renderingkontexts zugeordneten Lesefensters befinden, sind die für diese Pixel erhaltenen Werte nicht definiert. Es wird keine Änderung am *internalFormat-,* *Width-,* *Height-* oder *Border-Parameter* des angegebenen Texturarrays oder an Texelwerten außerhalb des angegebenen Texturunterbilds vorgenommen.

Aufrufe von **glCopyTexSubImage2D können** nicht in Anzeigelisten enthalten sein.

> [!Note]  
> Die **glCopyTexSubImage2D-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

Die Texturierung hat keine Auswirkungen im Farbindexmodus. Die [**Funktionen glPixelStore**](glpixelstore-functions.md) und [**glPixelTransfer**](glpixeltransfer.md) wirken sich genau so auf Texturbilder aus, wie sie sich auf die Art und Weise auswirken, wie Pixel mit [**glDrawPixel gezeichnet werden.**](gldrawpixels.md)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glCopyTexSubImage2D ab:**

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ TEXTURE \_ 2D

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





