---
title: glunurbscurve-Funktion (glu. h)
description: Die Funktion "glunurbscurve" definiert die Form einer nicht einheitlichen rationellen B-Spline-Kurve (NURBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- glunurbscurve-Funktion OpenGL
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
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339140"
---
# <a name="glunurbscurve-function"></a>glunurbscurve-Funktion

Die Funktion " **glunurbscurve** " definiert die Form einer nicht einheitlichen rationellen B-Spline-Kurve ([NURBS](using-nurbs-curves-and-surfaces.md)).

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

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> <dt>

*nknoten* 
</dt> <dd>

Die Anzahl der Knoten im- *Knoten*. Der *nknoparameter* ist mit der Anzahl der Kontrollpunkte zuzüglich der Bestellung.

</dd> <dt>

*knir* 
</dt> <dd>

Ein Array von *nknoten-* Zeichen Werten, die sich nicht verkleinern.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Offset (als Anzahl von Gleit Komma Werten mit einfacher Genauigkeit) zwischen aufeinander folgenden Kurven Steuerungs Punkten.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Ein Zeiger auf ein Array von Steuerungs Punkten. Die Koordinaten müssen mit dem *Typ* übereinstimmen.

</dd> <dt>

*order* 
</dt> <dd>

Die Reihenfolge der nursb-Kurve. Der *Order* -Parameter ist mit dem Grad + 1; Daher hat eine kubische Kurve eine Reihenfolge von 4.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Kurve. Wenn diese Kurve innerhalb eines " [**glubegincurve**](glubegincurve.md)"-Paares " / [**gluendcurve**](gluendcurve.md) " definiert ist, kann der Typ jeder der gültigen eindimensionalen auswerterypen (z. b. gl \_ zuordnung1 \_ Vertex \_ 3 oder GL \_ zuordnung1 \_ Color \_ 4) sein. Zwischen einem " [**glubegintrim**](glubegintrim.md) / [**gluendtrim**](gluendtrim.md) "-paar sind nur die gültigen Typen "glu \_ zuordnung1 \_ Trim \_ 2" und "glu \_ zuordnung1 \_ Trim \_ 3" zulässig.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn **glunurbscurve** zwischen einem " **glubegincurve**"-paar " / **gluendcurve** " angezeigt wird, wird eine Kurve beschrieben, die gerendert wird. Sie ordnen positionelle, Textur-und Farbkoordinaten zu, indem Sie diese als separate " **glunurbscurve** " zwischen einem " **glubegincurve**"-paar " / **gluendcurve** " darstellen. Nehmen Sie nicht mehr als einen Aufrufen von **glunurbscurve** für Farb-, Positions-und Textur Daten innerhalb eines einzelnen **glubegincurve**- / **gluendcurve** -Paars vor. Machen Sie genau einen Aufrufs, um die Position der Kurve zu beschreiben (ein *Typ* von GL \_ zuordnung1 \_ Vertex \_ 3 oder GL \_ zuordnung1 \_ Scheitelpunkt \_ 4).

Wenn **glunurbscurve** zwischen einem " [**glubegintrim**](glubegintrim.md) / [**gluendtrim**](gluendtrim.md) "-paar angezeigt wird, wird eine Kürzungs Kurve auf einer nurb-Oberfläche beschrieben. Wenn der *Typ* "glu \_ zuordnung1 Trim 2" ist, wird \_ \_ eine Kurve im zweidimensionalen (*u* -und *v*-) Parameter Bereich beschrieben. Wenn dies der Fall \_ ist \_ \_ , wird eine Kurve im zweidimensionalen, homogenen (*u*, *v*-und *w*)-Parameter Bereich beschrieben. Weitere Informationen zu Kürzungs Kurven finden Sie unter " **glubegintrim**".

## <a name="examples"></a>Beispiele

Die folgenden Funktionen erzeugen eine strukturierte nursb-Kurve mit normalen:

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
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glubegincurve**](glubegincurve.md)
</dt> <dt>

[**glubegintrim**](glubegintrim.md)
</dt> <dt>

[**gluendcurve**](gluendcurve.md)
</dt> <dt>

[**gluendtrim**](gluendtrim.md)
</dt> <dt>

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**glupwlcurve**](glupwlcurve.md)
</dt> </dl>

 

 





