---
title: glunewquadric-Funktion (glu. h)
description: Die Funktion "glunewquadric" erstellt ein Quadric-Objekt.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- glunewquadric-Funktion OpenGL
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
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956696"
---
# <a name="glunewquadric-function"></a>glunewquadric-Funktion

Die Funktion " **glunewquadric** " erstellt ein Quadric-Objekt.

## <a name="syntax"></a>Syntax


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glunewquadric** " erstellt einen Zeiger auf ein neues Quadric-Objekt und gibt diesen zurück. Verweisen Sie auf dieses Objekt, wenn Sie Quadric-Rendering-und-Steuerungsfunktionen aufrufen. Der Rückgabewert 0 (null) bedeutet, dass nicht genügend Arbeitsspeicher vorhanden ist, um dem-Objekt zuzuordnen.

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

[**gluzylinder**](glucylinder.md)
</dt> <dt>

[**gludeletequadric**](gludeletequadric.md)
</dt> <dt>

[**gludisk**](gludisk.md)
</dt> <dt>

[**glupartialdisk**](glupartialdisk.md)
</dt> <dt>

[*gluvierccallback*](gluquadric.md)
</dt> <dt>

[**gluquadricdrawstyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluquadricnormals**](gluquadricnormals.md)
</dt> <dt>

[**gluquadricorientation**](gluquadricorientation.md)
</dt> <dt>

[**gluquadrictexture**](gluquadrictexture.md)
</dt> <dt>

[**glusphere**](glusphere.md)
</dt> </dl>

 

 





