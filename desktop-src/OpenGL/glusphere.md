---
title: glusphere-Funktion (glu. h)
description: Die Funktion "glusphere" zeichnet eine Kugel.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- glusphere-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478015"
---
# <a name="glusphere-function"></a>glusphere-Funktion

Die Funktion " **glusphere** " zeichnet eine Kugel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
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

*Kreises* 
</dt> <dd>

Der Radius der Kugel.

</dd> <dt>

*aufs* 
</dt> <dd>

Die Anzahl der Unterteilungen um die z-Achse (ähnlich wie Längengrad).

</dd> <dt>

*Stöcke* 
</dt> <dd>

Die Anzahl der untergeordneten Bereiche entlang der z-Achse (ähnlich wie bei breiten Linien).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **glusphere** -Funktion zeichnet eine Kugel des angegebenen Radius, zentriert um den Ursprung. Die Kugel wird um die z-Achse in Slices und entlang der z-Achse in Stapel aufgeteilt (ähnlich wie Längen-und Breitengrad).

Wenn die Ausrichtung auf "glu \_ outside" (mit " **gluquadricorientation**") festgelegt ist, werden alle normalisierten Punkte vom Mittelpunkt der Kugel entfernt. Andernfalls zeigen Sie auf den Mittelpunkt der Kugel.

Wenn die Texturierung aktiviert ist (mit " **gluquadrictexture**"), werden Texturkoordinaten generiert, sodass *t* von 0,0 bei *z* =-*RADIUS* bis 1,0 am *z*-  =  *RADIUS* reicht (*t* vergrößert sich linear entlang der Längenlinien); und *s* liegen zwischen 0,0 und der positiven y-Achse, bis 0,25 auf der positiven x-Achse, bis 0,5 auf der negativen y-Achse, bis 0,75 auf der negativen x-Achse und zurück zu 1,0 auf der positiven y-Achse.

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

[**gludisk**](gludisk.md)
</dt> <dt>

[**glunewquadric**](glunewquadric.md)
</dt> <dt>

[**glupartialdisk**](glupartialdisk.md)
</dt> <dt>

[**gluquadricorientation**](gluquadricorientation.md)
</dt> <dt>

[**gluquadrictexture**](gluquadrictexture.md)
</dt> </dl>

 

 





