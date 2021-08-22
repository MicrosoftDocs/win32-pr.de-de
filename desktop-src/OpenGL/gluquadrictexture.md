---
title: gluQuadricTexture-Funktion (Glu.h)
description: Die gluQuadricTexture-Funktion gibt an, ob Quadrics texturiert werden sollen.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- gluQuadricTexture-Funktion OpenGL
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
ms.openlocfilehash: bbde88e0a878fd59e01ad0a450cf4cbe9831c4ad867c8029373586a8efe830eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937481"
---
# <a name="gluquadrictexture-function"></a>gluQuadricTexture-Funktion

Die **gluQuadricTexture-Funktion** gibt an, ob Quadrics texturiert werden sollen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*quadObject* 
</dt> <dd>

Das quadrierte Objekt (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*textureCoords* 
</dt> <dd>

Ein Flag, das angibt, ob Texturkoordinaten generiert werden sollen. Die folgenden Werte sind gültig.



| Wert                                                                                                                                          | Bedeutung                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <dt>**GL \_ TRUE**</dt> </dl>    | Generieren sie Texturkoordinaten.<br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <dt>**GL \_ FALSE**</dt> </dl> | Generieren Sie keine Texturkoordinaten. Dies ist der Standardwert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluQuadricTexture-Funktion** gibt an, ob Texturkoordinaten für Quadrics generiert werden sollen, die mit **quadObject** gerendert werden.

Die Art und Weise, in der Texturkoordinaten generiert werden, hängt von dem spezifischen quadrierten ab.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> </dl>

 

 





