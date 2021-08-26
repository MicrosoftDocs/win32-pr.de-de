---
title: gluNewQuadric-Funktion (Glu.h)
description: Die gluNewQuadric-Funktion erstellt ein Quadric-Objekt.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- gluNewQuadric-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66fed28c555d327bffa18d8f9100a6f5e9824b714bff1308e6b2dab20b5d3671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036270"
---
# <a name="glunewquadric-function"></a>gluNewQuadric-Funktion

Die **gluNewQuadric-Funktion erstellt** ein Quadric-Objekt.

## <a name="syntax"></a>Syntax


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="remarks"></a>Hinweise

Die **gluNewQuadric-Funktion erstellt** einen Zeiger auf ein neues Quadric-Objekt und gibt einen Zeiger zurück. Verweisen Sie beim Aufrufen von Quadric-Rendering- und Steuerelementfunktionen auf dieses Objekt. Der Rückgabewert 0 (null) bedeutet, dass nicht genügend Arbeitsspeicher für das Objekt vorhanden ist.

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

[**gluCylinder**](glucylinder.md)
</dt> <dt>

[**gluDeleteQuadric**](gludeletequadric.md)
</dt> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





