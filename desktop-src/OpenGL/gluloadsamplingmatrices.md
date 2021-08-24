---
title: gluLoadSamplingMatrices-Funktion (Glu.h)
description: Die gluLoadSamplingMatrices-Funktion lädt NON-Uniform Rational B-Spline (NURBS)-Sampling- und Cullingmatrizen.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- gluLoadSamplingMatrices-Funktion OpenGL
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
ms.openlocfilehash: e41b2f6b25e0cecf0d13d87760a941d5ea68baa1fdd85495c8a316e862c77aec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777530"
---
# <a name="gluloadsamplingmatrices-function"></a>gluLoadSamplingMatrices-Funktion

Die **gluLoadSamplingMatrices-Funktion** lädt non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) Sampling- und Cullingmatrizen.

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

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Eine ModelView-Matrix (wie bei einem [**glGetFloatv-Aufruf).**](glgetfloatv.md)

</dd> <dt>

*projMatrix* 
</dt> <dd>

Eine Projektionsmatrix (aus einem **glGetFloatv-Aufruf).**

</dd> <dt>

*Ansichtsfenster* 
</dt> <dd>

Ein Viewport (wie bei einem [**glGetIntegerv-Aufruf).**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluLoadSamplingMatrices-Funktion** verwendet *modelMatrix,* *projMatrix* und *viewport,* um die in *nobj* gespeicherten Sampling- und Cullingmatrizen neu zu berechnen. Die Samplingmatrix bestimmt, wie fein eine NURBS-Kurve oder -Oberfläche mosaikiert werden muss, um die Samplingtoleranz zu erfüllen (wie durch die GLU \_ SAMPLING \_ TOLERANCE-Eigenschaft festgelegt). Die Cullingmatrix wird verwendet, um zu entscheiden, ob eine NURBS-Kurve oder -Oberfläche vor dem Rendering gecullt werden soll (wenn die \_ GLU-CULLING-Eigenschaft aktiviert ist).

Die **gluLoadSamplingMatrices-Funktion** ist nur erforderlich, wenn die GLU AUTO LOAD MATRIX-Eigenschaft deaktiviert ist \_ \_ \_ (siehe [**gluNurbsProperty**](glunurbsproperty.md)). Obwohl es praktisch sein kann, die GLU AUTO LOAD MATRIX-Eigenschaft aktiviert zu lassen, erfordert dies einen Roundtrip zum OpenGL-Server, um die aktuellen Werte der \_ \_ \_ Modellansichtsmatrix, Projektionsmatrix und Viewports zu erhalten.)

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

[**glGetFloatv**](glgetfloatv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





