---
title: gluEndCurve-Funktion (Glu.h)
description: Die Funktionen gluBeginCurve und gluEndCurve begrenzen eine NURBS-Kurvendefinition (Non-Uniform Rational B-Spline). | gluEndCurve-Funktion (Glu.h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- gluEndCurve-Funktion OpenGL
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
ms.openlocfilehash: 20b6d8e9871b03286eebc285d2c3ad8834c8c354b196213c985626fc80cd02fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489520"
---
# <a name="gluendcurve-function"></a>gluEndCurve-Funktion

Die Funktionen [**gluBeginCurve**](glubegincurve.md) und **gluEndCurve** grenzen eine nicht einheitliche rationale B-Spline -Kurvendefinition [(NURBS)](using-nurbs-curves-and-surfaces.md)ab.

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

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie [**gluBeginCurve,**](glubegincurve.md) um den Anfang einer NURBS-Kurvendefinition zu markieren. Nachdem **Sie gluBeginCurve** aufgerufen haben, rufen [**Sie gluNurbsCurve**](glunurbscurve.md) auf, um die Attribute der Kurve zu definieren. Genau einer der Aufrufe von **gluNurbsCurve** muss den Kurventyp GL \_ MAP1 \_ VERTEX \_ 3 oder GL \_ MAP1 \_ VERTEX \_ 4 aufweisen. Rufen Sie **gluEndCurve** auf, um das Ende der NURBS-Kurvendefinition zu markieren.

OpenGL-Auswertungen werden verwendet, um die NURBS-Kurve als eine Reihe von Liniensegmenten zu rendern. Der Auswertungszustand wird beim Rendern mit [**glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT ) und [**glPopAttrib**](glpopattrib.md)beibehalten. Informationen dazu, in welchem Zustand diese Aufrufe beibehalten werden, finden Sie unter **glPushAttrib.**

## <a name="examples"></a>Beispiele

Die folgenden Funktionen rendern eine texturierte NURBS-Kurve mit Normalitäten. Texturkoordinaten und Normalitäten werden auch als NURBS-Kurven angegeben:

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

 

 





