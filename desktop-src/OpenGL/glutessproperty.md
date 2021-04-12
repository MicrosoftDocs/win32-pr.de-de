---
title: glutessproperty-Funktion (glu. h)
description: Die Funktion "glutessproperty" legt die-Eigenschaft eines Mosaik Objekts fest.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- glutessproperty-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105897"
---
# <a name="glutessproperty-function"></a>glutessproperty-Funktion

Die Funktion " **glutessproperty** " legt die-Eigenschaft eines Mosaik Objekts fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ATI* 
</dt> <dd>

Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).

</dd> <dt>

*,* 
</dt> <dd>

Der festzulegende Eigenschaftswert. Die folgenden Werte sind gültig: die \_ Regel "glu Tess" \_ , " \_ glu Tess" und " \_ \_ \_ glu- \_ Toleranz" \_ .



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <dt>**Glu \_ - \_ aufwickungsregel \_**</dt> </dl>    | Bestimmt, welche Teile des Polygons sich im Inneren befinden. Der value-Parameter kann auf einen der folgenden Werte festgelegt werden: glu \_ Tess \_ \_ , ungerade, Glu Tess \_ Winding ungleich \_ \_ NULL, Glu \_ Tess \_ Winding \_ positiv, Glu \_ Tess \_ Winding \_ negative oder glu \_ Tess \_ Winding \_ ABS \_ GEQ \_ Two. <br/> Um zu verstehen, wie die Regel für die Regel funktioniert, sollten Sie zuerst berücksichtigen, dass die Eingabe Kontur die Ebene in Regionen partitioniert. Die Wicklungs Regel bestimmt, welche dieser Regionen sich innerhalb des Polygons befinden.<br/> Bei einer Einzel Kontur-c ist die Zahl von x Punkt x einfach die signierte Anzahl von Umdrehungen, die wir ungefähr x durchführen, während wir einmal um c herumreisen (wobei gegen den Uhrzeigersinn positiv ist). Wenn mehrere Kontur vorhanden sind, werden die einzelnen aufwicklungs Zahlen summiert. Diese Prozedur ordnet jedem Punkt x in der Ebene einen ganzzahligen Wert mit Vorzeichen zu. Beachten Sie, dass die Anzahl der Wicklungen für alle Punkte in einer einzelnen Region identisch ist.<br/> Die Wicklungs Regel klassifiziert einen Bereich als "innen", wenn die zugehörige Zahl zur ausgewählten Kategorie gehört (ungerade, nicht NULL, positiv, negativ oder absoluter Wert von mindestens zwei). Der vorherige glu-Mosaik Speicher (vor der Verwendung von Glu 1,2) hat die Regel "ungerade" verwendet. Die Regel "nicht NULL" (GLU \_ Tess \_ \_ , nicht null) ist eine andere gängige Methode zum Definieren des Inneren. Die anderen drei Regeln ( \_ atentess \_ Winding \_ positiv, Glu \_ Tess \_ Winding \_ negativ, Glu \_ Tess \_ Winding \_ ABS \_ GEQ \_ Two) eignen sich für Polygon-CSG-Vorgänge.<br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <dt>**nur die Grenze von Glu \_ Tess \_ \_**</dt> </dl> | Gibt einen booleschen Wert an (legen Sie den Wert auf GL \_ true oder GL \_ false fest). Wenn Sie Value auf den Wert "GL true" festlegen \_ , wird anstelle eines Mosaik Satzes eine Reihe geschlossener Kontur zurückgegeben, die das Polygon innere und das äußere trennt. Äußere Kontur werden im Uhrzeigersinn gegen den Uhrzeigersinn ausgerichtet. innere Kontur werden im Uhrzeigersinn ausgerichtet. Die \_ \_ Daten Rückrufe von Glu Tess BEGIN und glu \_ Tess \_ \_ verwenden die Type GL- \_ Zeilen \_ Schleife für jede Kontur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <dt>**Glu \_ Tess- \_ Toleranz**</dt> </dl>              | Gibt eine Toleranz für das Zusammenführen von Features an, um die Größe der Ausgabe zu verringern. Beispielsweise können zwei vertexen, die sich sehr nahe beieinander befinden, durch einen einzelnen Scheitelpunkt ersetzt werden. Die Toleranz wird mit der größten Koordinaten Größe eines beliebigen Eingabe Vertex multipliziert. Gibt den maximalen Abstand an, den ein beliebiges Feature als Ergebnis eines einzelnen zusammenlaufvorgangs verschieben kann. Wenn eine einzelne Funktion an mehreren Merge-Vorgängen beteiligt ist, kann die gesamte verschoderte Entfernung größer sein. <br/> Das Zusammenführen von Funktionen ist vollständig optional. die Toleranz ist nur ein Hinweis. Die Implementierung kann in einigen Fällen zusammengeführt werden, nicht in anderen, oder es werden niemals Features überhaupt zusammengeführt. Die Standardtoleranz ist 0 (null).<br/> Die aktuelle Implementierung führt Eckpunkte nur dann zusammen, wenn Sie unabhängig von der aktuellen Toleranz genau Coincident sind. Ein Scheitelpunkt wird nur dann in einen Edge gesplitet, wenn die Implementierung nicht unterscheiden kann, auf welcher Seite der Kante der Scheitelpunkt liegt. Zwei Ränder werden nur zusammengeführt, wenn beide Endpunkte identisch sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

*value* 
</dt> <dd>

Der Wert der angegeben Eigenschaft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glutessproperty** " steuert Eigenschaften, die in einem Mosaik Objekt gespeichert sind. Diese Eigenschaften beeinflussen die Art und Weise, wie Polygone interpretiert und gerendert werden.

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

[**"glugettessproperty"**](glugettessproperty.md)
</dt> <dt>

[**glunewtess**](glunewtess.md)
</dt> </dl>

 

 





