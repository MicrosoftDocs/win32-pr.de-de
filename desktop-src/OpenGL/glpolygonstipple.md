---
title: glpolygonstippel-Funktion (GL. h)
description: Die glpolygonstippel-Funktion legt das Polygon-stippling-Muster fest.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- glpolygonstippel-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477235"
---
# <a name="glpolygonstipple-function"></a>glpolygonstippel-Funktion

Die **glpolygonstippel** -Funktion legt das Polygon-stippling-Muster fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mask* 
</dt> <dd>

Ein Zeiger auf ein 32x32-stippingmuster, das aus dem Arbeitsspeicher auf die gleiche Weise entpackt wird, wie " [**gldrawpixels**](gldrawpixels.md) " Pixel entpackt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glpolygonstippel** -Funktion legt das Polygon-stippling-Muster fest. Beim Polygon-stippling, wie z. b. Zeilen stippling (siehe [**glLineStipple**](gllinestipple.md)), werden bestimmte Fragmente maskiert, die von rasterization erzeugt werden, und ein Muster erstellt. Stippling ist unabhängig vom Polygon-Antialiasing.

Der *Mask* -Parameter ist ein Zeiger auf ein 32 x 32-stippingmuster, das im Arbeitsspeicher gespeichert ist, genau wie die Pixeldaten, die für **gldrawpixels** bereitgestellt werden, wobei *Höhe* und *Breite* gleich 32, ein Pixel *Format* des GL \_ \_ -Farb Indexes und der *Datentyp* von GL \_ Bitmap sind. Das Stippel Muster wird also als 32 x 32-Array von 1-Bit-Farbindizes dargestellt, die in nicht signierten Bytes verpackt sind. Die Parameter der [**glpixelstore**](glpixelstore-functions.md) -Funktion, wie z. b. gl \_ unpack \_ Swap \_ Bytes und GL \_ unpack \_ lsb \_ First, wirken sich auf die Zusammenstellung der Bits in ein Stippel Muster aus. Pixel Übertragungs Vorgänge (Shift, Offset und Pixel Map) werden jedoch nicht auf das Stippel Bild angewendet.

Der Polygon-stippling ist mit " [**glEnable**](glenable.md) " und " **gldeaktivieren**" aktiviert und deaktiviert \_ \_ Wenn diese Option aktiviert ist, wird ein rasterisiertes Polygon Fragment mit den Fenster Koordinaten *x*<sub>w</sub> und *y*<sub>w</sub> nur dann an die nächste Stufe von OpenGL gesendet, wenn das (*x*<sub>w</sub> mod 32) Th-Bit in der (*y*<sub>w</sub> mod 32) Th-Zeile des stippingmusters 1 ist. Wenn das Polygon-stippling deaktiviert ist, ist es so, als ob es sich um ein stippingmuster handelt.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpolygonstiple** ab:

[**glgetpolygonstippel**](glgetpolygonstipple.md)

[**glisenabled**](glisenabled.md) mit Argument GL \_ Polygon \_ Stippel

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

[**gllinestippel**](gllinestipple.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> </dl>

 

 





