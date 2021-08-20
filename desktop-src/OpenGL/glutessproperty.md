---
title: gluTessProperty-Funktion (Glu.h)
description: Die gluTessProperty-Funktion legt die -Eigenschaft eines Mosaikobjekts fest.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- gluTessProperty-Funktion OpenGL
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
ms.openlocfilehash: 595139b91e0fb19ac6ef479831604663dea1981e401aa807ba2bb3cd24a29a41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488430"
---
# <a name="glutessproperty-function"></a>gluTessProperty-Funktion

Die **gluTessProperty-Funktion** legt die -Eigenschaft eines Mosaikobjekts fest.

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

*Tess* 
</dt> <dd>

Das Mosaikobjekt (erstellt mit [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*welche* 
</dt> <dd>

Der festzulegende Eigenschaftswert. Die folgenden Werte sind gültig: GLU \_ TESS \_ WINDING \_ RULE, GLU \_ TESS \_ BOUNDARY ONLY und GLU \_ \_ TESS \_ TOLERANCE.



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <dt>**GLU \_ TESS \_ WINDING \_ RULE**</dt> </dl>    | Bestimmt, welche Teile des Polygons sich im Inneren befinden. Der Value-Parameter kann auf eine der folgenden Werte festgelegt werden: GLU \_ TESS \_ WINDING \_ ODD, GLU \_ TESS \_ WINDING \_ NONZERO, GLU \_ TESS \_ WINDING \_ POSITIVE, GLU \_ TESS \_ WINDING \_ NEGATIVE oder GLU \_ TESS \_ WINDING ABS \_ \_ GEQ \_ TWO. <br/> Um zu verstehen, wie die Wickelregel funktioniert, berücksichtigen Sie zunächst, dass die Eingabe die Ebene in Regionen unterteilt. Die Ziehregel bestimmt, welche dieser Regionen sich innerhalb des Polygons befinden.<br/> Für ein einzelnes konturierendes C ist die Ziehnummer eines Punkts x einfach die signierte Anzahl von Revolutionen, die wir um x drehen, während wir einmal um C herum reisen (wobei gegen den Uhrzeigersinn positiv ist). Wenn mehrere Konturen vorhanden sind, werden die einzelnen Ziehzahlen summiert. Diese Prozedur ordnet jedem Punkt x auf der Ebene einen ganzzahligen Wert mit Vorzeichen zu. Beachten Sie, dass die Wickelnummer für alle Punkte in einer einzelnen Region identisch ist.<br/> Die Ziehregel klassifiziert einen Bereich als "innerhalb", wenn seine Ziehnummer zur ausgewählten Kategorie gehört (ungerade, ungleich Null, positiv, negativ oder absoluter Wert von mindestens zwei). Der vorherige GLU-Mosaikator (vor GLU 1.2) verwendete die "ungerade" Regel. Die Regel "ungleich 0" (GLU \_ TESS \_ WINDING \_ NONZERO) ist eine weitere gängige Methode zum Definieren des Inneren. Die anderen drei Regeln (GLU \_ TESS \_ WINDING \_ POSITIVE, GLU \_ TESS \_ WINDING \_ NEGATIVE, GLU \_ TESS \_ WINDING \_ ABS \_ GEQ \_ TWO) sind für Polygon-CSG-Vorgänge nützlich.<br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <dt>**\_NUR GLU-TESS-GRENZE \_ \_**</dt> </dl> | Gibt einen booleschen Wert an (legen Sie den Wert auf GL \_ TRUE oder GL FALSE \_ fest). Wenn Sie den Wert auf GL \_ TRUE festlegen, wird anstelle eines Mosaiks eine Reihe geschlossener Konturen zurückgegeben, die das Polygoninnere und das äußere Polygon trennen. Äußere Konturen sind im Hinblick auf die Normalität gegen den Uhrzeigersinn ausgerichtet; Innere Konturen sind im Uhrzeigersinn ausgerichtet. Die \_ RÜCKRUFE GLU TESS \_ BEGIN und GLU \_ TESS \_ BEGIN DATA verwenden für jede \_ Kontur den Typ GL LINE \_ \_ LOOP.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <dt>**GLU \_ TESS \_ TOLERANCE**</dt> </dl>              | Gibt eine Toleranz für das Zusammenführen von Features an, um die Größe der Ausgabe zu reduzieren. Beispielsweise können zwei Scheitelpunkte, die sehr nah beieinander liegen, durch einen einzelnen Scheitelpunkt ersetzt werden. Die Toleranz wird mit der größten Koordinatengröße jedes Eingabevertex multipliziert. gibt den maximalen Abstand an, den jedes Feature als Ergebnis eines einzelnen Mergevorgangs verschieben kann. Wenn ein einzelnes Feature an mehreren Zusammenführungsvorgängen teilnimmt, kann der verschobene Gesamtabstand größer sein. <br/> Das Zusammenführen von Features ist vollständig optional. Die Toleranz ist nur ein Hinweis. Die Implementierung kann in einigen Fällen und nicht in anderen Fällen zusammengeführt werden, oder Funktionen können nie zusammengeführt werden. Die Standardtoleranz ist 0 (null).<br/> Die aktuelle Implementierung führt Scheitelpunkte nur zusammen, wenn sie unabhängig von der aktuellen Toleranz genau zufällig sind. Ein Scheitelpunkt wird nur dann in eine Kante aufgeteilt, wenn die Implementierung nicht unterscheiden kann, auf welcher Seite des Edges sich der Scheitelpunkt befindet. Zwei Kanten werden nur zusammengeführt, wenn beide Endpunkte identisch sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

*value* 
</dt> <dd>

Der Wert der angegebenen Eigenschaft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluTessProperty-Funktion** steuert Eigenschaften, die in einem Mosaikobjekt gespeichert sind. Diese Eigenschaften wirken sich darauf aus, wie die Polygone interpretiert und gerendert werden.

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

[**gluGetTessProperty**](glugettessproperty.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> </dl>

 

 





