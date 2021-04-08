---
title: gludeletenurbsrenderer-Funktion (glu. h)
description: Die Funktion "gludeletenurbsrenderer" zerstört ein nicht einheitliches Rational B-Spline-Objekt (NURBS).
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- gludeletenurbsrenderer-Funktion OpenGL
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
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741417"
---
# <a name="gludeletenurbsrenderer-function"></a>gludeletenurbsrenderer-Funktion

Die Funktion " **gludeletenurbsrenderer** " zerstört ein nicht einheitliches Rational B-Spline-Objekt ([NURBS](using-nurbs-curves-and-surfaces.md)).

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

Das NURBS-Objekt, das zerstört werden soll (mit **glunewnurbsrenderer** erstellt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gludeletenurbsrenderer** " zerstört das NURBS-Objekt und gibt den verwendeten Arbeitsspeicher frei. Nachdem Sie " **gludeletenurbsrenderer**" aufgerufen haben, können Sie *nobj* nicht mehr verwenden.

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

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





