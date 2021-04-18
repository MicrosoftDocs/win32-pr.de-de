---
title: gluloadsamplingmatrices-Funktion (glu. h)
description: Die Funktion "gluloadsamplingmatrices" lädt nicht einheitliche, nicht einheitliche Rational B-Spline (NURBS)-samplingmatrizen.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- gluloadsamplingmatrices-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337311"
---
# <a name="gluloadsamplingmatrices-function"></a>gluloadsamplingmatrices-Funktion

Die Funktion " **gluloadsamplingmatrices** " lädt nicht einheitliche, nicht einheitliche Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md))-samplingmatrizen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> <dt>

*modelmatrix* 
</dt> <dd>

Eine Modelview-Matrix (wie bei einem [**glgetfloatv**](glgetfloatv.md) -Befehl).

</dd> <dt>

*projmatrix* 
</dt> <dd>

Eine Projektions Matrix (wie bei einem **glgetfloatv** -Befehl).

</dd> <dt>

*Viewport* 
</dt> <dd>

Ein Viewport (wie bei einem [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) -Befehl).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluloadsamplingmatrices** " verwendet " *modelmatrix*", " *projmatrix*" und "Viewport", um die in *nobj* gespeicherten samplingund immatrixmatrizen neu zu berechnen.  Die Stichproben Matrix bestimmt, wie gut eine nursb-Kurve oder-Oberfläche im Mosaik Prozess berücksichtigt werden muss, um die Stichproben Toleranz zu erfüllen (wie durch die Eigenschaft für die- \_ Stichproben \_ Toleranz bestimmt). Die culult-Matrix wird bei der Entscheidung verwendet, ob eine nursb-Kurve oder-Oberfläche vor dem Rendern vor dem Rendering (bei aktivierter \_ engisteringeigenschaft) gekettet werden soll.

Die Funktion " **gluloadsamplingmatrices** " ist nur erforderlich, wenn die "glu \_ \_ autoload Matrix"- \_ Eigenschaft ausgeschaltet ist (siehe [**glunurbsproperty**](glunurbsproperty.md)). Obwohl es sinnvoll sein kann, die Eigenschaften für die \_ Automatische Load-Matrix von Glu zu aktivieren \_ \_ , erfordert dies einen Roundtrip zum OpenGL-Server, um die aktuellen Werte der Modelview-Matrix, der Projektions Matrix und des Viewports abzurufen.)

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

[**glgetfloatv**](glgetfloatv.md)
</dt> <dt>

[**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glugetnurbsproperty**](glugetnurbsproperty.md)
</dt> <dt>

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





