---
title: gluBeginCurve-Funktion (Glu.h)
description: Die Funktionen gluBeginCurve und gluEndCurve begrenzen eine Non-Uniform Rational B-Spline(NURBS)-Kurvendefinition. | gluBeginCurve-Funktion (Glu.h)
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- OpenGL-Funktion "gluBeginCurve"
topic_type:
- apiref
api_name:
- gluBeginCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 171c6ce95acf7592fcb2c3badccfeb9f2c5d68413f963f7b5043ec63502ee720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489740"
---
# <a name="glubegincurve-function"></a>gluBeginCurve-Funktion

Die **Funktionen gluBeginCurve** und [**gluEndCurve**](gluendcurve.md) begrenzen eine nicht einheitliche rationale B-Spline-Kurvendefinition [(NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluBeginCurve(
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

Verwenden **Sie gluBeginCurve,** um den Anfang einer NURBS-Kurvendefinition zu markieren. Führen Sie nach dem Aufruf von **gluBeginCurve** mindestens einen Aufruf von [**gluNurbsCurve**](glunurbscurve.md) durch, um die Attribute der Kurve zu definieren. Genau einer der Aufrufe von **gluNurbsCurve** muss den Kurventyp GL \_ MAP1 \_ VERTEX \_ 3 oder GL \_ MAP1 \_ VERTEX \_ 4 haben. Um das Ende der NURBS-Kurvendefinition zu markieren, rufen Sie [**gluEndCurve auf.**](gluendcurve.md)

OpenGL-Auswertungen werden verwendet, um die NURBS-Kurve als eine Reihe von Liniensegmenten zu rendern. Der Auswertungszustand wird während des Renderings mit [**glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) und [**glPopAttrib beibehalten.**](glpopattrib.md) Informationen dazu, welchen Zustand diese Aufrufe beibehalten, finden Sie unter **glPushAttrib**.

## <a name="examples"></a>Beispiele

Die folgenden Funktionen rendern eine texturierte NURBS-Kurve mit Normals. Texturkoordinaten und Normals werden auch als NURBS-Kurven angegeben:

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
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

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





