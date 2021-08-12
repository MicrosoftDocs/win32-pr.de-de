---
title: glRasterPos4s-Funktion (Gl.h)
description: Gibt die Rasterposition für Pixelvorgänge an. | glRasterPos4s-Funktion (Gl.h)
ms.assetid: 60e6ced4-a542-4189-a3da-eed36f81cafb
keywords:
- glRasterPos4s-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRasterPos4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d46eba3121f28fcab3eb256c038e4dd2b18d27c7537a92bd76b33f641f761
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614596"
---
# <a name="glrasterpos4s-function"></a>glRasterPos4s-Funktion

Gibt die Rasterposition für Pixelvorgänge an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glRasterPos4s(
   GLshort x,
   GLshort y,
   GLshort z,
   GLshort w
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

</dd> <dt>

*Z* 
</dt> <dd>

Gibt die Z-Koordinate für die aktuelle Rasterposition an.

</dd> <dt>

*w* 
</dt> <dd>

Die w-Koordinate für die aktuelle Rasterposition.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

OpenGL verwaltet eine 3D-Position in Fensterkoordinaten. Diese Position, die als Rasterposition bezeichnet wird, wird mit Subpixelgenauigkeit beibehalten. Es wird verwendet, um Pixel- und Bitmapschreibvorgänge zu positionieren. Siehe [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)und [**glCopyPixels**](glcopypixels.md).

Die aktuelle Rasterposition besteht aus drei Fensterkoordinaten (*x, y, z*), einem Clipkoordinaten *w-Wert,* einem Augenkoordinatenabstand, einem gültigen Bit und zugeordneten Farbdaten und Texturkoordinaten. Die w-Koordinate ist eine Clipkoordinate, da *w* nicht auf Fensterkoordinaten projiziert wird.  Die [glRasterPos4-Funktion](glrasterpos-functions.md) gibt explizit die Objektkoordinaten *x, y, z* und *w* an. Die glRasterPos3-Funktion gibt die Objektkoordinaten *x, y* und *z* explizit an, während *w* implizit auf eins festgelegt ist. Die glRasterPos2-Funktion verwendet die Argumentwerte für *x* und *y,* während *z* und *w* implizit auf 0 und eins festgelegt werden.

Die von [glRasterPos](glrasterpos-functions.md) dargestellten Objektkoordinaten werden wie die eines [glVertex-Befehls](glvertex-functions.md) behandelt. Sie werden durch die aktuelle Modellansicht und Projektionsmatrizen transformiert und an die Clippingphase übergeben. Wenn der Scheitelpunkt nicht gekäutert wird, wird er projiziert und auf Fensterkoordinaten skaliert, die zur neuen aktuellen Rasterposition werden, und das \_ GL CURRENT RASTER POSITION \_ \_ \_ VALID-Flag wird festgelegt. Wenn der Scheitelpunkt gekäutert wird, wird das gültige Bit gelöscht, und die aktuelle Rasterposition und die zugehörigen Farb- und Texturkoordinaten sind nicht definiert.

Die aktuelle Rasterposition enthält auch einige zugeordnete Farbdaten und Texturkoordinaten. Wenn die Beleuchtung aktiviert ist, wird GL \_ CURRENT RASTER COLOR im \_ \_ RGBA-Modus oder gl \_ CURRENT RASTER INDEX im \_ \_ Farbindexmodus auf die Farbe festgelegt, die durch die Beleuchtungsberechnung erzeugt wird (siehe [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)und [**glShadeModel**](glshademodel.md)). Wenn die Beleuchtung deaktiviert ist, wird die aktuelle Farbe (im RGBA-Modus, zustandsvariable GL CURRENT COLOR) oder der \_ \_ Farbindex (im Farbindexmodus, Zustandsvariable GL \_ CURRENT \_ INDEX) verwendet, um die aktuelle Rasterfarbe zu aktualisieren.

Ebenso wird GL \_ CURRENT \_ RASTER TEXTURE \_ \_ COORDS als Funktion von GL \_ CURRENT TEXTURE \_ \_ COORDS basierend auf der Texturmatrix und den Texturgenerierungsfunktionen aktualisiert (siehe [glTexGen](gltexgen-functions.md)). Schließlich ersetzt der Abstand vom Ursprung des Augenkoordinatensystems zum Scheitelpunkt, der nur durch die Modellansichtsmatrix transformiert wird, GL \_ CURRENT \_ RASTER \_ DISTANCE.

Anfänglich ist die aktuelle Rasterposition (0,0,0,1), der aktuelle Rasterabstand ist 0, das gültige Bit wird festgelegt, die zugeordnete RGBA-Farbe ist (1,1,1,1), der zugeordnete Farbindex ist 1, und die zugeordneten Texturkoordinaten sind (0, 0, 0, 1). Im RGBA-Modus ist GL \_ CURRENT RASTER INDEX immer \_ \_ 1. Im Farbindexmodus behält die aktuelle Raster-RGBA-Farbe immer ihren Anfangswert bei.

> [!Note]  
> Die Rasterposition wird sowohl durch [glRasterPos](glrasterpos-functions.md) als auch durch [**glBitmap**](glbitmap.md)geändert.

 

> [!Note]  
> Wenn die Rasterpositionskoordinaten ungültig sind, werden Zeichnungsbefehle, die auf der Rasterposition basieren, ignoriert (d.b. sie führen nicht zu Änderungen am OpenGL-Zustand).

 

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [glRasterPos](glrasterpos-functions.md)ab:

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ RASTER \_ POSITION  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT RASTER POSITION \_ \_ \_ VALID  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ RASTER \_ DISTANCE  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ CURRENT \_ RASTER \_ COLOR  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ RASTER \_ INDEX  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ CURRENT RASTER TEXTURE \_ \_ \_ COORDS  
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

 

 





