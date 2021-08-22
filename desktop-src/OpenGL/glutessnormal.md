---
title: gluTessNormal-Funktion (Glu.h)
description: Die gluTessNormal-Funktion gibt eine Normale für ein Polygon an.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- gluTessNormal-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2db848c6971fe2893f2bc2cd4ca33e96811dda0d44e81e8a852cd441a6478d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488470"
---
# <a name="glutessnormal-function"></a>gluTessNormal-Funktion

Die **gluTessNormal-Funktion** gibt eine Normale für ein Polygon an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tess* 
</dt> <dd>

Das Mosaikobjekt (erstellt mit [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*x* 
</dt> <dd>

Die x-Koordinatenkomponente einer Normalen.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Koordinatenkomponente einer Normalen.

</dd> <dt>

*Z* 
</dt> <dd>

Die Z-Koordinatenkomponente einer Normalen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **funktion gluTessNormal** beschreibt eine normale für ein von Ihnen definiertes Polygon. Alle Eingabedaten werden auf eine Ebene projiziert, die einer der drei Koordinatenachsen vor dem Mosaik entspricht, und alle Ausgabedreiecke sind im Hinblick auf die Normalität gegen den Uhrzeigersinn ausgerichtet. (Um die Ausrichtung im Uhrzeigersinn zu erhalten, kehren Sie das Vorzeichen der angegebenen Normalen um.) Wenn Sie beispielsweise wissen, dass alle Polygone in der x-y-Ebene liegen, rufen Sie **gluTessNormal**(tess, 0.0, 0.0, 1.0) auf, bevor Sie Polygone rendern.

Wenn die angegebene Normaleinstellung (0,0, 0,0, 0,0) (Standardwert) ist, wird die Normalität wie folgt bestimmt:

1.  Die Richtung der Normalität bis zu ihrem Vorzeichen wird durch Anpassen einer Ebene an die Scheitelpunkte ermittelt, ohne zu berücksichtigen, wie die Scheitelpunkte verbunden sind. Es wird erwartet, dass die Eingabedaten ungefähr auf der Ebene liegen. Andernfalls kann die Projektion auf eine der drei Koordinatenachsen die Geometrie erheblich ändern.
2.  Das Vorzeichen der Normalen wird ausgewählt, sodass die Summe der signierten Bereiche aller Eingabekonturen nicht negativer Art ist (wobei eine Kontur gegen den Uhrzeigersinn über einen positiven Bereich verfügt).

Die angegebene Normalität bleibt erhalten, bis sie durch einen anderen Aufruf von **gluTessNormal** geändert wird.

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





