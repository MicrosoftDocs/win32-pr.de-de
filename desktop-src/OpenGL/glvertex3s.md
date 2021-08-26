---
title: glVertex3s-Funktion (Gl.h)
description: Gibt einen Scheitelpunkt an. | glVertex3s-Funktion (Gl.h)
ms.assetid: ee970440-3eb3-46d6-80d2-e23649585510
keywords:
- glVertex3s-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33a9d5f3280c3910ffff1352a459926504c8ad04b43957e227eaa46b1990683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035860"
---
# <a name="glvertex3s-function"></a>glVertex3s-Funktion

Gibt einen Scheitelpunkt an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glVertex3s(
   GLshort x,
   GLshort y,
   GLshort z
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Gibt die x-Koordinate eines Scheitelpunkts an.

</dd> <dt>

*y* 
</dt> <dd>

Gibt die y-Koordinate eines Scheitelpunkts an.

</dd> <dt>

*Z* 
</dt> <dd>

Gibt die Z-Koordinate eines Scheitelpunkts an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die GlVertex-Funktionsbefehle werden in [**glBegin**](glbegin.md) / [**glEnd-Paaren**](glend.md) verwendet, um Punkt-, Linien- und Polygonvertices anzugeben. Die aktuellen Farb-, Normal- und Texturkoordinaten werden dem Scheitelpunkt zugeordnet, wenn glVertex aufgerufen wird. Wenn nur *x* und *y* angegeben werden, wird *z* standardmäßig auf 0,0 und *w* standardmäßig auf 1,0 festgelegt. Wenn *x,* *y* und *z* angegeben werden, wird *w* standardmäßig auf 1,0 festgelegt. Das Aufrufen von glVertex außerhalb eines **glBegin** / **glEnd-Paars** führt zu undefiniertem Verhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glRect**](glrect-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> </dl>

 

 





