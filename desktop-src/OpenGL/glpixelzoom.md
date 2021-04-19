---
title: glpixelzoom-Funktion (GL. h)
description: Die glpixelzoom-Funktion gibt die Pixel Zoomfaktoren an.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- glpixelzoom-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106369924"
---
# <a name="glpixelzoom-function"></a>glpixelzoom-Funktion

Die **glpixelzoom** -Funktion gibt die Pixel Zoomfaktoren an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*xfactor* 
</dt> <dd>

Der *x* -Zoomfaktor für Pixel Schreibvorgänge.

</dd> <dt>

*yfactor* 
</dt> <dd>

Der *y* -Zoomfaktor für Pixel Schreibvorgänge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glpixelzoom** -Funktion gibt Werte für die *x* -und *y* -Zoomfaktoren an. Bei der Ausführung von [**gldrawpixels**](gldrawpixels.md) oder [**glcopypixels**](glcopypixels.md), wenn (*x*<sub>r</sub> ,*y*<sub>r</sub> ) die aktuelle Raster Position ist, und ein angegebenes Element in der *n*-ten Zeile und *m*.-Spalte des Pixel Rechtecks liegt, dann Pixel, deren zentriert im Rechteck mit Ecken

![Gleichung, die die Orte anzeigt, an denen Pixel Kandidaten für die Ersetzung sind.](images/pix05.png)

sind Kandidaten für die Ersetzung. Alle Pixel, deren Mitte am unteren oder linken Rand dieses rechteckigen Bereichs liegt, werden ebenfalls geändert.

Die Pixel Zoomfaktoren sind nicht auf positive Werte beschränkt. Negative Zoomfaktoren spiegeln das resultierende Bild der aktuellen Raster Position wider.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpixelzoom** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Zoom \_ X

**glget** mit dem Argument GL \_ Zoom \_ Y

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

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





