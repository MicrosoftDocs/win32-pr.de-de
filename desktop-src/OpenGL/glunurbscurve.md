---
title: gluNurbsCurve-Funktion (Glu.h)
description: Die gluNurbsCurve-Funktion definiert die Form einer non-Uniform Rational B-Spline (NURBS)-Kurve.
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- gluNurbsCurve-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5973ce3cb4d1ac05ea353fd78359f6b3b1bc9a3a0ab3180807b0834cc4bb20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489040"
---
# <a name="glunurbscurve-function"></a>gluNurbsCurve-Funktion

Die **gluNurbsCurve-Funktion** definiert die Form einer nicht einheitlichen rationalen B-Spline-Kurve [(NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*nknots* 
</dt> <dd>

Die Anzahl der 4000 *000 000 000 000 0* Der *nknots-Parameter* entspricht der Anzahl der Kontrollpunkte plus der Reihenfolge.

</dd> <dt>

*Knoten* 
</dt> <dd>

Ein Array von *nknots* nicht dekrementierenden Werten.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Offset (als Anzahl von Gleitkommawerten mit einzelner Genauigkeit) zwischen aufeinander folgenden Kurvenkontrollpunkten.

</dd> <dt>

*CTLARRAY* 
</dt> <dd>

Ein Zeiger auf ein Array von Kontrollpunkten. Die Koordinaten müssen dem Typ *zustimmen.*

</dd> <dt>

*order* 
</dt> <dd>

Die Reihenfolge der NURBS-Kurve. Der *Order-Parameter* entspricht Degree + 1; daher hat eine kubische Kurve eine Reihenfolge von 4.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Kurve. Wenn diese Kurve innerhalb eines [**gluBeginCurve-gluEndCurve-Paars**](glubegincurve.md)definiert ist, kann der Typ einer der gültigen eindimensionalen Auswertungstypen sein (z. B. / [](gluendcurve.md) GL \_ MAP1 \_ VERTEX 3 oder \_ GL \_ MAP1 COLOR \_ \_ 4). Zwischen einem gluBeginTrim-gluEndTrim-Paar sind [](glubegintrim.md) / [](gluendtrim.md) GLU \_ MAP1 TRIM 2 und \_ \_ GLU \_ MAP1 \_ TRIM 3 die einzigen gültigen \_ Typen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn **gluNurbsCurve** zwischen einem **gluBeginCurve-gluEndCurve-Paar** auftritt, beschreibt es eine zu /  rendernde Kurve. Sie ordnen Positions-, Textur- und Farbkoordinaten zu, indem Sie sie als separate **gluNurbsCurve** zwischen einem gluBeginCurve-gluEndCurve-Paar  /  präsentieren. Verwenden Sie nicht mehr als einen Aufruf von **gluNurbsCurve** für Farb-, Positions- und Texturdaten innerhalb eines einzelnen gluBeginCurve-gluEndCurve-Paars.  /  Nehmen Sie genau einen Aufruf vor,  um die Position der Kurve zu beschreiben (typ GL \_ MAP1 \_ VERTEX \_ 3 oder GL \_ MAP1 \_ VERTEX \_ 4).

Wenn **gluNurbsCurve** zwischen einem [**gluBeginTrim-gluEndTrim-Paar**](glubegintrim.md)auftritt, beschreibt es eine Kürzungskurve auf einer / [](gluendtrim.md) NURBS-Oberfläche. Wenn *der Typ* GLU MAP1 TRIM 2 ist, wird eine Kurve im zweidimensionalen \_ \_ \_ Parameterraum (*u* und *v*) beschrieben. Wenn es sich um GLU MAP1 TRIM 3 handelt, wird eine Kurve im zweidimensionalen homogenen \_ \_ \_ Parameterraum (*u*, *v* und *w*) beschrieben. Weitere Informationen zum Kürzen von Kurven finden Sie unter **gluBeginTrim**.

## <a name="examples"></a>Beispiele

Die folgenden Funktionen rendern eine texturierte NURBS-Kurve mit Normals:

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndCurve**](gluendcurve.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





