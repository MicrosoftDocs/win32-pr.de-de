---
title: glubegintrim-Funktion (glu. h)
description: Die Funktionen "glubegintrim" und "gluendtrim" begrenzen eine nicht einheitliche, nicht einheitliche rationelle B-Spline (NURBS)-Kürzungs Schleifen Definition. | glubegintrim-Funktion (glu. h)
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- glubegintrim-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluBeginTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84cbe5c1cd0cc68ee892d42fc60db05b6ae2bea6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366582"
---
# <a name="glubegintrim-function"></a>glubegintrim-Funktion

Die Funktionen " **glubegintrim** " und " [**gluendtrim**](gluendtrim.md) " begrenzen eine nicht einheitliche, nicht einheitliche rationelle B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md))-Kürzungs Schleifen Definition.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluBeginTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie " **glubegintrim** ", um den Anfang einer Kürzungs Schleife zu markieren, und " **gluendtrim** ", um das Ende einer Kürzungs Schleife zu markieren. Eine Kürzungs Schleife ist ein Satz orientierter Kurven Segmente (die eine geschlossene Kurve bilden), die Grenzen einer nursb-Oberfläche definieren. Sie fügen diese Kürzungs Schleifen in die Definition einer nursb-Oberfläche ein, zwischen den Aufrufen von " [**glubeginsurface**](glubeginsurface.md) " und " [**gluendsurface**](gluendsurface.md)".

Die Definition für eine nursb-Oberfläche kann viele Kürzungs Schleifen enthalten. Wenn Sie z. b. eine Definition für eine nurb-Oberfläche schreiben, die einem Rechteck mit einem ausgepunkteten Loch ähnelt, würde die Definition zwei Kürzungs Schleifen enthalten. Eine Schleife würde den äußeren Rand des Rechtecks definieren. die andere würde die ausgepunktete Lücke definieren. Die Definitionen der einzelnen Kürzungs Schleifen werden von einem " **glubegintrim**  /  **gluendtrim** "-paar in Klammern gesetzt.

Die Definition einer einzelnen geschlossenen Kürzungs Schleife kann aus mehreren Kurven Segmenten bestehen, die jeweils als eine Reihe von Liniensegmenten beschrieben werden, die eine lineare Kurve bilden (siehe [**glupwlcurve**](glupwlcurve.md)), als eine einzelne nurb-Kurve (siehe [**glunurbscurve**](glunurbscurve.md)) oder als eine Kombination aus beidem in beliebiger Reihenfolge. Die einzigen Bibliotheks Aufrufe, die in einer Kürzungs Schleifen Definition (zwischen den Aufrufen von " **glubegintrim** " und " **gluendtrim**") vorkommen können, sind " **glupwlcurve** " und " **glunurbscurve**".

Der angezeigte Bereich der nursb-Oberfläche ist die Region in der Domäne links neben der Kürzungs Kurve, wenn der Kurven Parameter zunimmt. Daher befindet sich der beibehaltene Bereich der nursb-Oberfläche in einer gegen Uhrzeigersinn enden Kürzungs Schleife und außerhalb einer umschneiderschleife im Uhrzeigersinn Für das zuvor erwähnte Rechteck wird die Kürzungs Schleife für den äußeren Rand des Rechtecks gegen den Uhrzeigersinn ausgeführt, während die Kürzungs Schleife für das ausgepunktete Loch im Uhrzeigersinn ausgeführt wird.

Wenn Sie mehr als eine Kurve verwenden, um eine einzelne Kürzungs Schleife zu definieren, müssen die Kurven Segmente eine geschlossene Schleife bilden (d. h., der Endpunkt jeder Kurve muss der Ausgangspunkt der nächsten Kurve sein, und der Endpunkt der abschließenden Kurve muss der Ausgangspunkt der ersten Kurve sein). Wenn die Endpunkte der Kurve ausreichend nah beieinander sind, aber nicht genau Coincident, werden Sie gezwungen, eine Übereinstimmung zu finden. Wenn die Endpunkte nicht ausreichend geschlossen sind, tritt ein Fehler auf (siehe [*glunurbscallback*](glunurbs.md)).

Wenn eine Kürzungs Schleifen Definition mehrere Kurven enthält, muss die Richtung der Kurven konsistent sein (d. h., der innere muss sich Links von allen Kurven befinden). Sie können schsted-Kürzungs Schleifen verwenden, wenn sich die Kurve der Kurve ordnungsgemäß ausweist. Das verkürzen von Kurven kann sich nicht selbst überschneiden, und Sie können sich auch nicht untereinander (oder ein Fehler Ergebnis) überschneiden.

Wenn keine Kürzungs Informationen für eine nursb-Oberfläche angegeben werden, wird die gesamte Oberfläche gezeichnet.

## <a name="examples"></a>Beispiele

Dieses Code Fragment definiert eine Kürzungs Schleife, die aus einer schrittweisen linearen Kurve und zwei nursb-Kurven besteht:

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

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

[**glubeginsurface**](glubeginsurface.md)
</dt> <dt>

[**gluendsurface**](gluendsurface.md)
</dt> <dt>

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[*glunurbscallback*](glunurbs.md)
</dt> <dt>

[**glunurbscurve**](glunurbscurve.md)
</dt> <dt>

[**glupwlcurve**](glupwlcurve.md)
</dt> </dl>

 

 





