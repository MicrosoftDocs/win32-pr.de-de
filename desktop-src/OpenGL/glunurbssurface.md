---
title: glunurbssurface-Funktion (glu. h)
description: Die Funktion "glunurbssurface" definiert die Form einer nicht einheitlichen Oberfläche von rationalem B-Spline (NURBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- glunurbssurface-Funktion OpenGL
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
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949392"
---
# <a name="glunurbssurface-function"></a>glunurbssurface-Funktion

Die Funktion " **glunurbssurface** " definiert die Form einer nicht einheitlichen Oberfläche von rationalem B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)).

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

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> <dt>

*Anzahl von SKUs \_* 
</dt> <dd>

Die Anzahl der Knoten in der Richtung der parametrischen *u* .

</dd> <dt>

*sknot* 
</dt> <dd>

Ein Array von *sknot \_ count* -Werten, die sich in der parametrischen *u* -Richtung nicht verkleinern.

</dd> <dt>

*\_tknotenanzahl* 
</dt> <dd>

Die Anzahl der Knoten in der parametrischen *v* -Richtung.

</dd> <dt>

*tknot* 
</dt> <dd>

Ein Array von *tknot \_* -Werten, die sich in der parametrischen *v* -Richtung nicht verkleinern.

</dd> <dt>

*s \_ Stride* 
</dt> <dd>

Der Offset (als eine Reihe einzelner Werte für den Wert für die Genauigkeit) zwischen aufeinander folgenden Steuerungs Punkten in der parametrisierten *u* -Richtung in *ctlarray*.

</dd> <dt>

*t \_ Stride* 
</dt> <dd>

Der Offset (in einzelnen Werten mit Werten für den Gleit Komma Wert) zwischen aufeinander folgenden Kontrollpunkten in der parametrisierten *v* -Richtung in *ctlarray*.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Ein Array, das Steuerungs Punkte für die nursb-Oberfläche enthält. Die Offsets zwischen aufeinander folgenden Kontrollpunkten in den parametrischen *u* -und *v* -Richtungen werden von *s \_ Stride* und *t \_ Stride* angegeben.

</dd> <dt>

*sorder* 
</dt> <dd>

Die Reihenfolge der nursb-Oberfläche in der Richtung der parametrischen *u* . Die Reihenfolge ist um eins größer als der Grad. Daher hat eine Oberfläche in *u* eine vier *-Reihenfolge* .

</dd> <dt>

*der Tor* 
</dt> <dd>

Die Reihenfolge der nursb-Oberfläche in der parametrischen *v* -Richtung. Die Reihenfolge ist um eins größer als der Grad. Daher hat eine Oberfläche in *v* die *v* -Reihenfolge 4.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Oberfläche. Der *Typparameter* kann einer der gültigen zweidimensionalen auswerterypen sein (z \_ . b. gl map2 \_ Vertex \_ 3 oder GL \_ map2 \_ Color \_ 4).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **glunurbssurface** innerhalb einer nurb-Oberflächen Definition, um die Form einer nurb-Oberfläche (vor jeder Kürzung) zu beschreiben. Verwenden Sie die Funktion " [**glubeginsurface**](glubeginsurface.md) ", um den Anfang einer nurist-Oberflächen Definition zu markieren. Verwenden Sie die Funktion " [**gluendsurface**](gluendsurface.md) ", um das Ende einer nurist-Oberflächen Definition zu markieren. Der Befehl " **glunurbssurface** " wird nur innerhalb einer nurb-Oberflächen Definition aufgerufen.

Sie ordnen positionelle, Textur-und Farbkoordinaten einer Oberfläche zu, indem Sie diese als separate **glunurbssurface** zwischen einem **glubeginsurface**- / **gluendsurface** -paar darstellen. Innerhalb eines einzelnen " **glubeginsurface** / **gluendsurface** "-Paars können Sie nur einen Aufrufen von " **glunurbssurface** " für Farbe, Position und Textur Daten erstellen. Machen Sie genau einen Aufrufs, um die Position der Oberfläche zu beschreiben (ein *Typ* von GL \_ map2 \_ Vertex \_ 3 oder GL \_ map2 \_ Scheitelpunkt \_ 4).

Sie können eine nurb-Oberfläche mit den Funktionen " [**glunurbscurve**](glunurbscurve.md) " und " [**glupwlcurve**](glupwlcurve.md) " zwischen Aufrufen von " [**glubegintrim**](glubegintrim.md) " und " [**gluendtrim**](gluendtrim.md)" kürzen.

Ein **glunurbssurface** mit *sknot \_ count* -Knoten in der *u* -Richtung und *tknot- \_ Zähler* in der *v* -Richtung mit Orders *sorder* und *torder* müssen (*sknicht \_ count*  - *sorder*) multipied by-Steuerungs Punkte (*tknot \_ count*  - *torder*) enthalten.

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

[**glubegintrim**](glubegintrim.md)
</dt> <dt>

[**gluendsurface**](gluendsurface.md)
</dt> <dt>

[**gluendtrim**](gluendtrim.md)
</dt> <dt>

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**glunurbscurve**](glunurbscurve.md)
</dt> <dt>

[**glupwlcurve**](glupwlcurve.md)
</dt> </dl>

 

 





