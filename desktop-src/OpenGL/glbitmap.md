---
title: glBitmap-Funktion (Gl.h)
description: Die glBitmap-Funktion zeichnet eine Bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- glBitmap-Funktion OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da90b8e592f8cd9d1702c7810990042b3929ef40e70814e8fb7d3326d902cb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082230"
---
# <a name="glbitmap-function"></a>glBitmap-Funktion

Die **glBitmap-Funktion** zeichnet eine Bitmap.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*width* 
</dt> <dd>

Die Pixelbreite des Bitmapbilds.

</dd> <dt>

*height* 
</dt> <dd>

Die Pixelhöhe des Bitmapbilds.

</dd> <dt>

*xorig* 
</dt> <dd>

Die *x-Position* des Ursprungs im Bitmapbild. Der Ursprung wird von der unteren linken Ecke der Bitmap aus gemessen, wobei die Richtungen nach rechts und nach oben die positiven Achsen sind.

</dd> <dt>

*yorig* 
</dt> <dd>

Die *y-Position* des Ursprungs im Bitmapbild. Der Ursprung wird von der unteren linken Ecke der Bitmap aus gemessen, wobei die Richtungen nach rechts und nach oben die positiven Achsen sind.

</dd> <dt>

*Xmove* 
</dt> <dd>

Der  x-Offset, der der aktuellen Rasterposition hinzugefügt werden soll, nachdem die Bitmap gezeichnet wurde.

</dd> <dt>

*ymove* 
</dt> <dd>

Der *y-Offset,* der der aktuellen Rasterposition hinzugefügt werden soll, nachdem die Bitmap gezeichnet wurde.

</dd> <dt>

*Bitmap* 
</dt> <dd>

Die Adresse des Bitmapbilds.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *Breite* oder *Höhe* ist negativ.<br/>                                                                                           |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Eine Bitmap ist ein binäres Bild. Beim Zeichnen wird die Bitmap relativ zur aktuellen Rasterposition positioniert, und Framepufferpixel, die 1s in der Bitmap entsprechen, werden mit der aktuellen Rasterfarbe oder dem aktuellen Rasterindex geschrieben. Framepufferpixel, die Nullen in der Bitmap entsprechen, werden nicht geändert.

Das Bitmapbild wird wie Bilddaten für die [**glDrawPixels-Funktion**](gldrawpixels.md) interpretiert, wobei *Breite* und *Höhe* den Argumenten für Breite und Höhe dieser Funktion entsprechen und der *Typ* auf GL \_ BITMAP und das *Format* auf GL COLOR INDEX festgelegt \_ \_ ist. Modi, die Sie mit [**glPixelStore**](glpixelstore-functions.md) angeben, wirken sich auf die Interpretation von Bitmapbilddaten aus. -Modi, die Sie mit [**glPixelTransfer**](glpixeltransfer.md) angeben, nicht.

Wenn die aktuelle Rasterposition ungültig ist, wird **glBitmap** ignoriert. Andernfalls wird die untere linke Ecke des Bitmapbilds an den folgenden Fensterkoordinaten positioniert:

*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?

*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?

In diesen Koordinaten ist (*x*<sub>r</sub> , *y*<sub>r</sub> ) die Rasterposition und (*x*? , *y*? ) ist der Bitmapursprung. Fragmente werden dann für jedes Pixel generiert, das einer 1 im Bitmapbild entspricht. Diese Fragmente werden mithilfe der aktuellen Raster-Z-Koordinate, des Farb- oder Farbindexes und der aktuellen Rastertexturkoordinaten generiert. Sie werden dann so behandelt, als ob sie von einem Punkt, einer Linie oder einem Polygon generiert worden wären, einschließlich Texturzuordnung, Veralten und aller Vorgänge pro Fragment, z. B. Alpha- und Tiefentests.

Nachdem die Bitmap gezeichnet wurde, werden die *x-* und *y-Koordinaten* der aktuellen Rasterposition durch *xmove* und *ymove* versetzt. Es wird keine Änderung an der z-Koordinate der aktuellen Rasterposition oder an der aktuellen Rasterfarbe, dem aktuellen Index oder den Texturkoordinaten vorgenommen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glBitmap-Funktion** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ RASTER \_ POSITION

 

**glGet** mit dem Argument GL \_ CURRENT \_ RASTER \_ COLOR

 

**glGet** mit argument GL \_ CURRENT \_ RASTER \_ INDEX

 

**glGet** mit dem Argument GL \_ CURRENT RASTER TEXTURE \_ \_ \_ COORDS

 

**glGet** mit argument GL \_ CURRENT RASTER POSITION \_ \_ \_ VALID

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> </dl>

 

 





