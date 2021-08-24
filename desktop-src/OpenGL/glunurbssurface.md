---
title: gluNurbsSurface-Funktion (Glu.h)
description: Die gluNurbsSurface-Funktion definiert die Form einer Non-Uniform Rational B-Spline (NURBS)-Oberfläche.
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- gluNurbsSurface-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50f56232ac891cbdfba18195741d875ecc5436112772ed4fa665903374e96602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554190"
---
# <a name="glunurbssurface-function"></a>gluNurbsSurface-Funktion

Die **gluNurbsSurface-Funktion** definiert die Form einer nicht einheitlichen rationalen B-Spline-Oberfläche [(NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*sknot \_ count* 
</dt> <dd>

Die Anzahl der Läuter in *parametrischer Richtung.*

</dd> <dt>

*sknot* 
</dt> <dd>

Ein Array von *sknot \_ count* nondecreasing-Werte in der parametrischen *u-Richtung.*

</dd> <dt>

*tknot \_ count* 
</dt> <dd>

Die Anzahl von Löchern in *parametrischer* v-Richtung.

</dd> <dt>

*tknot* 
</dt> <dd>

Ein Array von *tknot \_ count* nondecreasing-Werte in der parametrischen *v-Richtung.*

</dd> <dt>

*s \_ stride* 
</dt> <dd>

Der Offset (als Eine-Genauigkeit-Gleitkommawerte) zwischen aufeinander folgenden Kontrollpunkten in der parametrischen *u-Richtung* in *ctlarray*.

</dd> <dt>

*t \_ stride* 
</dt> <dd>

Der Offset (in Gleitkommawerten mit einfacher Genauigkeit) zwischen aufeinander folgenden Kontrollpunkten in parametrischer *v-Richtung* in *CTLARRAY.*

</dd> <dt>

*ctlarray* 
</dt> <dd>

Ein Array, das Steuerungspunkte für die NURBS-Oberfläche enthält. Die Offsets zwischen aufeinander folgenden Kontrollpunkten in den parametrischen *u-* und *v-Richtungen* werden durch s *\_ stride* und t *\_ stride* angegeben.

</dd> <dt>

*sorder* 
</dt> <dd>

Die Reihenfolge der NURBS-Oberfläche  in parametrischer u-Richtung. Die Reihenfolge ist eins mehr als der Grad, sodass eine kubische Oberfläche in *u* eine *u-Reihenfolge* von 4 aufweist.

</dd> <dt>

*torder* 
</dt> <dd>

Die Reihenfolge der NURBS-Oberfläche in *parametrischer v-Richtung.* Die Reihenfolge ist eins mehr als der Grad, sodass eine kubische Oberfläche in *v* eine *v-Reihenfolge* von 4 aufweist.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Oberfläche. Der *Typparameter* kann jeder gültige zweidimensionale Auswertungstyp sein (z. B. GL \_ MAP2 \_ VERTEX \_ 3 oder GL \_ MAP2 \_ COLOR \_ 4).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie **gluNurbsSurface** innerhalb einer NURBS-Oberflächendefinition, um die Form einer NURBS-Oberfläche (vor dem Kürzen) zu beschreiben. Um den Anfang einer NURBS-Oberflächendefinition zu markieren, verwenden Sie die [**gluBeginSurface-Funktion.**](glubeginsurface.md) Um das Ende einer NURBS-Oberflächendefinition zu markieren, verwenden Sie die [**gluEndSurface-Funktion.**](gluendsurface.md) Rufen Sie **gluNurbsSurface** nur innerhalb einer NURBS-Oberflächendefinition auf.

Sie ordnen Positions-, Textur- und Farbkoordinaten einer Oberfläche zu, indem Sie sie als separate **gluNurbsSurface** zwischen einem **gluBeginSurface** / **gluEndSurface-Paar** darstellen. Innerhalb eines einzelnen **gluBeginSurface** / **gluEndSurface-Paars** können Sie **gluNurbsSurface** nur einen Aufruf für Farb-, Positions- und Texturdaten ausführen. Nehmen Sie genau einen Aufruf vor, um die Position der Oberfläche zu beschreiben (ein *Typ* von GL \_ MAP2 \_ VERTEX \_ 3 oder GL \_ MAP2 \_ VERTEX \_ 4).

Sie können eine NURBS-Oberfläche mithilfe der Funktionen [**gluNurbsCurve**](glunurbscurve.md) und [**gluPwlCurve**](glupwlcurve.md) zwischen Aufrufen von [**gluBeginTrim**](glubegintrim.md) und [**gluEndTrim kürzen.**](gluendtrim.md)

Ein **gluNurbsSurface** mit *sknot count-Zählern \_* in *u-Richtung* und *tknot count-Zählern \_* in *v-Richtung* mit *Bestellungen sorder* und *torder* muss (*sknot \_ count*  - *sorder*) multipied by (*tknot \_ count*  - *torder*) Steuerungspunkte aufweisen.

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

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





