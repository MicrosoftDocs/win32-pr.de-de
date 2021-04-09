---
title: glbitmap-Funktion (GL. h)
description: Die glbitmap-Funktion zeichnet eine Bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- glbitmap-Funktion OpenGL
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
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040714"
---
# <a name="glbitmap-function"></a>glbitmap-Funktion

Die **glbitmap** -Funktion zeichnet eine Bitmap.

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

Die Pixel Breite des Bitmap-Bilds.

</dd> <dt>

*height* 
</dt> <dd>

Die Pixelhöhe des Bitmapbilds.

</dd> <dt>

*xorig* 
</dt> <dd>

Der *x* -Speicherort des Ursprungs im Bitmap-Bild. Der Ursprung wird von der unteren linken Ecke der Bitmap gemessen, wobei die Pfeil nach rechts und nach oben die positiven Achsen bilden.

</dd> <dt>

*yorig* 
</dt> <dd>

Die *y* -Position des Ursprungs im Bitmap-Bild. Der Ursprung wird von der unteren linken Ecke der Bitmap gemessen, wobei die Pfeil nach rechts und nach oben die positiven Achsen bilden.

</dd> <dt>

*xmove* 
</dt> <dd>

Der *x* -Offset, der der aktuellen Raster Position nach dem Zeichnen der Bitmap hinzugefügt werden soll.

</dd> <dt>

*ymove* 
</dt> <dd>

Der *y* -Offset, der der aktuellen Raster Position hinzugefügt werden soll, nachdem die Bitmap gezeichnet wurde.

</dd> <dt>

*Bitmap* 
</dt> <dd>

Die Adresse des Bitmapbilds.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *Breite* oder *Höhe* ist negativ.<br/>                                                                                           |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Eine Bitmap ist ein binäres Bild. Wenn Sie gezeichnet wird, wird die Bitmap relativ zur aktuellen Raster Position positioniert, und die in der Bitmap entsprechenden Frame Puffer Pixel werden mit der aktuellen Raster Farbe oder dem aktuellen Index geschrieben. Frame-Puffer Pixel, die Nullen in der Bitmap entsprechen, werden nicht geändert.

Das Bitmap-Bild wird wie Bilddaten für die Funktion " [**gldrawpixels**](gldrawpixels.md) " interpretiert, wobei " *Width* " und " *height* " den breiten-und Höhen Argumenten dieser Funktion entsprechen und der *Typ* auf die GL- \_ Bitmap und das *Format* auf "GL \_ Color Index" festgelegt ist \_ . Modi, die Sie mithilfe von [**glpixelstore**](glpixelstore-functions.md) angeben, wirken sich auf die Interpretation von Bitmap-Bilddaten aus der Modus, den Sie mit [**glpixeltransfer**](glpixeltransfer.md) angeben, ist nicht.

Wenn die aktuelle Raster Position ungültig ist, wird **glbitmap** ignoriert. Andernfalls wird die linke untere Ecke des Bitmap-Bilds an den folgenden Fenster Koordinaten positioniert:

*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?

*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?

In diesen Koordinaten ist (*x*<sub>r</sub> , *y*<sub>r</sub> ) die Raster Position, und (*x*? , *y*? ) ist der bitmapursprung. Fragmente werden dann für jedes Pixel generiert, das einem 1 im Bitmap-Bild entspricht. Diese Fragmente werden mithilfe der aktuellen Raster- *z*-Koordinate, des Farb-oder Farb Index und der aktuellen Rastertextur Koordinaten generiert. Sie werden dann genauso behandelt, als würden Sie von einem Punkt, einer Linie oder einem Polygon generiert werden, einschließlich Textur Zuordnung, Fogging und sämtlicher Vorgänge pro Fragment, z. b. Alpha-und tiefen Tests.

Nachdem die Bitmap gezeichnet wurde, werden die *x* -und *y* -Koordinaten der aktuellen Raster Position durch *xmove* und *ymove* versetzt. An der *z*-Koordinate der aktuellen Raster Position oder an der aktuellen Raster Farbe, dem Index oder den Texturkoordinaten wird keine Änderung vorgenommen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glbitmap** " ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ aktuelle \_ Raster \_ Position

 

**glget** mit dem Argument GL \_ aktuelle \_ Raster \_ Farbe

 

**glget** mit dem Argument GL \_ Current \_ Raster \_ Index

 

**glget** mit dem Argument GL \_ Current \_ Raster \_ Textur \_ CoOrds

 

**glget** mit dem Argument GL \_ aktuelle \_ Raster \_ Position \_ gültig

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

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> </dl>

 

 





