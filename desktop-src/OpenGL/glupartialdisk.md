---
title: gluPartialDisk-Funktion (Glu.h)
description: Die gluPartialDisk-Funktion zeichnet einen Bogen eines Datenträgers.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- gluPartialDisk-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 687738cce6bb311d7e8223877b716abdaef180340ab570f430659ee2e98458ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519440"
---
# <a name="glupartialdisk-function"></a>gluPartialDisk-Funktion

Die **gluPartialDisk-Funktion** zeichnet einen Bogen eines Datenträgers.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*qobj* 
</dt> <dd>

Ein Quadric-Objekt (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

Der innere Radius des partiellen Datenträgers (kann 0 (null) sein).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Der äußere Radius des partiellen Datenträgers.

</dd> <dt>

*Scheiben* 
</dt> <dd>

Die Anzahl der Unterteilungen um die Z-Achse.

</dd> <dt>

*Schleifen* 
</dt> <dd>

Die Anzahl der konzentrierten Ringe um den Ursprung, in den der partielle Datenträger unterteilt ist.

</dd> <dt>

*Startangle* 
</dt> <dd>

Der Anfangswinkel des Datenträgeranteils in Grad.

</dd> <dt>

*Sweepangle* 
</dt> <dd>

Der Sweepwinkel des Datenträgeranteils in Grad.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluPartialDisk-Funktion** rendert einen Teildatenträger auf der *z* = 0-Ebene. Ein Teildatenträger ähnelt einem vollständigen Datenträger, mit der Ausnahme, dass nur die Teilmenge des Datenträgers von *startAngle* bis *startAngle* sweepAngle enthalten ist (wobei 0 Grad entlang der positiven y-Achse, 90 Grad entlang der positiven  +   X-Achse, 180 Grad entlang der negativen y-Achse und 270 Grad entlang der negativen X-Achse liegt).

Der partielle Datenträger hat einen Radius von *outerRadius* und enthält eine konzentrierte kreisförmige Lücke mit einem Radius *von innerRadius*. Wenn *innerRadius* 0 (null) ist, wird keine Lücke generiert. Der Teildatenträger wird um die Z-Achse in *Slices*(z. B. Pizzaslices) und auch über die Z-Achse in Ringe unterteilt (wie durch *Slices* bzw. Schleifen angegeben).

In Bezug auf die Ausrichtung wird die positive Z-Seite des partiellen Datenträgers als außerhalb des Datenträgers betrachtet (siehe [**gluQuadricOrientation**](gluquadricorientation.md)). Dies bedeutet, dass alle generierten Normals entlang der positiven Z-Achse zeigen, wenn die Ausrichtung auf GLU \_ OUTSIDE festgelegt ist.

Wenn Sie die Texturierung (mit [**gluQuadricTexture)**](gluquadrictexture.md)aktiviert haben, generiert **gluPartialDisk** Texturkoordinaten linear so, dass bei *r*  =  *outerRadius* der Wert bei (*r*, 0, 0) ist (1, 0,5); bei (0, *r,* 0) ist es (0,5, 1), bei (*r*, 0, 0) ist es (0, 0,5) und bei (0, *r*, 0) ist es (0,5, 0).

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

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





