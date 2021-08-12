---
title: glRasterPos2d-Funktion (Gl.h)
description: Gibt die Rasterposition für Pixelvorgänge an. | glRasterPos2d-Funktion (Gl.h)
ms.assetid: 3aad4085-8957-433c-8822-765df6278af8
keywords:
- glRasterPos2d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRasterPos2d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0006361f14e166e8407f2d5c5045e1204ce7b3782e59b15c6d4b5daccf022645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614794"
---
# <a name="glrasterpos2d-function"></a>glRasterPos2d-Funktion

Gibt die Rasterposition für Pixelvorgänge an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glRasterPos2d(
   GLdouble x,
   GLdouble y
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Gibt die x-Koordinate für die aktuelle Rasterposition an.

</dd> <dt>

*y* 
</dt> <dd>

Gibt die y-Koordinate für die aktuelle Rasterposition an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

OpenGL behält eine 3D-Position in Fensterkoordinaten bei. Diese Position, die als Rasterposition bezeichnet wird, wird mit Subpixelgenauigkeit beibehalten. Er wird verwendet, um Pixel- und Bitmap-Schreibvorgänge zu positionieren. Siehe [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)und [**glCopyPixels**](glcopypixels.md).

Die aktuelle Rasterposition besteht aus drei Fensterkoordinaten (*x, y, z),* einem Clipkoordinatenwert *w,* einem Augenkoordinatenabstand, einem gültigen Bit und zugeordneten Farbdaten und Texturkoordinaten. Die  w-Koordinate ist eine Clipkoordinate, *da w* nicht auf Fensterkoordinaten projiziert wird. Die [glRasterPos4-Funktion](glrasterpos-functions.md) gibt explizit die Objektkoordinaten *x, y, z* und *w* an. Die glRasterPos3-Funktion gibt die Objektkoordinaten *x, y* und *z* explizit an, während *w* implizit auf 1 festgelegt ist. Die glRasterPos2-Funktion verwendet die Argumentwerte für *x* und *y,* während z und  *w* implizit auf 0 und 1 gesetzt werden.

Die von [glRasterPos](glrasterpos-functions.md) dargestellten Objektkoordinaten werden genau wie die eines [glVertex-Befehls](glvertex-functions.md) behandelt. Sie werden durch die aktuellen Modellansichts- und Projektionsmatrizen transformiert und an die Clippingphase übergeben. Wenn der Scheitelpunkt nicht gecullt wird, wird er projiziert und auf Fensterkoordinaten skaliert, die zur neuen aktuellen Rasterposition werden, und das FLAG GL CURRENT RASTER POSITION VALID wird \_ \_ \_ \_ festgelegt. Wenn der Scheitelpunkt gecullt wird, wird das gültige Bit gefiltert, und die aktuelle Rasterposition und die zugeordneten Farb- und Texturkoordinaten sind nicht definiert.

Die aktuelle Rasterposition enthält auch einige zugeordnete Farbdaten und Texturkoordinaten. Wenn die Beleuchtung aktiviert ist, wird GL CURRENT RASTER COLOR, im RGBA-Modus oder gl CURRENT RASTER INDEX im Farbindexmodus auf die Farbe festgelegt, die von der Beleuchtungsberechnung erzeugt wird \_ \_ \_ \_ \_ \_ (siehe [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)und [**glShadeModel**](glshademodel.md)). Wenn die Beleuchtung deaktiviert ist, wird die aktuelle Farbe (im RGBA-Modus, Die Zustandsvariable GL CURRENT COLOR) oder der Farbindex (im Farbindexmodus, Zustandsvariable \_ GL CURRENT INDEX) verwendet, um die aktuelle Rasterfarbe zu \_ \_ \_ aktualisieren.

Ebenso wird GL CURRENT RASTER TEXTURE COORDS als Funktion von GL CURRENT TEXTURE COORDS aktualisiert, basierend auf der Texturmatrix und den \_ \_ Texturgenerierungsfunktionen \_ \_ \_ \_ \_ (siehe [glTexGen](gltexgen-functions.md)). Schließlich ersetzt der Abstand vom Ursprung des Augenkoordinatensystems zum Scheitelpunkt, der nur von der Modellansichtsmatrix transformiert wird, GL \_ CURRENT \_ RASTER \_ DISTANCE.

Anfänglich ist die aktuelle Rasterposition (0,0,0,1), der aktuelle Rasterabstand ist 0, das gültige Bit wird festgelegt, die zugeordnete RGBA-Farbe ist (1,1,1,1), der zugeordnete Farbindex ist 1 und die zugeordneten Texturkoordinaten sind (0, 0, 0, 1). Im RGBA-Modus ist GL CURRENT RASTER INDEX immer 1. Im Farbindexmodus behält die aktuelle \_ \_ RGBA-Rasterfarbe immer ihren \_ Anfangswert bei.

> [!Note]  
> Die Rasterposition wird sowohl durch [glRasterPos](glrasterpos-functions.md) als auch durch [**glBitmap geändert.**](glbitmap.md)

 

> [!Note]  
> Wenn die Rasterpositionskoordinaten ungültig sind, werden Zeichnungsbefehle, die auf der Rasterposition basieren, ignoriert (d. h., sie führen nicht zu Änderungen am OpenGL-Zustand).

 

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [glRasterPos ab:](glrasterpos-functions.md)

<dl>

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ CURRENT RASTER \_ \_ POSITION  
[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ CURRENT RASTER POSITION \_ \_ \_ VALID  
[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) dem Argument GL \_ CURRENT RASTER \_ \_ DISTANCE  
[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ CURRENT RASTER \_ \_ COLOR  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ RASTER \_ INDEX  
[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ CURRENT RASTER TEXTURE \_ \_ \_ COORDS  
</dl>

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[glLight](gllight-functions.md)
</dt> <dt>

[glLightModel](gllightmodel-functions.md)
</dt> <dt>

[**glShadeModel**](glshademodel.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





