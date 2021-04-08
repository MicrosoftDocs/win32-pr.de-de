---
title: glutess normal-Funktion (glu. h)
description: Die Funktion "glutess normal" gibt eine normale für ein Polygon an.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- glutess normal-Funktion OpenGL
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
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957075"
---
# <a name="glutessnormal-function"></a>glutess normal-Funktion

Die Funktion " **glutess normal** " gibt eine normale für ein Polygon an.

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

*ATI* 
</dt> <dd>

Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).

</dd> <dt>

*x* 
</dt> <dd>

Die x-Koordinaten Komponente eines normalen.

</dd> <dt>

*y* 
</dt> <dd>

Die Komponente der y-Koordinate eines normalen.

</dd> <dt>

*z* 
</dt> <dd>

Die z-Koordinaten Komponente eines normalen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glutess normal** " beschreibt einen normalen Wert für ein Polygon, das Sie definieren. Alle Eingabedaten werden auf eine Ebene senkrecht zu einer der drei Koordinatenachsen vor dem Mosaik projiziert, und alle Ausgabe Dreiecke werden im Hinblick auf den normalen gegen den Uhrzeigersinn ausgerichtet. (Um die Ausrichtung im Uhrzeigersinn zu erhalten, umkehren Sie das Vorzeichen der angegebenen normal). Wenn Sie z. b. wissen, dass alle Polygone auf der x-y-Ebene liegen, nennen Sie " **glutess normal**(Tess, 0,0, 0,0, 1,0)", bevor Sie Polygone rendern.

Wenn der angegebene normale Wert (0,0, 0,0, 0,0) (Standardwert) ist, wird der normale Wert wie folgt bestimmt:

1.  Die Richtung der normalen, bis zu ihrem Vorzeichen, wird gefunden, indem eine Ebene an die Eckpunkte angepasst wird, ohne dass die vertexen miteinander verbunden sind. Es wird erwartet, dass die Eingabedaten ungefähr in der Ebene liegen. Andernfalls kann die Geometrie durch Projektion senkrecht zu einer der drei Koordinatenachsen erheblich geändert werden.
2.  Das Vorzeichen der normalen wird ausgewählt, sodass die Summe der signierten Bereiche aller Eingabe Konturen nicht negativ ist (wobei eine Kontur gegen den Uhrzeigersinn einen positiven Bereich aufweist).

Die angegebene normale bleibt **bestehen, bis** Sie von einem anderen aufgerufen wird.

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

[**glunewtess**](glunewtess.md)
</dt> <dt>

[**glutess beginpolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**glutessendpolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





