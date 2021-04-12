---
title: gluquadrictexture-Funktion (glu. h)
description: Die Funktion "gluquadrictexture" gibt an, ob viercs texturiert werden sollen.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- gluquadrictexture-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc395564b6c6f30f38a8c5129c489d0bfca6b80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104930"
---
# <a name="gluquadrictexture-function"></a>gluquadrictexture-Funktion

Die Funktion " **gluquadrictexture** " gibt an, ob viercs texturiert werden sollen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*quadobject* 
</dt> <dd>

Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).

</dd> <dt>

*texturecoords* 
</dt> <dd>

Ein Flag, das angibt, ob Texturkoordinaten generiert werden sollen. Die folgenden Werte sind gültig.



| Wert                                                                                                                                          | Bedeutung                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <dt>**GL \_ true**</dt> </dl>    | Texturkoordinaten generieren.<br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <dt>**GL \_ false**</dt> </dl> | Keine Texturkoordinaten generieren. Dies ist der Standardwert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluquadrictexture** " gibt an, ob Texturkoordinaten für viercs generiert werden sollen, die mit **quadobject** gerendert werden.

Die Art und Weise, in der Texturkoordinaten generiert werden, hängt von dem gerenderten Quadric ab.

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

[**glunewquadric**](glunewquadric.md)
</dt> <dt>

[**gluquadricdrawstyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluquadricnormals**](gluquadricnormals.md)
</dt> </dl>

 

 





