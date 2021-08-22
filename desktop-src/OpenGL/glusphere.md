---
title: gluSphere-Funktion (Glu.h)
description: Die gluSphere-Funktion zeichnet eine Kugel.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- gluSphere-Funktion OpenGL
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
ms.openlocfilehash: 590c4b7335fe0596c5b5b0f3dc709998fafc21f7be78f493a05f6520ed9fd368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488730"
---
# <a name="glusphere-function"></a>gluSphere-Funktion

Die **gluSphere-Funktion** zeichnet eine Kugel.

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

Das Quadric-Objekt (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*Radius* 
</dt> <dd>

Der Radius der Kugel.

</dd> <dt>

*Scheiben* 
</dt> <dd>

Die Anzahl der Unterteilungen um die Z-Achse (ähnlich den Längengradzeilen).

</dd> <dt>

*Stacks* 
</dt> <dd>

Die Anzahl der Unterteilungen entlang der Z-Achse (ähnlich den Breitengradlinien).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluSphere-Funktion** zeichnet eine Kugel des angegebenen Radius, der um den Ursprung zentriert ist. Die Kugel wird um die Z-Achse in Slices und entlang der Z-Achse in Stapel unterteilt (ähnlich wie Längen- und Breitengradlinien).

Wenn die Ausrichtung auf GLU \_ OUTSIDE (mit **gluQuadricOrientation)** festgelegt ist, zeigen alle generierten Normals vom Mittelpunkt der Kugel ab. Andernfalls zeigen sie auf die Mitte der Kugel.

Wenn die Texturierung aktiviert ist (mit **gluQuadricTexture):** Texturkoordinaten werden generiert, sodass *t* von 0,0 bei *z* = –*Radius* bis 1,0 bei *z* Radius ( t erhöht sich linear entlang der Linienlinien) und s von 0,0 an der positiven  =   y-Achse, auf 0,25 an der positiven X-Achse, auf 0,5 an der negativen y-Achse, auf 0,75 an der negativen x-Achse und zurück zu 1,0 an der positiven y-Achse. 

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

[**gluCylinder**](glucylinder.md)
</dt> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





