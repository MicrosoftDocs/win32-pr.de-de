---
title: gluDeleteNurbsRenderer-Funktion (Glu.h)
description: Die funktion gluDeleteNurbsRenderer zerstört ein NURBS-Objekt (Non-Uniform Rational B-Spline).
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- gluDeleteNurbsRenderer-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b114c6d67452468f3b8b92e443580d8d6f06c7df8bc1b6647916c210d204955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613017"
---
# <a name="gludeletenurbsrenderer-function"></a>gluDeleteNurbsRenderer-Funktion

Die **funktion gluDeleteNurbsRenderer** zerstört ein nicht einheitliches rationales B-Spline-Objekt [(NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt, das zerstört werden soll (erstellt mit **gluNewNurbsRenderer**).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **funktion gluDeleteNurbsRenderer** zerstört das NURBS-Objekt und gibt den verwendeten Arbeitsspeicher frei. Nachdem Sie **gluDeleteNurbsRenderer** aufgerufen haben, können Sie *nobj* nicht mehr verwenden.

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

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





