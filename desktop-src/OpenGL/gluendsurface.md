---
title: gluendsurface-Funktion (glu. h)
description: Die Funktionen "glubeginsurface" und "gluendsurface" begrenzen eine nicht einheitliche Oberflächen Definition von "Rational B-Spline (NURBS)". | gluendsurface-Funktion (glu. h)
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
keywords:
- gluendsurface-Funktion OpenGL
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
ms.openlocfilehash: 54631d5c4ef752cffd989f8fa02f8cb512c67da3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530719"
---
# <a name="gluendsurface-function"></a>gluendsurface-Funktion

Die Funktionen " [**glubeginsurface**](glubeginsurface.md) " und " **gluendsurface** " begrenzen eine nicht einheitliche Oberflächen Definition von "Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md))".

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

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktionen " [**glubeginsurface**](glubeginsurface.md) " und " **gluendsurface** " markieren den Anfang und das Ende der nurb-Oberflächen Definitionen, die mit Aufrufen von " **glunurbssurface**" definiert werden.

1.  Aufrufen von " **glubeginsurface** ", um den Anfang einer nursb-Oberflächen Definition zu markieren.
2.  Erstellen Sie einen oder mehrere Aufrufe von **glunurbssurface** , um die Attribute der Oberfläche zu definieren.

    Genau einer dieser Aufrufe von **glunurbssurface** muss den Surface-Typ GL \_ map2 \_ Vertex \_ 3 oder GL \_ map2 \_ Scheitelpunkt \_ 4 aufweisen.

3.  Um das Ende der nursb-Oberflächen Definition zu markieren, nennen Sie " **gluendsurface**".

Die Funktionen [**glubegintrim**](glubegintrim.md), [**glupwlcurve**](glupwlcurve.md), [**glunurbscurve**](glunurbscurve.md)und **gluendtrim** unterstützen das Kürzen von nurb-Oberflächen.

Verwenden Sie OpenGL-Auswertungen, um die nursb-Oberfläche als eine Reihe von Polygonen darzustellen. Bewahren Sie den auswertsauswertszustand während des Renderings mit [**glpushatpub**](glpushattrib.md) (GL \_ eval \_ Bit) und [**glpopatpub**](glpopattrib.md)auf.

## <a name="examples"></a>Beispiele

Die folgenden Funktionen Renten eine strukturierte nursb-Oberfläche mit Normals. die Texturkoordinaten und normale werden auch als nursb-Oberflächen beschrieben:

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
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glubegincurve**](glubegincurve.md)
</dt> <dt>

[**glubegintrim**](glubegintrim.md)
</dt> <dt>

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**glunurbscurve**](glunurbscurve.md)
</dt> <dt>

[**glunurbssurface**](glunurbssurface.md)
</dt> <dt>

[**glupwlcurve**](glupwlcurve.md)
</dt> </dl>

 

 





