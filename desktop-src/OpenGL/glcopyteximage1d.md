---
title: glCopyTexImage1D-Funktion (Gl.h)
description: Die glCopyTexImage1D-Funktion kopiert Pixel aus dem Framepuffer in ein eindimensionales Texturbild.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- glCopyTexImage1D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e3dd966aa08eb5c74fa15235ed51f07a671c4e6f1378a990c6686fdc801e1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617348"
---
# <a name="glcopyteximage1d-function"></a>glCopyTexImage1D-Funktion

Die **glCopyTexImage1D-Funktion** kopiert Pixel aus dem Framepuffer in ein eindimensionales Texturbild.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Das Ziel, für das die Bilddaten geändert werden. Muss den Wert GL \_ TEXTURE \_ 1D aufweisen.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebenennummer. Ebene 0 ist das Basisimage. Ebene *n* ist das Bild der *n-ten* Mipmapverringerung.

</dd> <dt>

*internalFormat* 
</dt> <dd>

Das interne Format und die Auflösung der Texturdaten. Dieser Parameter muss einer der folgenden symbolischen Werte sein.



| Konstante                 | R-Bits | G Bits | B-Bits | A Bits | L-Bits | I Bits |
|--------------------------|--------|--------|--------|--------|--------|--------|
| GL \_ ALPHA                |        |        |        |        |        |        |
| GL \_ ALPHA4               |        |        |        | 4      |        |        |
| GL \_ ALPHA8               |        |        |        | 8      |        |        |
| GL \_ ALPHA12              |        |        |        | 12     |        |        |
| GL \_ ALPHA16              |        |        |        | 16     |        |        |
| GL \_ LUMINANCE            |        |        |        |        |        |        |
| GL \_ LUMINANCE4           |        |        |        |        | 4      |        |
| GL \_ LUMINANCE8           |        |        |        |        | 8      |        |
| GL \_ LUMINANCE12          |        |        |        |        | 12     |        |
| GL \_ LUMINANCE16          |        |        |        |        | 16     |        |
| GL \_ LUMINANCE \_ ALPHA     |        |        |        |        |        |        |
| GL \_ LUMINANCE4 \_ ALPHA4   |        |        |        | 4      | 4      |        |
| GL \_ LUMINANCE6 \_ ALPHA2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ ALPHA4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| \_GL-INTENSITÄT            |        |        |        |        |        |        |
| GL \_ INTENSITY4           |        |        |        |        |        | 4      |
| GL \_ INTENSITY8           |        |        |        |        |        | 8      |
| GL \_ INTENSITY12          |        |        |        |        |        | 12     |
| GL \_ INTENSITY16          |        |        |        |        |        | 16     |
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

Die X-Ebenenkoordinate des Fensters in der unteren linken Ecke der zu kopierenden Pixelzeile.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Ebenenkoordinate des Fensters in der unteren linken Ecke der zu kopierenden Pixelzeile.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Texturbilds. Muss 0 oder 2n + 2(*Rahmen*) für eine ganze Zahl *n sein.* Die Höhe des Texturbilds ist 1.

</dd> <dt>

*Grenze* 
</dt> <dd>

Die Breite des Rahmens. Muss entweder 0 (null) oder 1 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* war kein akzeptierter Wert.<br/>                                                                                                           |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *level* war kleiner als 0 (null) oder größer als log2 *max,* wobei *max* der zurückgegebene Wert von GL \_ MAX TEXTURE SIZE \_ \_ ist.<br/>                           |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *border* war nicht 0 (null) oder 1.<br/>                                                                                                                   |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *width* war kleiner als 0 (null), größer als 2 + GL MAX TEXTURE SIZE, oder die Breite kann nicht als \_ \_ \_ 2n +(*Rahmen*) für  eine ganze Zahl *n dargestellt werden.*<br/> |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/>                    |



## <a name="remarks"></a>Hinweise

Die **glCopyTexImage1D-Funktion** definiert ein eindimensionales Texturbild mit Pixeln aus dem aktuellen Framepuffer und nicht aus dem Hauptspeicher, wie es bei [**glTexImage1D**](glteximage1d.md)der Fall ist.

Mithilfe der Mipmapebene, die mit level angegeben *wird,* werden Texturarrays als Pixelzeile definiert, die an der unteren linken Ecke des Fensters an den von *x* und *y* angegebenen Koordinaten ausgerichtet ist, mit einer Länge, die der Breite *+* 2 Rahmen \* entspricht. Das interne Format des Texturarrays wird mit dem *internalFormat-Parameter* angegeben.

Die **glCopyTexImage1D-Funktion** verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glCopyPixels,**](glcopypixels.md)mit der Ausnahme, dass vor der endgültigen Konvertierung der Pixel alle Pixelkomponentenwerte an den Bereich 0,1 geklammert und in das interne Format der Textur für die Speicherung im Texturarray konvertiert \[ \] werden. Die Pixel reihenfolge wird mit niedrigeren *x Koordinaten* bestimmt, die niedrigeren Texturkoordinaten entspricht. Wenn einer der Pixel innerhalb einer angegebenen Zeile des aktuellen Framepuffers außerhalb des Fensters liegt, das dem aktuellen Renderingkontext zugeordnet ist, sind ihre Werte nicht definiert.

Aufrufe von **glCopyTexImage1D können nicht** in Anzeigelisten enthalten sein.

> [!Note]  
> Die **glCopyTexImage1D-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

Die Texturierung hat keine Auswirkungen im Farbindexmodus. Die [**Funktionen glPixelStore**](glpixelstore-functions.md) und [**glPixelTransfer**](glpixeltransfer.md) wirken sich genau so auf Texturbilder aus, wie sie [**glDrawPixels beeinflussen.**](gldrawpixels.md)

Die folgende Funktion ruft Informationen im Zusammenhang mit **glCopyTexImage1D ab:**

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ TEXTURE \_ 1D

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
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

 

 





