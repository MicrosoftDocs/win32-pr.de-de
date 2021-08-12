---
title: glCopyTexImage2D-Funktion (Gl.h)
description: Die glCopyTexImage2D-Funktion kopiert Pixel aus dem Framepuffer in ein zweidimensionales Texturbild.
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- glCopyTexImage2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e91481e94d247f5572ac2a65093c4af825c720200aee6daf3e429fad2a70886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617213"
---
# <a name="glcopyteximage2d-function"></a>glCopyTexImage2D-Funktion

Die **glCopyTexImage2D-Funktion** kopiert Pixel aus dem Framepuffer in ein zweidimensionales Texturbild.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
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

*internalFormat* 
</dt> <dd>

Das interne Format und die Auflösung der Texturdaten. Die Werte 1, 2, 3 und 4 werden für *internalFormat nicht akzeptiert.* Der -Parameter kann einen der folgenden symbolischen Werte annehmen.



| Konstante                 | R-Bits | G Bits | B Bits | Ein Bits | L Bits | I Bits |
|--------------------------|--------|--------|--------|--------|--------|--------|
| GL \_ ALPHA                |        |        |        |        |        |        |
| GL \_ ALPHA4               |        |        |        | 4      |        |        |
| GL \_ ALPHA8               |        |        |        | 8      |        |        |
| GL \_ ALPHA12              |        |        |        | 12     |        |        |
| GL \_ ALPHA16              |        |        |        | 16     |        |        |
| GL \_ LUDOMINANZ            |        |        |        |        |        |        |
| GL \_ LUDOMINANZ4           |        |        |        |        | 4      |        |
| GL \_ LUDOMINANZ8           |        |        |        |        | 8      |        |
| GL \_ LUMINANCE12          |        |        |        |        | 12     |        |
| GL \_ LUDOMINANZ16          |        |        |        |        | 16     |        |
| GL \_ LUDOMINANZ \_ ALPHA     |        |        |        |        |        |        |
| GL \_ LUDOMINANZ4 \_ ALPHA4   |        |        |        | 4      | 4      |        |
| GL \_ LUDOMINANZ6 \_ ALPHA2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ ALPHA4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| \_GL-INTENSITÄT            |        |        |        |        |        |        |
| \_GL-INTENSITÄT4           |        |        |        |        |        | 4      |
| \_GL-INTENSITÄT8           |        |        |        |        |        | 8      |
| \_GL-INTENSITÄT12          |        |        |        |        |        | 12     |
| \_GL-INTENSITÄT16          |        |        |        |        |        | 16     |
| GL \_ RGB                  |        |        |        |        |        |        |
| GL \_ R3 \_ G3 \_ B2           | 3      | 3      | 2      |        |        |        |
| GL \_ RGB4                 | 4      | 4      | 4      |        |        |        |
| GL \_ RGB5                 | 5      | 5      | 5      |        |        |        |
| GL \_ RGB8                 | 8      | 8      | 8      |        |        |        |
| GL \_ RGB10                | 10     | 10     | 10     |        |        |        |
| GL \_ RGB12                | 12     | 12     | 12     |        |        |        |
| GL \_ RGB16                | 16     | 16     | 16     |        |        |        |
| GL \_ RGBA                 |        |        |        |        |        |        |
| GL \_ RGBA2                | 2      | 2      | 2      | 2      |        |        |
| GL \_ RGBA4                | 4      | 4      | 4      | 4      |        |        |
| GL \_ RGB5 \_ A1             | 5      | 5      | 5      | 1      |        |        |
| GL \_ RGBA8                | 8      | 8      | 8      | 8      |        |        |
| GL \_ RGB10 \_ A2            | 10     | 10     | 10     | 2      |        |        |
| GL \_ RGBA12               | 12     | 12     | 12     | 12     |        |        |
| GL \_ RGBA16               | 16     | 16     | 16     | 16     |        |        |



 

</dd> <dt>

*x* 
</dt> <dd>

Die x-Ebenenkoordinate des Fensters der unteren linken Ecke des rechteckigen Bereichs der zu kopierenden Pixel.

</dd> <dt>

*y* 
</dt> <dd>

Die Fensterkoordinate der linken unteren Ecke des rechteckigen Bereichs der zu kopierenden Pixel.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Texturbilds. Muss 2n + 2 \* *Rahmen* für eine ganze Zahl *n sein.*

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Texturbilds. Muss 2n + 2 \* *Rahmen* für eine ganze Zahl *n sein.*

</dd> <dt>

*Grenze* 
</dt> <dd>

Die Breite des Rahmens. Muss entweder 0 (null) oder 1 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* war kein akzeptierter Wert.<br/>                                                                                                               |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *level* war kleiner als 0 (null) oder größer als log2 *max,* wobei *max* der zurückgegebene Wert von GL \_ MAX TEXTURE SIZE \_ \_ ist.<br/>                               |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *border* war nicht null oder 1.<br/>                                                                                                                       |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *width* war kleiner als 0 (null), größer als 2 + GL \_ MAX TEXTURE \_ \_ SIZE, oder die *Breite* kann nicht als 2n + 2 \* *Rahmen* für eine ganze Zahl *n* dargestellt werden.<br/> |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                        |



## <a name="remarks"></a>Hinweise

Die **glCopyTexImage2D-Funktion** definiert ein zweidimensionales Texturbild mitHilfe von Pixeln aus dem aktuellen Framepuffer und nicht aus dem Hauptspeicher, wie dies bei [**glTexImage2D**](glteximage2d.md)der Fall ist.

Unter Verwendung der mit *der Ebene* angegebenen Mipmapebene werden Texturarrays als Rechteck von Pixeln mit der unteren linken Ecke an den Koordinaten *x* und *y,* Breite gleich *Breite* + (2 \* *Rahmen)* und Höhe gleich *Höhe* + (2 \* *Rahmen)* definiert. Das interne Format des Texturarrays wird mit dem *internalFormat-Parameter* angegeben.

Die **glCopyTexImage2D-Funktion** verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glCopyPixels,**](glcopypixels.md) mit der Ausnahme, dass vor der endgültigen Konvertierung der Pixel alle Pixelkomponentenwerte an den Bereich \[ 0,1 angeklammern und in das interne Format der Textur für die Speicherung im \] Texturarray konvertiert werden. Die Pixelreihenfolge wird mit niedrigeren *x-* und *y-Koordinaten* bestimmt, die niedrigeren *s-* und t-Texturkoordinaten entsprechen.  Wenn sich eines der Pixel innerhalb einer angegebenen Zeile des aktuellen Framepuffers außerhalb des Fensters befindet, das dem aktuellen Renderingkontext zugeordnet ist, sind deren Werte nicht definiert.

Aufrufe von **glCopyTexImage2D** können nicht in Anzeigelisten eingeschlossen werden.

> [!Note]  
> Die **glCopyTexImage2D-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

Texturierung hat keine Auswirkungen im Farbindexmodus. Die Funktionen [**glPixelStore**](glpixelstore-functions.md) und [**glPixelTransfer**](glpixeltransfer.md) wirken sich auf Texturbilder genau so aus, wie sie sich auf [**glDrawPixels**](gldrawpixels.md)auswirken.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glCopyTexImage2D** ab:

[**glIsEnabled**](glisenabled.md) mit argument GL \_ TEXTURE \_ 2D

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

[**glCopyTexImage1D**](glcopyteximage1d.md)
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

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





