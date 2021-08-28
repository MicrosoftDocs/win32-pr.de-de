---
title: gluBeginTrim-Funktion (Glu.h)
description: Die Funktionen gluBeginTrim und gluEndTrim begrenzen eine NurBS-Schleifendefinition (Non-Uniform Rational B-Spline). | gluBeginTrim-Funktion (Glu.h)
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- gluBeginTrim-Funktion OpenGL
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
ms.openlocfilehash: bebf103a2476aa856b55319e0eca42b8708da169fcedb34e48362062689727ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937883"
---
# <a name="glubegintrim-function"></a>gluBeginTrim-Funktion

Die Funktionen **gluBeginTrim** und [**gluEndTrim**](gluendtrim.md) grenzen eine nicht einheitliche rationale B-Spline -Trimmungsschleifendefinition [(NURBS)](using-nurbs-curves-and-surfaces.md)ab.

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

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie **gluBeginTrim,** um den Anfang einer Kürzungsschleife zu markieren, und **gluEndTrim,** um das Ende einer Kürzungsschleife zu markieren. Eine Kürzungsschleife ist eine Reihe von orientierten Kurvensegmenten (die eine geschlossene Kurve bilden), die Grenzen einer NURBS-Oberfläche definieren. Sie schließen diese Kürzungsschleifen in die Definition einer NURBS-Oberfläche zwischen Aufrufen von [**gluBeginSurface**](glubeginsurface.md) und [**gluEndSurface**](gluendsurface.md)ein.

Die Definition für eine NURBS-Oberfläche kann viele Kürzungsschleifen enthalten. Wenn Sie z. B. eine Definition für eine NURBS-Oberfläche schreiben, die einem Rechteck ähnelt, in dem ein Löcher ausgeschnitten ist, enthält die Definition zwei Kürzungsschleifen. Eine Schleife würde den äußeren Rand des Rechtecks definieren. der andere würde die abgeschrämpfte Lücke definieren. Die Definitionen jeder dieser Kürzungsschleifen werden durch ein **gluBeginTrim**  /  **gluEndTrim-Paar** in Klammern gesetzt.

Die Definition einer einzelnen geschlossenen Kürzungsschleife kann aus mehreren Kurvensegmenten bestehen, die jeweils als eine Reihe von Liniensegmenten beschrieben werden, die eine lineare Kurve bilden (siehe [**gluPwlCurve),**](glupwlcurve.md)als einzelne NURBS-Kurve (siehe [**gluNurbsCurve**](glunurbscurve.md)) oder als Kombination aus beiden in beliebiger Reihenfolge. Die einzigen Bibliotheksaufrufe, die in einer Trimmingschleifendefinition (zwischen den Aufrufen von **gluBeginTrim** und **gluEndTrim)** angezeigt werden können, sind **gluPwlCurve** und **gluNurbsCurve.**

Der angezeigte Bereich der NURBS-Oberfläche ist der Bereich in der Domäne links neben der Kürzungskurve, wenn der Kurvenparameter zunimmt. Daher befindet sich der beibehaltene Bereich der NURBS-Oberfläche innerhalb einer Kürzungsschleife gegen den Uhrzeigersinn und außerhalb einer Kürzungsschleife im Uhrzeigersinn. Für das zuvor erwähnte Rechteck wird die Kürzungsschleife für den äußeren Rand des Rechtecks gegen den Uhrzeigersinn ausgeführt, während die Kürzungsschleife für die ausgeschnittene Lücke im Uhrzeigersinn ausgeführt wird.

Wenn Sie mehr als eine Kurve verwenden, um eine einzelne Kürzungsschleife zu definieren, müssen die Kurvensegmente eine geschlossene Schleife bilden (das heißt, der Endpunkt jeder Kurve muss der Ausgangspunkt der nächsten Kurve sein, und der Endpunkt der endgültigen Kurve muss der Ausgangspunkt der ersten Kurve sein). Wenn die Endpunkte der Kurve ausreichend nah beieinander liegen, aber nicht genau zufällig sind, werden sie zur Übereinstimmung gezwungen. Wenn die Endpunkte nicht ausreichend nahe sind, tritt ein Fehler auf (siehe [*gluNurbsCallback*](glunurbs.md)).

Wenn eine Trimmingschleifendefinition mehrere Kurven enthält, muss die Richtung der Kurven konsistent sein (d.b. das innere muss links von allen Kurven liegen). Sie können geschachtelte Kürzungsschleifen verwenden, solange die Kurvenausrichtung ordnungsgemäß abweicht. Kürzungskurven dürfen sich nicht selbst überschneiden, und sie können sich nicht überschneiden (oder es tritt ein Fehler auf).

Wenn für eine NURBS-Oberfläche keine Kürzungsinformationen angegeben werden, wird die gesamte Oberfläche gezeichnet.

## <a name="examples"></a>Beispiele

Dieses Codefragment definiert eine Kürzungsschleife, die aus einer schrittweisen linearen Kurve und zwei NURBS-Kurven besteht:

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
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





