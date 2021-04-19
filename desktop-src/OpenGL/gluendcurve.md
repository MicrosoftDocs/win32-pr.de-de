---
title: gluendcurve-Funktion (glu. h)
description: Die Funktionen "glubegincurve" und "gluendcurve" begrenzen eine nicht einheitliche (NURBS) Kurven Definition von Rational B. | gluendcurve-Funktion (glu. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- gluendcurve-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6c0c08bf31135ca82e87d2093ef3b57197955
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361821"
---
# <a name="gluendcurve-function"></a>gluendcurve-Funktion

Die Funktionen " [**glubegincurve**](glubegincurve.md) " und " **gluendcurve** " begrenzen eine nicht einheitliche ([NURBS](using-nurbs-curves-and-surfaces.md)) Kurven Definition von Rational B.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluEndCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie " [**glubegincurve**](glubegincurve.md) ", um den Anfang einer nursb-Kurven Definition zu markieren. Nachdem Sie " **glubegincurve**" aufgerufen haben, erstellen Sie einen oder mehrere Aufrufe von " [**glunurbscurve**](glunurbscurve.md) ", um die Attribute der Kurve zu definieren. Genau einer der Aufrufe von **glunurbscurve** muss den Kurven-Typ GL \_ zuordnung1 \_ Vertex \_ 3 oder GL \_ zuordnung1 \_ Scheitelpunkt \_ 4 aufweisen. Um das Ende der nursb-Kurven Definition zu markieren, nennen Sie " **gluendcurve**".

OpenGL-Evaluatoren werden verwendet, um die nursb-Kurve als Reihe von Liniensegmenten zu Rendering. Der auswersichtsstatus wird während des Renderings mit [**glpushatpub**](glpushattrib.md) (GL \_ eval \_ Bit) und [**glpopatpub**](glpopattrib.md)beibehalten. Informationen dazu, in welchem Zustand diese Aufrufe beibehalten werden, finden Sie unter **glpushatpub**.

## <a name="examples"></a>Beispiele

Die folgenden Funktionen erzeugen eine strukturierte nursb-Kurve mit Normals. Texturkoordinaten und normale werden auch als nursb-Kurven angegeben:

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
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glpushatpub**](glpushattrib.md)
</dt> <dt>

[**glubeginsurface**](glubeginsurface.md)
</dt> <dt>

[**glubegintrim**](glubegintrim.md)
</dt> <dt>

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**glunurbscurve**](glunurbscurve.md)
</dt> </dl>

 

 





