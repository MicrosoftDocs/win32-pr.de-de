---
title: glCopyTexImage1D-Funktion (GL. h)
description: Die glCopyTexImage1D-Funktion kopiert Pixel aus dem Frame Puffer in ein eindimensionales Textur Bild.
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
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340349"
---
# <a name="glcopyteximage1d-function"></a>glCopyTexImage1D-Funktion

Die **glCopyTexImage1D** -Funktion kopiert Pixel aus dem Frame Puffer in ein eindimensionales Textur Bild.

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

Das Ziel, für das die Bilddaten geändert werden. Muss den Wert "GL \_ Texture \_ 1D" aufweisen.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebene. Ebene 0 ist das Basis Image. Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.

</dd> <dt>

*internalformat* 
</dt> <dd>

Das interne Format und die Auflösung der Textur Daten. Dieser Parameter muss einen der folgenden symbolischen Werte aufweisen.



| Konstante                 | R-Bits | G Bits | B Bits | Eine Bits | L Bits | I Bits |
|--------------------------|--------|--------|--------|--------|--------|--------|
| GL- \_ Alpha                |        |        |        |        |        |        |
| GL \_ ALPHA4               |        |        |        | 4      |        |        |
| GL \_ ALPHA8               |        |        |        | 8      |        |        |
| GL \_ ALPHA12              |        |        |        | 12     |        |        |
| GL \_ ALPHA16              |        |        |        | 16     |        |        |
| GL- \_ Beleuchtung            |        |        |        |        |        |        |
| GL \_ LUMINANCE4           |        |        |        |        | 4      |        |
| GL \_ LUMINANCE8           |        |        |        |        | 8      |        |
| GL \_ LUMINANCE12          |        |        |        |        | 12     |        |
| GL \_ LUMINANCE16          |        |        |        |        | 16     |        |
| GL- \_ Leuchtkraft \_ Alpha     |        |        |        |        |        |        |
| GL \_ LUMINANCE4 \_ ALPHA4   |        |        |        | 4      | 4      |        |
| GL \_ LUMINANCE6 \_ ALPHA2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ ALPHA4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| GL- \_ Intensität            |        |        |        |        |        |        |
| GL \_ INTENSITY4           |        |        |        |        |        | 4      |
| GL \_ INTENSITY8           |        |        |        |        |        | 8      |
| GL \_ INTENSITY12          |        |        |        |        |        | 12     |
| GL \_ INTENSITY16          |        |        |        |        |        | 16     |
| GL. \_ RGB                  |        |        |        |        |        |        |
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
| GL \_ RGB5 \_ a1             | 5      | 5      | 5      | 1      |        |        |
| GL \_ RGBA8                | 8      | 8      | 8      | 8      |        |        |
| GL \_ RGB10 \_ a2            | 10     | 10     | 10     | 2      |        |        |
| GL \_ RGBA12               | 12     | 12     | 12     | 12     |        |        |
| GL \_ RGBA16               | 16     | 16     | 16     | 16     |        |        |



 

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

Die Breite des Textur Bilds. Muss NULL oder 2N + 2 (*Border*) für eine ganze Zahl *n* sein. Die Höhe des Textur Bilds ist 1.

</dd> <dt>

*Aun* 
</dt> <dd>

Die Breite des Rahmens. Muss entweder NULL oder 1 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Ziel* war kein akzeptierter Wert.<br/>                                                                                                           |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Ebene* war kleiner als 0 (null) oder größer als log2 *Max*, wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size ist.<br/>                           |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | der *Rahmen war nicht* 0 (null) oder 1.<br/>                                                                                                                   |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *Breite* war kleiner als 0 (null), größer als 2 + gl \_ Maximale \_ Textur \_ Größe, oder *Breite* kann nicht als 2n + (*Border*) für eine Ganzzahl *n* dargestellt werden.<br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                    |



## <a name="remarks"></a>Bemerkungen

Die **glCopyTexImage1D** -Funktion definiert ein eindimensionales Textur Bild mithilfe von Pixel aus dem aktuellen Framebuffer, nicht aus dem Hauptspeicher, wie es bei [**glTexImage1D**](glteximage1d.md)der Fall ist.

Mithilfe der mit *Level* angegebenen MipMap-Ebene werden Textur Arrays als Pixel Zeile definiert, die an der unteren linken Ecke des Fensters an den durch *x* und *y* angegebenen Koordinaten ausgerichtet ist, wobei die Länge gleich dem Rahmen der *Breite* + 2 ist \* . Das interne Format des Textur Arrays wird mit dem *internalformat* -Parameter angegeben.

Die **glCopyTexImage1D** -Funktion verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glcopypixels**](glcopypixels.md), mit dem Unterschied, dass vor der abschließenden Konvertierung der Pixel alle Pixel Komponenten Werte an den Bereich \[ 0, 1 gebunden und in das \] interne Format der Textur für die Speicherung im Textur Array konvertiert werden. Die Pixel Reihenfolge wird mit niedrigeren *x* -Koordinaten bestimmt, die den unteren Texturkoordinaten entsprechen. Wenn eine der Pixel innerhalb einer angegebenen Zeile des aktuellen Frame Puffer außerhalb des Fensters liegt, das dem aktuellen renderingkontext zugeordnet ist, sind ihre Werte nicht definiert.

Sie können **glCopyTexImage1D** -Aufrufe nicht in Anzeigelisten einschließen.

> [!Note]  
> Die **glCopyTexImage1D** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

Die Texturierung hat keine Auswirkung auf den Farb Index Modus. Die Funktionen " [**glpixelstore**](glpixelstore-functions.md) " und " [**glpixeltransfer**](glpixeltransfer.md) " wirken sich auf Textur Bilder genau so aus, wie Sie sich auf [**gldrawpixels**](gldrawpixels.md)auswirken

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glCopyTexImage1D** ab:

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

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
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

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





