---
title: glupartialdisk-Funktion (glu. h)
description: Die Funktion "glupartialdisk" zeichnet einen Bogen eines Datenträgers.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- glupartialdisk-Funktion OpenGL
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
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337283"
---
# <a name="glupartialdisk-function"></a>glupartialdisk-Funktion

Die Funktion " **glupartialdisk** " zeichnet einen Bogen eines Datenträgers.

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

Ein quadktobjekt (mit [**glunewquadric**](glunewquadric.md)erstellt).

</dd> <dt>

*innerradius* 
</dt> <dd>

Der innere Radius des partiellen Datenträgers (kann NULL sein).

</dd> <dt>

*outerradius* 
</dt> <dd>

Der äußere Radius des partiellen Datenträgers.

</dd> <dt>

*aufs* 
</dt> <dd>

Die Anzahl der Unterteilungen um die z-Achse.

</dd> <dt>

*Loops* 
</dt> <dd>

Die Anzahl der konzentrischen Ringe für den Ursprung, in den der Teil Datenträger unterteilt wird.

</dd> <dt>

*Start Angle* 
</dt> <dd>

Der Anfangs Winkel (in Grad) des Datenträger Teils.

</dd> <dt>

*sweepAngle* 
</dt> <dd>

Der Mittelpunktswinkel des Datenträger Teils in Grad.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glupartialdisk** " rendert einen partiellen Datenträger auf der *z* = 0-Ebene. Ein Teil Datenträger ähnelt einem vollständigen Datenträger, mit dem Unterschied, dass nur die Teilmenge des Datenträgers von *startAngle* über *startAngle*  +  *sweepAngle* enthalten ist (wobei 0 Grad entlang der positiven y-Achse liegt, 90 Grad entlang der positiven x-Achse, 180 Grad entlang der negativen y-Achse und 270 Grad entlang der negativen x-Achse).

Der Teil Datenträger weist einen Radius von *outerradius* auf und enthält eine konzentrische zirkuläre Lücke mit einem Radius von *innerradius*. Wenn *innerradius* gleich 0 (null) ist, wird kein Loch generiert. Der Teil Datenträger wird um die z-Achse in Slices (z. b. Pizza Slices) und auch über die z-Achse in Ringe (wie von *Slices* bzw. *Schleifen* angegeben) unterteilt.

Im Hinblick auf die Ausrichtung wird die positive z-Seite des partiellen Datenträgers als außerhalb betrachtet (siehe [**gluquadricorientation**](gluquadricorientation.md)). Dies bedeutet Folgendes: Wenn die Ausrichtung auf "glu extern" festgelegt ist \_ , werden alle normalisieren generiert, die auf die positive z-Achse zeigen.

Wenn Sie die Texturierung (mit " [**gluquadrictexture**](gluquadrictexture.md)") aktiviert haben, generiert " **glupartialdisk** " die Texturkoordinaten linear, sodass *r*  =  *outerradius*, der Wert bei (*r*, 0, 0) ist (1, 0,5); bei (0, *r*, 0) ist es (0,5, 1); bei (*r*, 0, 0) ist es (0, 0,5); und bei (0, *r*, 0) ist es (0,5, 0).

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

[**gluquadricorientation**](gluquadricorientation.md)
</dt> <dt>

[**gluquadrictexture**](gluquadrictexture.md)
</dt> <dt>

[**glusphere**](glusphere.md)
</dt> </dl>

 

 





