---
title: gluzylinder-Funktion (glu. h)
description: Die Funktion "gluzylinder" zeichnet einen Zylinder.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- gluzylinder-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345305"
---
# <a name="glucylinder-function"></a>gluzylinder-Funktion

Die Funktion " **gluzylinder** " zeichnet einen Zylinder.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*qobj* 
</dt> <dd>

Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).

</dd> <dt>

*baseradius* 
</dt> <dd>

Der Radius des Zylinders bei *z* = 0.

</dd> <dt>

*topradius* 
</dt> <dd>

Der Radius des Zylinders an der *z*-  =  *Höhe*.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Zylinders.

</dd> <dt>

*aufs* 
</dt> <dd>

Die Anzahl der Unterteilungen um die z-Achse.

</dd> <dt>

*Stöcke* 
</dt> <dd>

Die Anzahl der Unterteilungen entlang der z-Achse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluzylinder** " zeichnet einen Zylinder, der entlang der z-Achse ausgerichtet ist. Die Basis des Zylinders wird bei *z* = 0 und am oberen Rand bei der *z*-  =  *Höhe* platziert. Wie bei einer Kugel wird ein Zylinder um die z-Achse in Slices und entlang der z-Achse in Stapel aufgeteilt.

Beachten Sie, dass diese Routine einen Kegel generiert, wenn *topradius* auf 0 (null) festgelegt ist.

Wenn die Ausrichtung auf "glu \_ outside" (mit " [**gluquadricorientation**](gluquadricorientation.md)") festgelegt ist, zeigen alle generierten normale von der z-Achse Weg. Andernfalls zeigen Sie auf die z-Achse.

Wenn die Texturierung aktiviert ist (mit " [**gluquadrictexture**](gluquadrictexture.md)"): Es werden Texturkoordinaten generiert, sodass *t* von 0,0 bei *z* = 0 auf 1,0 bei *z*  =  *height* und *s* zwischen 0,0 an der positiven y-Achse, bis 0,25 an der positiven x-Achse, zu 0,5 auf der negativen y-Achse, zu 0,75 auf der negativen x-Achse und zurück zu 1,0 auf der positiven y-Achse reicht.

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

[**gludisk**](gludisk.md)
</dt> <dt>

[**glunewquadric**](glunewquadric.md)
</dt> <dt>

[**glupartialdisk**](glupartialdisk.md)
</dt> <dt>

[**gluquadricorientation**](gluquadricorientation.md)
</dt> <dt>

[**gluquadrictexture**](gluquadrictexture.md)
</dt> <dt>

[**glusphere**](glusphere.md)
</dt> </dl>

 

 





