---
title: gluCylinder-Funktion (Glu.h)
description: Die gluCylinder-Funktion zeichnet einen Zylinder.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- gluCylinder-Funktion OpenGL
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
ms.openlocfilehash: 1a09ff92aec17a13f03ecb1cbaaf118398b2b88dea76936454d527bb9c37032f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061608"
---
# <a name="glucylinder-function"></a>gluCylinder-Funktion

Die **gluCylinder-Funktion** zeichnet einen Zylinder.

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

Das Quadric-Objekt (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*baseRadius* 
</dt> <dd>

Der Radius des Zylinders bei *z* = 0.

</dd> <dt>

*topRadius* 
</dt> <dd>

Der Radius des Zylinders in *z*  =  *Höhe*.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Zylinders.

</dd> <dt>

*Scheiben* 
</dt> <dd>

Die Anzahl der Unterteilungen um die Z-Achse.

</dd> <dt>

*Stacks* 
</dt> <dd>

Die Anzahl der Unterteilungen entlang der Z-Achse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluCylinder-Funktion** zeichnet einen Zylinder, der entlang der Z-Achse ausgerichtet ist. Die Basis des Zylinders wird bei *z* = 0 und die obere bei *z Höhe*  =  *platziert.* Wie eine Kugel wird ein Zylinder um die Z-Achse in Slices und entlang der Z-Achse in Stapel unterteilt.

Beachten Sie, dass diese Routine einen Kegel generiert, wenn *topRadius* auf 0 festgelegt ist.

Wenn die Ausrichtung auf GLU \_ OUTSIDE (mit [**gluQuadricOrientation)**](gluquadricorientation.md)festgelegt ist, zeigen alle generierten Normals von der Z-Achse ab. Andernfalls zeigen sie auf die Z-Achse.

Wenn die Texturierung aktiviert ist (mit [**gluQuadricTexture):**](gluquadrictexture.md)Texturkoordinaten werden generiert, sodass *t* linear von 0,0 bei *z* = 0 bis 1,0 bei *z* Höhe und s im Bereich  =  von 0,0 an der positiven y-Achse liegt. auf 0,25 an der positiven X-Achse, auf 0,5 an der negativen y-Achse, auf 0,75 an der negativen x-Achse und zurück zu 1,0 an der positiven y-Achse. 

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

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





