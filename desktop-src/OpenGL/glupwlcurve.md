---
title: glupwlcurve-Funktion (glu. h)
description: Die Funktion "glupwlcurve" beschreibt eine schrittweise lineare, lineare, nicht einheitliche rationelle B-Spline-Kürzungs Kurve (NURBS).
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- glupwlcurve-Funktion OpenGL
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
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345913"
---
# <a name="glupwlcurve-function"></a>glupwlcurve-Funktion

Die Funktion " **glupwlcurve** " beschreibt eine schrittweise lineare, lineare, nicht einheitliche rationelle B-Spline-Kürzungs Kurve ([NURBS](using-nurbs-curves-and-surfaces.md)).

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

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> <dt>

*count* 
</dt> <dd>

Die Anzahl der Punkte in der Kurve.

</dd> <dt>

*array* 
</dt> <dd>

Ein Array, das die Kurven Punkte enthält.

</dd> <dt>

*Schritt* 
</dt> <dd>

Der Offset (eine Anzahl von Gleit Komma Werten mit einfacher Genauigkeit) zwischen den Punkten der Kurve.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Kurve. Muss entweder "glu \_ zuordnung1 \_ Trim \_ 2" oder "glu \_ zuordnung1 \_ Trim \_ 3" lauten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glupwlcurve** " beschreibt eine schrittweise lineare Kürzungs Kurve für eine nursb-Oberfläche. Eine schrittweise lineare Kurve besteht aus einer Liste von Koordinaten der Punkte im Parameter Bereich für die zu gekürzte nursb-Oberfläche. Diese Punkte sind mit Liniensegmenten verbunden, um eine Kurve zu bilden. Wenn die Kurve eine Annäherung an eine echte Kurve ist, sollten die Punkte nahe genug sein, damit der resultierende Pfad bei der in der Anwendung verwendeten Auflösung gekrümmte angezeigt wird.

Wenn der *Typ* "glu \_ zuordnung1 Trim 2" ist, wird \_ \_ eine Kurve im zweidimensionalen (*u* -und *v*-) Parameter Bereich beschrieben. Wenn dies der Fall \_ ist \_ \_ , wird eine Kurve im zweidimensionalen, homogenen (*u*, *v*-und *w*)-Parameter Bereich beschrieben. Weitere Informationen zu Kürzungs Kurven finden Sie unter " [**glubegintrim**](glubegintrim.md)".

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
</dt> </dl>

 

 





