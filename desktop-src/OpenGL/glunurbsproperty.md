---
title: glunurbsproperty-Funktion (glu. h)
description: Die Funktion "glunurbsproperty" legt eine nicht einheitliche Rational B-Spline (NURBS)-Eigenschaft fest.
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
keywords:
- glunurbsproperty-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55eb8ed1914f500052c8565f6cc73e56f83bea1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475063"
---
# <a name="glunurbsproperty-function"></a>glunurbsproperty-Funktion

Die Funktion " **glunurbsproperty** " legt eine nicht einheitliche Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md))-Eigenschaft fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> <dt>

*property* 
</dt> <dd>

Die festzulegende Eigenschaft. Folgende Werte sind gültig:



| Wert                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_SAMPLING_TOLERANCE"></span><span id="glu_sampling_tolerance"></span><dl> <dt>**Glu- \_ Stichproben \_ Toleranz**</dt> </dl>       | Gibt die maximale Länge in Pixel an, die verwendet werden soll, wenn die Samplingmethode auf die Länge von Glu Path festgelegt ist \_ \_ . Der Standardwert ist 50,0 Pixel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GLU_DISPLAY_MODE"></span><span id="glu_display_mode"></span><dl> <dt>**Glu- \_ Anzeige \_ Modus**</dt> </dl>                         | Der *value* -Parameter definiert, wie eine nursb-Oberfläche gerendert werden soll. Sie können den *Wert* auf den Wert "glu \_ Fill", "glu \_ Umriss Polygon" oder " \_ glu \_ \_ Gliederung" festlegen <br/> Glu \_ ausfüllen. Die-Oberfläche wird als ein Satz von Polygonen gerendert. Dies ist der Standardwert. <br/> Glu Gliederung \_ \_ Polygon. Die nursb-Bibliothek zeichnet nur die Umrissen der durch Mosaik erstellten Polygone. <br/> Glu Gliederungs \_ \_ Patch. Nur die vom benutzerdefinierten Gliederungen der Patches und Trim-Kurven werden gezeichnet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CULLING"></span><span id="glu_culling"></span><dl> <dt>**Glu- \_ cullinger**</dt> </dl>                                         | Der *value* -Parameter ist ein boolescher Wert. Wenn value auf GL true festgelegt ist \_ , werden nursb-Kurven, deren Kontrollpunkte außerhalb des aktuellen Viewports liegen, vor dem Mosaik Prozess verworfen. Der Standardwert ist "GL \_ false" (da eine nursb-Kurve nicht vollständig innerhalb der Kontur der zugehörigen Steuerungs Punkte liegen kann).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GLU_AUTO_LOAD_MATRIX"></span><span id="glu_auto_load_matrix"></span><dl> <dt>**Glu- \_ Matrix zum automatischen \_ Laden \_**</dt> </dl>            | Der *value* -Parameter ist ein boolescher Wert. Wenn der nursb-Code auf "GL true" festgelegt \_ ist, lädt er die Projektions Matrix, die Modelview-Matrix und den Viewport vom OpenGL-Server in Compute-samplingmatrizen für jede gerenderte nursb-Kurve herunter. Sampling-und kulationsmatrizen sind erforderlich, um das Mosaik einer nursb-Oberfläche in Liniensegmente oder Polygone zu ermitteln und eine nursb-Oberfläche zu durchsuchen, wenn Sie außerhalb des Viewports liegt. <br/> Wenn dieser Modus auf "GL false" festgelegt ist \_ , müssen Sie eine Projektions Matrix, eine Modelview-Matrix und einen Viewport bereitstellen, damit der nurer-Renderer zum Erstellen von Sampling-und cullinger-Matrizen verwendet Dies können Sie mit der Funktion " [**gluloadsamplingmatrices**](gluloadsamplingmatrices.md) " erreichen.<br/> Der Standardwert für diesen Modus ist "GL \_ true". Wenn Sie diesen Modus von "GL \_ true" in "GL false" ändern, wirkt sich dies \_ erst dann auf [](gluloadsamplingmatrices.md)die Stichprobenentnahme und die immatrizen aus <br/> Die folgenden Eigenschafts Parameter werden in der Version 1,1 oder höher von Glu unterstützt und sind für die Version von Glu, Version 1,0, nicht gültig \_ \_ \_ \_ \_ \_ \_ \_ .<br/> Die folgenden Wert Parameter werden in der Version 1,1 oder höher von Glu unterstützt und sind für die Version von Glu, Version 1,0, nicht gültig: glu \_ path \_ length, Glu \_ Parametric \_ Error und glu \_ Domain \_ Distance.<br/> |
| <span id="GLU_PARAMETRIC_TOLERANCE"></span><span id="glu_parametric_tolerance"></span><dl> <dt>**Glu- \_ parametrimetrische \_ Toleranz**</dt> </dl> | Gibt den maximalen Abstand in Pixel an, der verwendet werden soll, wenn die Samplingmethode auf einen "glu \_ Parametric Error" festgelegt ist \_ Der Standardwert ist 0,5.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_SAMPLING_METHOD"></span><span id="glu_sampling_method"></span><dl> <dt>**Glu- \_ Stichproben \_ Methode**</dt> </dl>                | Gibt an, wie eine nursb-Oberfläche verwendet werden soll. Die glu- \_ Samplingmethode \_ kann einen der folgenden drei Werte aufweisen. <br/> Glu \_ - \_ Pfadlänge. Der Standardwert. Gibt an, dass Oberflächen, die mit der maximalen Länge der Kanten der Mosaik-Polygone (in Pixel) gerendert werden, nicht größer sind als der von der glu- \_ Samplings-Toleranz angegebene Wert \_ . <br/> Glu- \_ parametrischer \_ Fehler. Gibt an, dass beim Rendern der-Oberfläche der Wert von Glu \_ -parametrischer \_ Toleranz den maximalen Abstand zwischen den Mosaik Polygonen und den ungefähren Oberflächen in Pixel angibt. <br/> \_Domänen \_ Entfernung von Glu. Gibt in parametrischen Koordinaten an, wie viele Stichprobenpunkte pro Einheitslänge in den Dimensionen *u* und *v* übernommen werden sollen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GLU_U_STEP"></span><span id="glu_u_step"></span><dl> <dt>**Glu \_ U- \_ Schritt**</dt> </dl>                                           | Gibt die Anzahl von Stichprobenpunkten pro Einheitslänge an, die in parametrischen Koordinaten entlang der *u* -Dimension entnommen werden. Der Wert für den Schritt "glu U" wird verwendet, wenn die "glu"- \_ \_ \_ Samplingmethode \_ auf die \_ Domänen \_ Entfernung Der Standardwert ist 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_V_STEP"></span><span id="glu_v_step"></span><dl> <dt>**Glu \_ V- \_ Schritt**</dt> </dl>                                           | Gibt die Anzahl von Stichprobenpunkten pro Einheitslänge an, die in parametrischen Koordinaten entlang der *v* -Dimension entnommen werden. Der Wert für den Schritt "glu V" wird verwendet, wenn die "glu"- \_ \_ \_ Samplingmethode \_ auf die \_ Domänen \_ Entfernung Der Standardwert ist 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*value* 
</dt> <dd>

Der Wert, auf den die festgelegte Eigenschaft festgelegt werden soll. Der *value* -Parameter kann ein numerischer Wert oder einer der folgenden drei Werte sein: glu \_ path \_ length, Glu \_ Parametric \_ Error oder glu \_ Domain \_ Distance.



| Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_PATH_LENGTH"></span><span id="glu_path_length"></span><dl> <dt>**Glu \_ - \_ Pfadlänge**</dt> </dl>                | Der Standardwert. Gibt an, dass Oberflächen, die mit der maximalen Länge der Kanten der Mosaik-Polygone (in Pixel) gerendert werden, nicht größer sind als der von der glu- \_ Samplings-Toleranz angegebene Wert \_ .<br/> |
| <span id="GLU_PARAMETRIC_ERROR"></span><span id="glu_parametric_error"></span><dl> <dt>**Glu- \_ parametrischer \_ Fehler**</dt> </dl> | Gibt an, dass beim Rendern der-Oberfläche der Wert von Glu \_ -parametrischer \_ Toleranz den maximalen Abstand zwischen den Mosaik Polygonen und den ungefähren Oberflächen in Pixel angibt.<br/>       |
| <span id="GLU_DOMAIN_DISTANCE"></span><span id="glu_domain_distance"></span><dl> <dt>**\_Domänen \_ Entfernung von Glu**</dt> </dl>    | Gibt in parametrischen Koordinaten an, wie viele Stichprobenpunkte pro Einheitslänge in den Dimensionen *u* und *v* übernommen werden sollen.<br/>                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie " **glunurbsproperty** ", um die in einem nurb-Objekt gespeicherten Eigenschaften zu steuern. Diese Eigenschaften beeinflussen die Art und Weise, wie eine nurbkurve gerendert wird.





 

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

[**glugetnurbsproperty**](glugetnurbsproperty.md)
</dt> <dt>

[**glugetstring**](glugetstring.md)
</dt> <dt>

[**gluloadsamplingmatrices**](gluloadsamplingmatrices.md)
</dt> <dt>

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





