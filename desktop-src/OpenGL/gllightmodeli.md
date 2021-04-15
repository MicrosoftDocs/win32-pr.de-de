---
title: gllightmodeli-Funktion (GL. h)
description: Die gllightmodeli-Funktion legt Beleuchtungsmodell Parameter fest.
ms.assetid: 49975166-b2b3-47f9-8305-aea2ba364546
keywords:
- gllightmodeli-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLightModeli
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ae32e91e62a5341ceb0fc3fc4b16b0e7cfbae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391541"
---
# <a name="gllightmodeli-function"></a>gllightmodeli-Funktion

Die [**gllightmodeli**](gllightf.md) -Funktion legt Beleuchtungsmodell Parameter fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLightModeli(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Ein einwertiger Beleuchtungsmodell Parameter. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**\_ \_ \_ lokaler \_ Viewer für GL-Light-Modell**</dt> </dl> | Der Parameter *param* ist ein einzelner ganzzahliger Wert, der angibt, wie Glanz Winkel der Reflektion berechnet werden. Wenn *param* den Wert 0 (oder 0,0) hat, nehmen Glanz reflektionswinkel die Ansichts Richtung an, und die Richtung der-*z* -Achse ist unabhängig von der Position des Scheitel Punkts in den Augen Koordinaten. Andernfalls werden Glanz Spiegelung vom Ursprung des Augen Koordinatensystems berechnet. Die Standardeinstellung ist 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**GL- \_ Light- \_ Modell auf \_ zwei \_ Seiten**</dt> </dl>             | Der Parameter *param* ist ein einzelner ganzzahliger Wert, der angibt, ob einseitige oder zweiseitige Beleuchtungsberechnungen für Polygone durchgeführt werden. Dies hat keine Auswirkung auf die Beleuchtungsberechnungen für Punkte, Linien oder Bitmaps. Wenn *param* 0 (oder 0,0) ist, wird eine einseitige Beleuchtung angegeben, und nur die Front-Material-Parameter werden in der Beleuchtungs Gleichung verwendet. Andernfalls wird eine zweiseitige Beleuchtung angegeben. <br/> In diesem Fall werden Vertices von rückwärts gerichteten Polygonen mit den backmaterialparametern beleuchtet und deren normale umgekehrt, bevor die Beleuchtungs Gleichung ausgewertet wird. Vertices von nach vorne gerichteten Polygonen werden immer mit den Front-Material-Parametern beleuchtet, ohne dass ihre normale geändert werden. Die Standardeinstellung ist 0.<br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf den *param* festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *PName* war kein akzeptierter Wert.<br/>                                                                                         |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **gllightmodeli** -Funktion legt den Beleuchtungsmodell Parameter fest. Der Parameter " *PName* " benennt einen *Parameter und gibt* den neuen Wert an. der Wert oder die Werte einzelner Licht Quellparameter.

Im RGBA-Modus ist die Farbe eines Scheitel Punkts die Summe der Material-Emissionsintensität, das Produkt der Material Ambient-Reflektion und das Beleuchtungsmodell der Umgebungs Intensität in voller Szene und der Anteil der einzelnen aktivierten Lichtquellen. Jede helle Quelle trägt die Summe von drei Begriffen bei: Ambient, diffuses und specarität.

-   Der Ambient-Lichtquellen Beitrag ist das Produkt der Material Ambient Reflektion und der Umgebungs Intensität des Lichts.
-   Der Anteil der diffusen Lichtquelle ist das Produkt der Material diffctance, der diffusen Intensität des Lichts und des Punkt Produkts der normalen Vertex mit dem normalisierten Vektor aus dem Scheitelpunkt und der Lichtquelle.
-   Der Glanz der Glanzlicht Quelle ist das Produkt der hellen Glanz Reflektion, die Glanz Intensität des Lichts und das Punktprodukt der normalisierten Scheitelpunkt-zu-Auge-und Vertex-zu-Licht-Vektoren, die an die Leistungsfähigkeit des Materials hervorgehoben werden.

Alle drei Lichtquellen Beiträge werden gleichmäßig auf Grundlage der Entfernung zwischen dem Scheitelpunkt und der Lichtquelle und der Lichtquelle, dem Spread-Exponent und dem Spread-Umstellungs-Winkel verringert. Alle Punkt Produkte werden durch 0 (null) ersetzt, wenn Sie einen negativen Wert ergeben.

Die Alpha Komponente der resultierenden beleuchteten Farbe wird auf den Alpha-Wert der Material diffctance festgelegt.

Im Farb Index Modus wird der Wert des beleuchteten Indexes eines Scheitel Punkts von der Ambient-zu den Glanzwerten, die mithilfe von GL-Farbindizes an [**glmaterial**](glmaterial-functions.md) übergeben werden \_ \_ . Diffuse und glanzvolle Koeffizienten, berechnet mit einer (. 30,. 59, .11) Gewichtung der hellen Farben, dem Glanz des Materials und denselben Reflektions-und Dämpfungs Gleichungen wie im RGBA-Fall, legen fest, wie viel oben in der Umgebung der resultierende Index ist.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **gllightmodeli** -Funktion ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Light \_ Model \_ local \_ Viewer

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Light \_ Model \_ Two \_ Side

[**glisenabled**](glisenabled.md) mit dem Argument GL- \_ Beleuchtung

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**gllight**](gllight-functions.md)
</dt> <dt>

[**glmaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





