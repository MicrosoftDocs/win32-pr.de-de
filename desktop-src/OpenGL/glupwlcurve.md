---
title: gluPwlCurve-Funktion (Glu.h)
description: Die gluPwlCurve-Funktion beschreibt eine stückweise lineare non-Uniform Rational B-Spline (NURBS)-Kürzungskurve.
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- gluPwlCurve-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9911619e54247c633d4b3cecc69327f92da6a7f27c3cebf9231ec86ad0f0a20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061568"
---
# <a name="glupwlcurve-function"></a>gluPwlCurve-Funktion

Die **gluPwlCurve-Funktion** beschreibt eine stückweise lineare non-Uniform Rational B-Spline (NURBS)-Trimmingkurve.[](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*count* 
</dt> <dd>

Die Anzahl der Punkte in der Kurve.

</dd> <dt>

*array* 
</dt> <dd>

Ein Array, das die Kurvenpunkte enthält.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Offset (eine Anzahl von Gleitkommawerten mit einzelner Genauigkeit) zwischen Punkten in der Kurve.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Kurve. Muss entweder GLU \_ MAP1 \_ TRIM \_ 2 oder GLU \_ MAP1 \_ TRIM \_ 3 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluPwlCurve-Funktion** beschreibt eine stückweise lineare Kürzungskurve für eine NURBS-Oberfläche. Eine stückweise lineare Kurve besteht aus einer Liste von Koordinaten von Punkten im Parameterraum für die zu kürzede NURBS-Oberfläche. Diese Punkte sind mit Liniensegmenten verbunden, um eine Kurve zu bilden. Wenn die Kurve eine Näherung zu einer echten Kurve ist, sollten die Punkte nahe genug sein, damit der resultierende Pfad bei der in der Anwendung verwendeten Auflösung gekrümmt angezeigt wird.

Wenn *der Typ* GLU MAP1 TRIM 2 ist, wird eine Kurve im zweidimensionalen \_ \_ \_ Parameterraum (*u* und *v*) beschrieben. Wenn es sich um GLU MAP1 TRIM 3 handelt, wird eine Kurve im zweidimensionalen homogenen \_ \_ \_ Parameterraum (*u*, *v* und *w*) beschrieben. Weitere Informationen zum Kürzen von Kurven finden Sie unter [**gluBeginTrim**](glubegintrim.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





