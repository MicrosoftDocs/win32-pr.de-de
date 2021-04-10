---
title: gludisk-Funktion (glu. h)
description: Die Funktion "gludisk" zeichnet einen Datenträger.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- gludisk-Funktion OpenGL
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
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040576"
---
# <a name="gludisk-function"></a>gludisk-Funktion

Die Funktion " **gludisk** " zeichnet einen Datenträger.

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

Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).

</dd> <dt>

*innerradius* 
</dt> <dd>

Der innere Radius des Datenträgers (kann NULL sein).

</dd> <dt>

*outerradius* 
</dt> <dd>

Der äußere Radius des Datenträgers.

</dd> <dt>

*aufs* 
</dt> <dd>

Die Anzahl der Unterteilungen um die z-Achse.

</dd> <dt>

*Loops* 
</dt> <dd>

Die Anzahl der konzentrischen Ringe für den Ursprung, in den der Datenträger unterteilt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gludisk** " rendert einen Datenträger auf der *z* = 0-Ebene. Der Datenträger weist einen Radius von *outerradius* auf und enthält eine konzentrische zirkuläre Lücke mit einem Radius von *innerradius*. Wenn *innerradius* 0 ist, wird kein Loch generiert. Der Datenträger ist um die z-Achse in Slices (z. b. Pizza Slices) und auch über die z-Achse in Ringe (wie von *Slices* bzw. *Schleifen* angegeben) unterteilt.

Im Hinblick auf die Ausrichtung wird die positive *z*-Seite des Datenträgers als *außerhalb* betrachtet (siehe [**gluquadricorientation**](gluquadricorientation.md)). Dies bedeutet Folgendes: Wenn die Ausrichtung auf "glu extern" festgelegt ist \_ , werden alle normalisieren generiert, die auf die positive z-Achse zeigen.

Wenn die Texturierung aktiviert ist (mit " [**gluquadrictexture**](gluquadrictexture.md)"), werden die Texturkoordinaten linear generiert, sodass *r*  =  *outerradius*, der Wert bei (*r*, 0, 0) ist (1, 0,5); bei (0, *r*, 0) ist er (0,5, 1); bei (-*r*, 0, 0) ist er (0, 0,5); und bei (0,-*r*, 0) ist er (0,5, 0).

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

 

 





