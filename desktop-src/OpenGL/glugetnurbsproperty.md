---
title: gluGetNurbsProperty-Funktion (Glu.h)
description: Die gluGetNurbsProperty-Funktion ruft eine Non-Uniform Rational B-Spline (NURBS)-Eigenschaft ab.
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- gluGetNurbsProperty-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a68e91fbdaafc2a1857a95e059125bf62347777edfbcc764868ceea0a8fce578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519590"
---
# <a name="glugetnurbsproperty-function"></a>gluGetNurbsProperty-Funktion

Die **gluGetNurbsProperty-Funktion** ruft eine non-Uniform Rational B-Spline [(NURBS)-Eigenschaft](using-nurbs-curves-and-surfaces.md)ab.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Die Eigenschaft, deren Wert abgerufen werden soll. Die folgenden Werte sind gültig: GLU SAMPLING \_ \_ TOLERANCE, GLU \_ DISPLAY \_ MODE, \_ GLU CULLING, GLU \_ AUTO LOAD \_ \_ MATRIX, GLU \_ PARAMETRIC \_ TOLERANCE, GLU \_ SAMPLING METHOD, GLU U STEP und \_ \_ \_ GLU V \_ \_ STEP.

</dd> <dt>

*value* 
</dt> <dd>

Ein Zeiger auf die Position, an der der Wert der benannten Eigenschaft geschrieben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden **Sie gluGetNurbsProperty,** um Eigenschaften abzurufen, die in einem NURBS-Objekt gespeichert sind. Diese Eigenschaften beeinflussen die Art und Weise, wie NURBS-Kurven und -Oberflächen gerendert werden. Informationen zu NURBS-Eigenschaften finden Sie unter [**gluNurbsProperty**](glunurbsproperty.md).

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

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





