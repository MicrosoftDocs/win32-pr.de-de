---
title: glVertex2i-Funktion (Gl.h)
description: Gibt einen Scheitelpunkt an. | glVertex2i-Funktion (Gl.h)
ms.assetid: 13dc175b-9382-4266-962d-6dcf23ff5949
keywords:
- glVertex2i-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex2i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c05b0cf84b5b730d308cc3122a9f9b555eaedd7a7945c9d5cfc6341fa34b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036260"
---
# <a name="glvertex2i-function"></a>glVertex2i-Funktion

Gibt einen Scheitelpunkt an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glVertex2i(
   GLint x,
   GLint y
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

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die glVertex-Funktionsbefehle werden in [**glBegin**](glbegin.md) / [**glEnd-Paaren**](glend.md) verwendet, um Punkt-, Linien- und Polygonvertices anzugeben. Die aktuellen Farb-, Normal- und Texturkoordinaten werden dem Scheitelpunkt zugeordnet, wenn glVertex aufgerufen wird. Wenn nur *x* und *y angegeben* werden, *wird z* standardmäßig auf 0,0 und *w* auf 1,0 festgelegt. Wenn *x,* *y* und z angegeben *werden,* *wird w* standardmäßig auf 1,0 festgelegt. Das Aufrufen von glVertex außerhalb eines **glBegin** / **glEnd-Paars** führt zu nicht definiertem Verhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

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

 

 





