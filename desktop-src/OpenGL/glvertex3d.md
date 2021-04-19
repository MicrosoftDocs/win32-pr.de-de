---
title: glVertex3d-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex3d-Funktion (GL. h)
ms.assetid: 531a552d-7979-4994-ad28-73c2d3987bae
keywords:
- glVertex3d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 608ab02bf2cd41b7f2ffcc8fa3fe8cb2dea0ca89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366606"
---
# <a name="glvertex3d-function"></a>glVertex3d-Funktion

Gibt einen Scheitelpunkt an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glVertex3d(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Gibt die x-Koordinate eines Scheitel Punkts an.

</dd> <dt>

*y* 
</dt> <dd>

Gibt die y-Koordinate eines Scheitel Punkts an.

</dd> <dt>

*z* 
</dt> <dd>

Gibt die z-Koordinate eines Scheitel Punkts an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die glVertex-Funktions Befehle werden innerhalb von [**glBegin**](glbegin.md)- / [**glEnd**](glend.md) -Paaren zum Angeben von Punkt-, Linien-und Polygon Scheitel Punkten verwendet. Die aktuellen Farben, normalen und Texturkoordinaten werden dem Scheitelpunkt zugeordnet, wenn glVertex aufgerufen wird. Wenn nur *x* und *y* angegeben werden, wird für *z* standardmäßig 0,0 und für *w* der Standardwert 1,0 verwendet. Wenn *x*, *y* und *z* angegeben werden, wird *der Standardwert* 1,0 verwendet. Das Aufrufen von glVertex außerhalb eines **glBegin**- / **glEnd** -Paars führt zu undefiniertem Verhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glcolor**](glcolor-functions.md)
</dt> <dt>

[**gledgeflag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glevalcoord**](glevalcoord-functions.md)
</dt> <dt>

[**glindex**](glindex-functions.md)
</dt> <dt>

[**glmaterial**](glmaterial-functions.md)
</dt> <dt>

[**glnormal**](glnormal-functions.md)
</dt> <dt>

[**glrect**](glrect-functions.md)
</dt> <dt>

[**gltexcoord**](gltexcoord-functions.md)
</dt> </dl>

 

 





