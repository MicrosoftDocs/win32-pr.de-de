---
title: glLightModelf-Funktion (Gl.h)
description: Die glLightModelf-Funktion legt Beleuchtungsmodellparameter fest.
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

Die **glLightModelf-Funktion** legt Beleuchtungsmodellparameter fest.

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

Ein einwertige Beleuchtungsmodellparameter. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**GL \_ LIGHT \_ MODEL \_ LOCAL \_ VIEWER**</dt> </dl> | Der *Parameter param* ist ein einzelner Gleitkommawert, der angibt, wie spiegelförmige Reflektionswinkel berechnet werden. Wenn *param* 0 (oder 0,0) ist, nehmen spiegelförmige Reflektionswinkel die Ansichtsrichtung an, die parallel zur und in Richtung der -*z-Achse* ist, unabhängig von der Position des Scheitelpunkts in den Augenkoordinaten. Andernfalls werden spiegelförmige Reflektionen vom Ursprung des Augenkoordinatensystems berechnet. Die Standardeinstellung ist 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**GL \_ LIGHT \_ MODEL \_ TWO \_ SIDE**</dt> </dl>             | Der *Parameter param* ist ein einzelner Gleitkommawert, der angibt, ob einseitige oder zweiseitige Beleuchtungsberechnungen für Polygone durchgeführt werden. Sie hat keine Auswirkungen auf die Beleuchtungsberechnungen für Punkte, Linien oder Bitmaps. Wenn *param* 0 (oder 0,0) ist, wird eine einseitige Beleuchtung angegeben, und nur die Parameter für das Vordermaterial werden in der Beleuchtungsgleichung verwendet. Andernfalls wird die zweiseitige Beleuchtung angegeben. <br/> In diesem Fall werden Scheiteltices von nach außen gerichteten Polygonen mithilfe der Parameter des Hintergrundmaterials hell gemacht, und ihre Normalwerte werden umgekehrt, bevor die Beleuchtungsgleichung ausgewertet wird. Scheitelungen von polygonen nach vorne gerichteten Polygonen werden immer mithilfe der Parameter des Vordermaterials leuchtet, ohne dass sich ihre Normalwerte ändern. Die Standardeinstellung ist 0.<br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf *den param* festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *pname* war kein akzeptierter Wert.<br/>                                                                                         |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **funktion glLightModelf legt** den Beleuchtungsmodellparameter fest. Der *pname-Parameter* benennt einen Parameter, *und param* gibt den neuen Wert an. Der Wert oder die Werte einzelner Light Source-Parameter.

Im RGBA-Modus ist die helle Farbe eines Scheitelpunkts die Summe der Materialausdrucksstärke, des Produkts der materialen Umgebungsrefleance und der Umgebungsstärke des Beleuchtungsmodells mit voller Szenenstärke und dem Beitrag jeder aktivierten Lichtquelle. Jede Lichtquelle trägt zur Summe von drei Begriffen bei: Ambient, Diffuse und Specular.

-   Der Beitrag der Umgebungslichtquelle ist das Produkt der materialen Umgebungsreflektoranz und der Umgebungsstärke des Lichts.
-   Der diffuse Lichtquellenbeitrag ist das Produkt der materialen diffusen Reflektoren, der diffusen Intensität des Lichts und des Punktprodukts des Normalwerts des Scheitelpunkts mit dem normalisierten Vektor vom Scheitelpunkt zur Lichtquelle.
-   Der Glanzlichtquellenbeitrag ist das Produkt der materialspezifischen Reflektoren, der Glanzstärke des Lichts und des Punktprodukts der normalisierten Vertex-to-Eye- und Vertex-to-Light-Vektoren, die zur Stärke des Materials erhöht werden.

Alle drei Lichtquellenbeiträge werden gleichmäßig auf der Grundlage des Abstands vom Scheitelpunkt zur Lichtquelle und der Lichtquellenrichtung, des Verteilungs exponenten und des Verteilungsabschneidewinkels abgedämpft. Alle Punktprodukte werden durch 0 (null) ersetzt, wenn sie zu einem negativen Wert ausgewertet werden.

Die Alphakomponente der resultierenden hellfarbenen Farbe wird auf den Alphawert der diffusen Materialreflektoranz festgelegt.

Im Farbindexmodus reicht der Wert des hell erlichten Indexes eines Scheitelpunkts von der Umgebung bis zu den an [**glMaterial**](glmaterial-functions.md) übergebenen Specularwerten mithilfe von GL \_ COLOR \_ INDEXES. Diffuse und glanzförmige Koeffizienten, berechnet mit einer Gewichtung (.30, 0,59, 0,11) der Farben des Lichts, der Schläfrigkeit des Materials und den gleichen Reflektions- und Dämpfungsgleichungen wie im RGBA-Fall, bestimmen, wie viel über der Umgebung des resultierenden Indexes liegt.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glLightModelf-Funktion** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ LIGHT MODEL LOCAL \_ \_ \_ VIEWER

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ LIGHT MODEL TWO \_ \_ \_ SIDE

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ LIGHTING

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





