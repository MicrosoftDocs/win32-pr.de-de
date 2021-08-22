---
title: gluOrtho2D-Funktion (Glu.h)
description: Die gluOrtho2D-Funktion definiert eine 2D-Orthografische Projektionsmatrix.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- gluOrtho2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a2f0d5fad1a2efb0df0c802dbb2cf51b54ff3e43402c3143bad982009f4f95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488860"
---
# <a name="gluortho2d-function"></a>gluOrtho2D-Funktion

Die **gluOrtho2D-Funktion** definiert eine 2D-Orthografische Projektionsmatrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Links* 
</dt> <dd>

Die Koordinate für die linke vertikale Clippingebene.

</dd> <dt>

*Richting* 
</dt> <dd>

Die Koordinate für die rechte vertikale Clippingebene.

</dd> <dt>

*top* 
</dt> <dd>

Die Koordinate für die obere horizontale Clippingebene.

</dd> <dt>

*Unteres* 
</dt> <dd>

Die Koordinate für die untere horizontale Clippingebene.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluOrtho2D-Funktion** richtet einen zweidimensionalen orthografischen Anzeigebereich ein. Dies entspricht dem Aufruf [**von glOrtho**](glortho.md) mit zNear = -1 und zFar = 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





