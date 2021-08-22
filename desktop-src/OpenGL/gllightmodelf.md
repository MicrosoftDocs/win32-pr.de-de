---
title: glLightModelf-Funktion (Gl.h)
description: Die glLightModelf-Funktion legt Parameter für das Beleuchtungsmodell fest.
ms.assetid: 7002c157-514e-4102-93f7-21a0df97a5c2
keywords:
- glLightModelf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLightModelf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1b413f4cd3daa1eeeaeaf1857018cae21edf5b4ab36bea7474bfd6bcd7e64ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493260"
---
# <a name="gllightmodelf-function"></a>glLightModelf-Funktion

Die **glLightModelf-Funktion** legt Parameter für das Beleuchtungsmodell fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLightModelf(
   GLenum  pname,
   GLfloat *param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pname* 
</dt> <dd>

Ein einwertiger Beleuchtungsmodellparameter. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**GL \_ LIGHT \_ MODEL \_ LOCAL \_ VIEWER**</dt> </dl> | Der *Parameter param* ist ein einzelner Gleitkommawert, der angibt, wie Spiegelungswinkel berechnet werden. Wenn *param* 0 (oder 0,0) ist, nehmen Glanzreflektionswinkel die Ansichtsrichtung so an, dass sie parallel zur und in Richtung der *z-Achse* sind, unabhängig von der Position des Scheitelpunkts in Augenkoordinaten. Andernfalls werden Spiegelungsreflektionen vom Ursprung des Augenkoordinatensystems berechnet. Die Standardeinstellung ist 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**GL \_ LIGHT \_ MODEL \_ TWO \_ SIDE**</dt> </dl>             | Der *Parameter param* ist ein einzelner Gleitkommawert, der angibt, ob ein- oder zweiseitige Beleuchtungsberechnungen für Polygone durchgeführt werden. Sie hat keine Auswirkungen auf die Beleuchtungsberechnungen für Punkte, Linien oder Bitmaps. Wenn *param* 0 (oder 0,0) ist, wird eine einseitige Beleuchtung angegeben, und in der Beleuchtungsgleichung werden nur die Parameter des Vordermaterials verwendet. Andernfalls wird eine zweiseitige Beleuchtung angegeben. <br/> In diesem Fall werden Scheitelpunkte von rückwärts gerichteten Polygonen mithilfe der Parameter des Hintergrundmaterials angelichtet, und ihre Normalwerte werden umgekehrt, bevor die Beleuchtungsgleichung ausgewertet wird. Scheitelpunkte von Polygonen mit Frontrichtung werden immer mithilfe der Parameter des Vordermaterials angelichtet, ohne dass sich ihre Normalitäten ändern. Die Standardeinstellung ist 0.<br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf den *der Parameter* festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *pname* war kein akzeptierter Wert.<br/>                                                                                         |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glLightModelf-Funktion** legt den Parameter des Beleuchtungsmodells fest. Der *pname-Parameter* benennt einen Parameter, und *param* gibt den neuen wert.den Wert oder die Werte einzelner Light Source-Parameter.

Im RGBA-Modus ist die helle Farbe eines Scheitelpunkts die Summe der Materialemissionsintensivität, das Produkt der materialen Umgebungsreflektion und des Beleuchtungsmodells mit vollständiger Szenen-Umgebungsdichte sowie der Beitrag jeder aktivierten Lichtquelle. Jede Lichtquelle trägt zur Summe von drei Begriffen bei: ambient, diffuse und specular.

-   Der Beitrag der Umgebungslichtquelle ist das Produkt der materialen Umgebungsreflektion und der Umgebungsdichte des Lichts.
-   Der Diffuse Light Source-Beitrag ist das Produkt der materialen diffusen Reflexion, der diffusen Intensität des Lichts und des Punktprodukts der Normalität des Scheitelpunkts mit dem normalisierten Vektor vom Scheitelpunkt zur Lichtquelle.
-   Der Glanzlichtquellen-Beitrag ist das Produkt der materialen Spiegelungsreflektion, der Glanzstärke des Lichts und des Punktprodukts der normalisierten Vertex-zu-Auge- und Vertex-zu-Licht-Vektoren, die zur Potenz der Durchlässigkeit des Materials ausgelöst werden.

Alle drei Light Source-Beiträge werden gleichmäßig auf der Grundlage der Entfernung vom Scheitelpunkt zur Lichtquelle und der Lichtquellenrichtung, der Verteilung des Exponenten und des Ausschneidewinkels abgeschwächt. Alle Punktprodukte werden durch 0 (null) ersetzt, wenn sie einen negativen Wert ergibt.

Die Alphakomponente der resultierenden lichtierten Farbe wird auf den Alphawert der materialen diffusen Reflektion festgelegt.

Im Farbindexmodus reicht der Wert des belichteten Indexes eines Scheitelpunkts von der Umgebung bis zu den Glanzwerten, die mit GL COLOR INDEXES an [**glMaterial**](glmaterial-functions.md) übergeben \_ \_ werden. Diffuse und speculare Koeffizienten, berechnet mit einer Gewichtung (.30, .59, .11) der Farben des Lichts, der Helligkeit des Materials und den gleichen Reflexions- und Dämpfungsgleichungen wie im RGBA-Fall, bestimmen, wie weit oberhalb der Umgebung der resultierende Index liegt.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glLightModelf-Funktion** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ LIGHT MODEL LOCAL \_ \_ \_ VIEWER

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ LIGHT MODEL TWO \_ \_ \_ SIDE

[**glIsEnabled**](glisenabled.md) mit argument GL \_ LIGHTING

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





