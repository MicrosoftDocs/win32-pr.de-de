---
title: gluEndTrim-Funktion (Glu.h)
description: Die Funktionen gluBeginTrim und gluEndTrim begrenzen eine Non-Uniform Rational B-Spline -Schleifendefinition (NON-Uniform Rational B-Spline, NURBS). | gluEndTrim-Funktion (Glu.h)
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- gluEndTrim-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e47f1ef8a1dcbeef4bc2d582699556a87d39a786b36c01a6de930fcfbd9a6b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612946"
---
# <a name="gluendtrim-function"></a>gluEndTrim-Funktion

Die [**Funktionen gluBeginTrim**](glubegintrim.md) und **gluEndTrim** begrenzen eine nicht einheitliche rationale B-Spline-Schleifendefinition [(NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluEndTrim(
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

Verwenden [**Sie gluBeginTrim,**](glubegintrim.md) um den Anfang einer Kürzungsschleife zu markieren, und **gluEndTrim,** um das Ende einer Kürzungsschleife zu markieren. Eine Kürzungsschleife ist ein Satz von ausgerichteten Kurvensegmenten (die eine geschlossene Kurve bilden), die Grenzen einer NURBS-Oberfläche definieren. Sie schließen diese Kürzungsschleifen in die Definition einer NURBS-Oberfläche zwischen Aufrufen von [**gluBeginSurface**](glubeginsurface.md) und [**gluEndSurface ein.**](gluendsurface.md)

Die Definition für eine NURBS-Oberfläche kann viele Kürzungsschleifen enthalten. Wenn Sie z. B. eine Definition für eine NURBS-Oberfläche schreiben, die einem Rechteck ähnelt, bei dem eine Lücke herausgeschnitten ist, enthält die Definition zwei Kürzungsschleifen. Eine Schleife würde den äußeren Rand des Rechtecks definieren. Die andere würde die geerbte Lücke definieren. Die Definitionen jeder dieser Kürzungsschleifen würden durch ein [**gluBeginTrim-gluEndTrim-Paar**](glubegintrim.md)in  /  **Klammern** gesetzt werden.

Die Definition einer einzelnen geschlossenen Kürzungsschleife kann aus mehreren Kurvensegmenten bestehen, die jeweils als eine Reihe von Liniensegmenten beschrieben werden, die eine lineare Kurve bilden (siehe [**gluPwlCurve),**](glupwlcurve.md)als einzelne NURBS-Kurve (siehe [**gluNurbsCurve)**](glunurbscurve.md)oder als Eine Kombination aus beidem in beliebiger Reihenfolge. Die einzigen Bibliotheksaufrufe, die in einer Trimmingschleifendefinition (zwischen den Aufrufen von [**gluBeginTrim**](glubegintrim.md) und **gluEndTrim)** auftreten können, sind **gluPwlCurve** und **gluNurbsCurve.**

Der angezeigte Bereich der NURBS-Oberfläche ist der Bereich in der Domäne links von der Kürzungskurve, wenn der Kurvenparameter zunimmt. Daher befindet sich der beibehaltene Bereich der NURBS-Oberfläche innerhalb einer kürzungsschleife gegen den Uhrzeigersinn und außerhalb einer Kürzungsschleife im Uhrzeigersinn. Für das zuvor erwähnte Rechteck wird die Kürzungsschleife für den äußeren Rand des Rechtecks gegen den Uhrzeigersinn ausgeführt, während die Kürzungsschleife für die gerundete Lücke im Uhrzeigersinn ausgeführt wird.

Wenn Sie mehr als eine Kurve verwenden, um eine einzelne Kürzungsschleife zu definieren, müssen die Kurvensegmente eine geschlossene Schleife bilden (d. h., der Endpunkt jeder Kurve muss der Ausgangspunkt der nächsten Kurve sein, und der Endpunkt der endgültigen Kurve muss der Ausgangspunkt der ersten Kurve sein). Wenn die Endpunkte der Kurve ausreichend nah beieinander liegen, aber nicht genau zufällig sind, müssen sie übereinstimmen. Wenn die Endpunkte nicht ausreichend nah sind, tritt ein Fehler auf (siehe [*gluNurbsCallback*](glunurbs.md)).

Wenn eine Trimmingschleifendefinition mehrere Kurven enthält, muss die Richtung der Kurven konsistent sein (d. h., das Innere muss links von allen Kurven sein). Sie können geschachtelte Kürzungsschleifen verwenden, solange sich die Kurvenausrichtungen ordnungsgemäß abwechseln. Das Kürzen von Kurven darf weder sich selbst überschneidend sein, noch können sie sich überschneiden (oder zu einem Fehler führen).

Wenn für eine NURBS-Oberfläche keine Kürzungsinformationen angegeben werden, wird die gesamte Oberfläche gezeichnet.

## <a name="examples"></a>Beispiele

Dieses Codefragment definiert eine Kürzungsschleife, die aus einer stückweise linearen Kurve und zwei NURBS-Kurven besteht:

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



## <a name="see-also"></a>Weitere Informationen

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

 

 





