---
title: glunewnurbsrenderer-Funktion (glu. h)
description: Die glunewnurbsrenderer-Funktion erstellt ein nicht einheitliches Rational B-Spline-Objekt (NURBS).
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- glunewnurbsrenderer-Funktion OpenGL
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
ms.openlocfilehash: 5b6e35df5abd9fb9e7757dd79066fbbe7efe8680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956697"
---
# <a name="glunewnurbsrenderer-function"></a>glunewnurbsrenderer-Funktion

Die **glunewnurbsrenderer** -Funktion erstellt ein nicht einheitliches Rational B-Spline-Objekt ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Syntax


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glunewnurbsrenderer** " erstellt einen Zeiger auf ein neues NURBS-Objekt und gibt diesen zurück. Lesen Sie dieses Objekt, wenn Sie die Funktionen zum Rendern und Steuern von nursb aufrufen. Der Rückgabewert 0 (null) bedeutet, dass nicht genügend Arbeitsspeicher vorhanden ist, um dem-Objekt zuzuordnen.

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

[**glubegincurve**](glubegincurve.md)
</dt> <dt>

[**glubeginsurface**](glubeginsurface.md)
</dt> <dt>

[**glubegintrim**](glubegintrim.md)
</dt> <dt>

[**gludeletenurbsrenderer**](gludeletenurbsrenderer.md)
</dt> <dt>

[*glunurbscallback*](glunurbs.md)
</dt> <dt>

[**glunurbsproperty**](glunurbsproperty.md)
</dt> </dl>

 

 





