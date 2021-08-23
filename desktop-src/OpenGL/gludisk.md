---
title: gluDisk-Funktion (Glu.h)
description: Die gluDisk-Funktion zeichnet einen Datenträger.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- gluDisk-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83abb24f665cbcbf978a6423868751794371606cf412f609876a8f17d42c115a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489530"
---
# <a name="gludisk-function"></a>gluDisk-Funktion

Die **gluDisk-Funktion** zeichnet einen Datenträger.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*qobj* 
</dt> <dd>

Das Quadric-Objekt (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

Der innere Radius des Datenträgers (kann 0 (null) sein).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Der äußere Radius des Datenträgers.

</dd> <dt>

*Scheiben* 
</dt> <dd>

Die Anzahl der Unterteilungen um die Z-Achse.

</dd> <dt>

*Schleifen* 
</dt> <dd>

Die Anzahl der konzentrierten Ringe über den Ursprung, in den der Datenträger unterteilt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluDisk-Funktion** rendert einen Datenträger auf der *z* = 0-Ebene. Der Datenträger verfügt über einen Radius *von outerRadius* und enthält ein konzentriertes kreisförmiges Lücke mit einem Radius *von innerRadius*. Wenn *innerRadius* 0 ist, wird keine Lücke generiert. Der Datenträger wird um die Z-Achse in *Slices*(z. B. Pizzaslices) und auch um die Z-Achse in Ringe unterteilt (wie durch *Slices* bzw. Schleifen angegeben).

In Bezug auf die Ausrichtung wird die positive *z-Seite* des Datenträgers als außerhalb betrachtet *(siehe* [**gluQuadricOrientation**](gluquadricorientation.md)). Dies bedeutet, dass alle generierten Normals entlang der positiven Z-Achse zeigen, wenn die Ausrichtung auf GLU \_ OUTSIDE festgelegt ist.

Wenn die Texturierung aktiviert ist (mit [**gluQuadricTexture),**](gluquadrictexture.md)werden Texturkoordinaten linear generiert, wobei *r* outerRadius , der Wert  =  bei (*r*, 0, 0) ist (1, 0,5), bei (0, *r,* 0) ist es (0,5, 1), bei (-*r,* 0, 0) ist es (0, 0,5) und bei (0, -*r*, 0) ist es (0,5, 0).

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

 

 





