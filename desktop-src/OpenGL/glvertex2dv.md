---
title: glVertex2dv-Funktion (Gl.h)
description: Gibt einen Scheitelpunkt an. | glVertex2dv-Funktion (Gl.h)
ms.assetid: b685d0aa-2874-4ad9-a20c-86823e9ad00b
keywords:
- glVertex2dv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbaf49ed5e1b53da7c0c4968acbab48880e6193b5f61f0179a47b40972f8236
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488320"
---
# <a name="glvertex2dv-function"></a>glVertex2dv-Funktion

Gibt einen Scheitelpunkt an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glVertex2dv(
   const GLdouble *v
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*V* 
</dt> <dd>

Ein Zeiger auf ein Array von zwei Elementen. Die Elemente sind die x- und y-Koordinaten eines Scheitelpunkts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

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

 

 





