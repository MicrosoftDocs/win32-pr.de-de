---
title: glVertex4fv-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex4fv-Funktion (GL. h)
ms.assetid: c2a766fd-3ad8-463b-8f09-36d0673e6716
keywords:
- glVertex4fv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex4fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e05551268b697ba4444c29d5f2b9bdfb0e832e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361807"
---
# <a name="glvertex4fv-function"></a>glVertex4fv-Funktion

Gibt einen Scheitelpunkt an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glVertex4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ramelow* 
</dt> <dd>

Ein Zeiger auf ein Array aus vier Elementen. Die Elemente sind die x-, y-, z-und w-Koordinaten eines Scheitel Punkts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

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

 

 





