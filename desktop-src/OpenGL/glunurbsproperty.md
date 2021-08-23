---
title: gluNurbsProperty-Funktion (Glu.h)
description: Die gluNurbsProperty-Funktion legt eine NURBS-Eigenschaft (Non-Uniform Rational B-Spline) fest.
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
keywords:
- gluNurbsProperty-Funktion OpenGL
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
ms.openlocfilehash: 1cbc52bd1405d15967db4aa1ef4941d0c4e166420d25d6d1fcb1ba4db0a6e744
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489030"
---
# <a name="glunurbsproperty-function"></a>gluNurbsProperty-Funktion

Die **gluNurbsProperty-Funktion** legt eine nicht einheitliche rationale B-Spline -Eigenschaft [(NURBS)](using-nurbs-curves-and-surfaces.md)fest.

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

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Die festzulegende Eigenschaft. Folgende Werte sind gültig:



| Wert                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_SAMPLING_TOLERANCE"></span><span id="glu_sampling_tolerance"></span><dl> <dt>**GLU \_ SAMPLING \_ TOLERANCE**</dt> </dl>       | Gibt die maximale Länge in Pixel an, die verwendet werden soll, wenn die Samplingmethode auf GLU PATH LENGTH festgelegt \_ \_ ist. Der Standardwert ist 50,0 Pixel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GLU_DISPLAY_MODE"></span><span id="glu_display_mode"></span><dl> <dt>**\_ \_ GLU-ANZEIGEMODUS**</dt> </dl>                         | Der *Value-Parameter* definiert, wie eine NURBS-Oberfläche gerendert werden soll. Sie können *den Wert* auf GLU \_ FILL, GLU OUTLINE POLYGON oder GLU OUTLINE PATCH \_ \_ \_ \_ festlegen. <br/> GLU \_ FILL. Die Oberfläche wird als Gruppe von Polygonen gerendert. Dies ist der Standardwert. <br/> GLU \_ OUTLINE \_ POLYGON. Die NURBS-Bibliothek zeichnet nur die Konturen der Polygone, die durch Mosaik erstellt wurden. <br/> GLU \_ OUTLINE \_ PATCH. Nur die Vom Benutzer definierten Umrisse von Patches und Kürzungskurven werden gezeichnet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CULLING"></span><span id="glu_culling"></span><dl> <dt>**GLU \_ CULLING**</dt> </dl>                                         | Der *value-Parameter* ist ein boolescher Wert. Wenn value auf GL TRUE festgelegt \_ ist, werden NURBS-Kurven, deren Kontrollpunkte außerhalb des aktuellen Viewports liegen, vor dem Mosaik verworfen. Der Standardwert ist GL \_ FALSE (da eine NURBS-Kurve nicht vollständig innerhalb der konvexen Hülle ihrer Kontrollpunkte liegen kann).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GLU_AUTO_LOAD_MATRIX"></span><span id="glu_auto_load_matrix"></span><dl> <dt>**GLU \_ AUTO \_ LOAD \_ MATRIX**</dt> </dl>            | Der *value-Parameter* ist ein boolescher Wert. Bei Festlegung auf GL \_ TRUE lädt der NURBS-Code die Projektionsmatrix, die Modellansichtsmatrix und den Viewport vom OpenGL-Server herunter, um Stichproben und Cullingmatrizen für jede gerenderte NURBS-Kurve zu berechnen. Sampling- und Cullingmatrizen sind erforderlich, um das Mosaik einer NURBS-Oberfläche in Liniensegmente oder Polygone zu bestimmen und eine NURBS-Oberfläche zu umschwenken, wenn sie außerhalb des Viewports liegt. <br/> Wenn dieser Modus auf GL FALSE festgelegt \_ ist, müssen Sie eine Projektionsmatrix, eine Modellansichtsmatrix und einen Viewport bereitstellen, damit der NURBS-Renderer stichproben- und culling-Matrizen erstellen kann. Sie können dies mit der [**gluLoadSamplingMatrices-Funktion**](gluloadsamplingmatrices.md) erreichen.<br/> Der Standardwert für diesen Modus ist GL \_ TRUE. Das Ändern dieses Modus von GL \_ TRUE in GL FALSE wirkt sich erst dann auf die \_ Sampling- und Cullingmaces aus, wenn Sie [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)aufrufen. <br/> Die folgenden Eigenschaftsparameter werden in GLU Version 1.1 oder höher unterstützt und sind für GLU-Version 1.0 nicht gültig: GLU \_ PARAMETRIC \_ TOLERANCE, GLU \_ SAMPLING \_ METHOD, GLU \_ U STEP und GLU V \_ \_ \_ STEP.<br/> Die folgenden Wertparameter werden in GLU Version 1.1 oder höher unterstützt und sind für GLU-Version 1.0 nicht gültig: GLU \_ PATH \_ LENGTH, GLU \_ PARAMETRIC \_ ERROR und GLU \_ DOMAIN \_ DISTANCE.<br/> |
| <span id="GLU_PARAMETRIC_TOLERANCE"></span><span id="glu_parametric_tolerance"></span><dl> <dt>**GLU \_ PARAMETRIC \_ TOLERANCE**</dt> </dl> | Gibt den maximalen Abstand in Pixel an, der verwendet werden soll, wenn die Samplingmethode auf GLU PARAMETRIC ERROR festgelegt \_ \_ ist. Der Standardwert ist 0,5.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_SAMPLING_METHOD"></span><span id="glu_sampling_method"></span><dl> <dt>**GLU \_ \_ SAMPLING-METHODE**</dt> </dl>                | Gibt an, wie eine NURBS-Oberfläche tessalisiert wird. DIE GLU \_ \_ SAMPLING-METHODE kann einen der folgenden drei Werte aufweisen. <br/> GLU \_ PATH \_ LENGTH(GLU PATH LENGTH). Der Standardwert. Gibt an, dass Oberflächen, die mit der maximalen Länge der Kanten der Mosaikpolygone in Pixel gerendert werden, nicht größer als der von GLU SAMPLING TOLERANCE angegebene Wert \_ \_ sind. <br/> GLU \_ PARAMETRIC \_ ERROR. Gibt an, dass beim Rendern der Oberfläche der Wert von GLU \_ PARAMETRIC \_ TOLERANCE den maximalen Abstand zwischen den Mosaikpolygonen und den oberflächen, die sie annähern, in Pixel angibt. <br/> GLU \_ DOMAIN \_ DISTANCE. Gibt in parametrischen Koordinaten an, wie viele Stichprobenpunkte pro Einheitslänge in den *Dimensionen u* und *v* erfasst werden sollen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GLU_U_STEP"></span><span id="glu_u_step"></span><dl> <dt>**GLU \_ U \_ STEP**</dt> </dl>                                           | Gibt die Anzahl der Stichprobenpunkte pro Einheitslänge an, die entlang der *u-Dimension* in parametrischen Koordinaten genommen werden. Der Wert von GLU \_ U \_ STEP wird verwendet, wenn GLU SAMPLING \_ METHOD auf GLU DOMAIN DISTANCE festgelegt \_ \_ \_ ist. Der Standardwert ist 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_V_STEP"></span><span id="glu_v_step"></span><dl> <dt>**GLU \_ \_ V-SCHRITT**</dt> </dl>                                           | Gibt die Anzahl der Stichprobenpunkte pro Einheitenlänge an, die entlang der *v-Dimension* in parametrischen Koordinaten genommen werden. Der Wert von GLU \_ V \_ STEP wird verwendet, wenn GLU SAMPLING \_ METHOD auf GLU DOMAIN DISTANCE festgelegt \_ \_ \_ ist. Der Standardwert ist 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*value* 
</dt> <dd>

Der Wert, auf den die angegebene Eigenschaft festgelegt werden soll. Der *Value-Parameter* kann ein numerischer Wert oder einer der folgenden drei Werte sein: GLU \_ PATH \_ LENGTH, GLU \_ PARAMETRIC ERROR oder GLU DOMAIN \_ \_ \_ DISTANCE.



| Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_PATH_LENGTH"></span><span id="glu_path_length"></span><dl> <dt>**GLU \_ PATH \_ LENGTH**</dt> </dl>                | Der Standardwert. Gibt an, dass Oberflächen, die mit der maximalen Länge der Kanten der Mosaikpolygone in Pixel gerendert werden, nicht größer als der von GLU SAMPLING TOLERANCE angegebene Wert \_ \_ sind.<br/> |
| <span id="GLU_PARAMETRIC_ERROR"></span><span id="glu_parametric_error"></span><dl> <dt>**GLU \_ PARAMETRIC \_ ERROR**</dt> </dl> | Gibt an, dass beim Rendern der Oberfläche der Wert von GLU \_ PARAMETRIC \_ TOLERANCE den maximalen Abstand zwischen den Mosaikpolygonen und den oberflächen, die sie annähern, in Pixel angibt.<br/>       |
| <span id="GLU_DOMAIN_DISTANCE"></span><span id="glu_domain_distance"></span><dl> <dt>**GLU \_ DOMAIN \_ DISTANCE**</dt> </dl>    | Gibt in parametrischen Koordinaten an, wie viele Stichprobenpunkte pro Einheitslänge in den *Dimensionen u* und *v* erfasst werden sollen.<br/>                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie **gluNurbsProperty,** um eigenschaften zu steuern, die in einem NURBS-Objekt gespeichert sind. Diese Eigenschaften beeinflussen die Art und Weise, wie eine NURBS-Kurve gerendert wird.





 

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

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluGetString**](glugetstring.md)
</dt> <dt>

[**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





