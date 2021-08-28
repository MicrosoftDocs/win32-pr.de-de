---
title: gluEndSurface-Funktion (Glu.h)
description: Die Funktionen gluBeginSurface und gluEndSurface begrenzen eine Non-Uniform Rational B-Spline (NURBS)-Oberflächendefinition. | gluEndSurface-Funktion (Glu.h)
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
keywords:
- gluEndSurface-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluEndSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32c8fb5165be78032429dce7957cd0975753515d55969b04415c61be2a7dc5ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675370"
---
# <a name="gluendsurface-function"></a>gluEndSurface-Funktion

Die [**Funktionen gluBeginSurface**](glubeginsurface.md) und **gluEndSurface** begrenzen eine nicht einheitliche rationale B-Spline-Oberflächendefinition [(NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluEndSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**Funktionen gluBeginSurface**](glubeginsurface.md) und **gluEndSurface** markieren den Anfang und das Ende von NURBS-Oberflächendefinitionen, die mit Aufrufen von **gluNurbsSurface definiert werden.**

1.  Rufen **Sie gluBeginSurface auf,** um den Anfang einer NURBS-Oberflächendefinition zu markieren.
2.  Führen Sie mindestens einen Aufruf von **gluNurbsSurface durch,** um die Attribute der Oberfläche zu definieren.

    Genau einer dieser Aufrufe von **gluNurbsSurface** muss den Oberflächentyp GL \_ MAP2 \_ VERTEX 3 oder \_ GL \_ MAP2 \_ VERTEX \_ 4 haben.

3.  Um das Ende der NURBS-Oberflächendefinition zu markieren, rufen Sie **gluEndSurface auf.**

Die [**Funktionen gluBeginTrim,**](glubegintrim.md) [**gluPwlCurve,**](glupwlcurve.md) [**gluNurbsCurve**](glunurbscurve.md)und **gluEndTrim** unterstützen das Kürzen von NURBS-Oberflächen.

Verwenden Sie OpenGL-Auswertungen, um die NURBS-Oberfläche als Gruppe von Polygonen zu rendern. Behalten Sie den Auswertungszustand während des Renderings [**mit glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) und [**glPopAttrib bei.**](glpopattrib.md)

## <a name="examples"></a>Beispiele

Die folgenden Funktionen rendern eine texturierte NURBS-Oberfläche mit Normals. Die Texturkoordinaten und -normaler werden auch als NURBS-Oberflächen beschrieben:

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluNurbsSurface**](glunurbssurface.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





