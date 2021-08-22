---
title: gluNewNurbsRenderer-Funktion (Glu.h)
description: Die funktion gluNewNurbsRenderer erstellt ein NURBS-Objekt (Non-Uniform Rational B-Spline).
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- gluNewNurbsRenderer-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089c1a88ac0fe9ac246efd435ae941ba5e66e2412595e4f5f96dc73e85e90478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937795"
---
# <a name="glunewnurbsrenderer-function"></a>gluNewNurbsRenderer-Funktion

Die **funktion gluNewNurbsRenderer** erstellt ein nicht einheitliches rationales B-Spline-Objekt [(NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Syntax


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="remarks"></a>Hinweise

Die **funktion gluNewNurbsRenderer** erstellt einen Zeiger auf ein neues NURBS-Objekt und gibt diesen zurück. Verweisen Sie beim Aufrufen von NURBS-Rendering- und -Steuerungsfunktionen auf dieses Objekt. Der Rückgabewert 0 bedeutet, dass nicht genügend Arbeitsspeicher vorhanden ist, um dem Objekt zuzuordnen.

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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





