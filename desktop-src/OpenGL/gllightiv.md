---
title: gllightiv-Funktion (GL. h)
description: Die gllightiv-Funktion gibt Werte für helle Quellparameter zurück.
ms.assetid: 927f6a7e-be42-46ab-9c23-6ce87f96bd8a
keywords:
- gllightivenfunktion OpenGL
topic_type:
- apiref
api_name:
- glLightiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c70e991cf96ed5d3565e1b6c9522693786cca80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337708"
---
# <a name="gllightiv-function"></a>gllightiv-Funktion

Die **gllightiv** -Funktion gibt Werte für helle Quellparameter zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLightiv(
         GLenum light,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*light* 
</dt> <dd>

Der Bezeichner eines Lichts. Die Anzahl der möglichen Lichter hängt von der Implementierung ab, aber es werden mindestens acht Leuchten unterstützt. Sie werden durch symbolische Namen der Form GL \_ Light *i* identifiziert, bei  der es sich um einen Wert handelt: 0 bis GL \_ Max \_ Lights-1.

</dd> <dt>

*pName* 
</dt> <dd>

Ein Light Source-Parameter für *Light*. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL- \_ AMBIENT**</dt> </dl>                                                                                                                                                                                                | Der Parameter *para* meters enthält vier ganzzahlige Werte, mit denen die Umgebungs-RGBA-Intensität des Lichts angegeben wird. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0. Gleit Komma Werte werden direkt zugeordnet. Keine ganzzahligen oder Gleit Komma Werte werden geklammert. Die standardmäßige Ambient-Lichtintensität ist (0,0, 0,0, 0,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL- \_ diffuses**</dt> </dl>                                                                                                                                                                                                | Der Parameter *para* meters enthält vier ganzzahlige Werte, mit denen die diffuse RGBA-Intensität des Lichts angegeben wird. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0. Gleit Komma Werte werden direkt zugeordnet. Keine ganzzahligen oder Gleit Komma Werte werden geklammert. Die standardmäßige diffuse Intensität beträgt (0,0, 0,0, 0,0, 1,0) für alle Glühlampen, die keine helle NULL sind. Die standardmäßige diffuse Intensität von Light Zero ist (1,0, 1,0, 1,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ Glanz**</dt> </dl>                                                                                                                                                                                             | Der Parameter *para* meters enthält vier ganzzahlige Werte, mit denen die Glanz Intensität des Lichts angegeben wird. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist 1,0. Gleit Komma Werte werden direkt zugeordnet. Keine ganzzahligen oder Gleit Komma Werte werden geklammert. Die standardmäßige Glanz Intensität beträgt (0,0, 0,0, 0,0, 1,0) für alle Glühlampen, die keine helle NULL sind. Die standardmäßige Glanz Intensität von Light Zero ist (1,0, 1,0, 1,0, 1,0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**GL- \_ Position**</dt> </dl>                                                                                                                                                                                             | Der Parameter *para* meters enthält vier ganzzahlige Werte, die die Position des Lichts in homogenen Objekt Koordinaten angeben. Ganzzahlige Werte und Gleit Komma Werte werden direkt zugeordnet. Keine ganzzahligen oder Gleit Komma Werte werden geklammert. <br/> Die Position wird von der Modelview-Matrix transformiert, wenn [**gllightiv**](gllightfv.md) aufgerufen wird (genau so, als ob es sich um einen Punkt handelt) und in den Augen Koordinaten gespeichert wird. Wenn die *w* -Komponente der Position 0,0 ist, wird das Licht als direktionale Quelle behandelt. Diffuses und Glanzlichter Berechnungen übernehmen die Richtung des Lichts, aber nicht die tatsächliche Position, berücksichtigen, und die Dämpfung ist deaktiviert. Andernfalls basieren diffuse und Glanzlichter Berechnungen auf der tatsächlichen Position des Lichts in den Augen Koordinaten, und die Dämpfung ist aktiviert. Die Standardposition ist (0, 0, 1, 0); Daher ist die standardmäßige Light-Quelle direktional, parallel zu und in der Richtung der-*z* -Achse.<br/> |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**GL- \_ Spot- \_ Richtung**</dt> </dl>                                                                                                                                                                          | Der Parameter *para* meters enthält drei ganzzahlige Werte, die die Richtung des Lichts in homogenen Objekt Koordinaten angeben. Ganzzahlige Werte und Gleit Komma Werte werden direkt zugeordnet. Keine ganzzahligen oder Gleit Komma Werte werden geklammert. <br/> Die Spot-Richtung wird durch die Umkehrung der Modelview-Matrix transformiert, wenn **gllightiv** aufgerufen wird (genau so, als ob es sich um eine normale handelt) und in den Augen Koordinaten gespeichert wird. Dies ist nur dann von Bedeutung, wenn die GL-Spot-Umstellung \_ \_ nicht 180 ist, was standardmäßig der Fall ist. Die Standardrichtung ist (0,0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL- \_ Spot- \_ Exponent**</dt> </dl>                                                                                                                                                                             | Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der die Intensität der Lichtverteilung angibt. Ganzzahlige und Gleit Komma Werte werden direkt zugeordnet. Nur Werte im Bereich von \[ 0, 128 \] werden akzeptiert. <br/> Die effektive Lichtintensität wird durch den Kosinus des Winkels zwischen der Richtung des Lichts und der Richtung vom Licht zum Vertex, der beleuchtet wird, und bis zur Potenz des Spot Exponenten verringert. Daher führen höhere Spot-expenten zu einer gezielteren Lichtquelle, unabhängig vom Punkt Umstellungs Winkel. Der standardmäßige Spot-Exponent ist 0 (null) und ergibt eine einheitliche Lichtverteilung.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL. \_ Spot- \_ cuumff**</dt> </dl>                                                                                                                                                                                   | Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der den maximalen breitenwinkel einer Lichtquelle angibt. Ganzzahlige und Gleit Komma Werte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 90 \] und der spezielle Wert 180 werden akzeptiert. <br/> Wenn der Winkel zwischen der Richtung des Lichts und der Richtung vom Licht zum Scheitelpunkt größer als der Winkel Umstellungs Winkel ist, wird das Licht vollständig maskiert. Andernfalls wird die Intensität durch den Spot Exponent und die Dämpfungsfaktoren gesteuert. Der Standardwert für die Spot-Umstellungs Funktion ist 180, was eine einheitliche Lichtverteilung zur Folge hat.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**GL- \_ Konstante \_ Dämpfung, GL- \_ lineare \_ Dämpfung, GL- \_ quadratische \_ Dämpfung**</dt> </dl> | Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der einen der drei Licht Dämpfungsfaktoren angibt. Ganzzahlige und Gleit Komma Werte werden direkt zugeordnet. Nur nicht negative Werte werden akzeptiert. <br/> Wenn das Licht positionell und nicht direktional ist, wird seine Intensität durch die gegenseitige Summe der Summe von verringert: der Konstante Faktor, der lineare Faktor multipliziert mit dem Abstand zwischen dem Licht und dem Vertex, der beleuchtet wird, und der quadratische Faktor multipliziert mit dem Quadrat desselben Abstands. Die standardmäßigen Dämpfungsfaktoren sind (1, 0, 0), was zu einer nicht Dämpfung führt.<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt den Wert an, auf den der Parameter " *PName* " von Light Source *Light* festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Light* oder *PName* war kein akzeptierter Wert.<br/>                                                                                                                                                                  |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Ein Spot Exponent-Wert wurde außerhalb des Bereichs \[ 0, 128 \] oder der Spot-cuum angegeben, der außerhalb des Bereichs \[ 0, 90 \] (mit Ausnahme des sonderwerts 180) angegeben wurde, oder es wurde ein negativer Dämpfungsfaktor angegeben.<br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                                                     |



## <a name="remarks"></a>Bemerkungen

Die **gllightiv** -Funktion legt den Wert oder die Werte einzelner Lichtquellen Parameter fest. Der *Light* -Parameter benennt das Licht und ist ein symbolischer Name der Form GL \_ Light *i*, wobei 0 = *i* < GL \_ Max \_ Lights ist.

Der *PName* -Parameter gibt einen der hellen Quellparameter an, und zwar erneut durch einen symbolischen Namen. Der *params* -Parameter ist entweder ein einzelner Wert oder ein Zeiger auf ein Array, das die neuen Werte enthält.

Die Beleuchtungs Berechnung wird mithilfe von " [**glEnable**](glenable.md) " und " [**glEnable**](gldisable.md) " mit dem Argument "GL Beleuchtung" aktiviert \_ Wenn Beleuchtung aktiviert ist, tragen helle Quellen, die aktiviert sind, zur Beleuchtungs Berechnung bei. Light Source *i* wird mithilfe von **glEnable** und **gldeaktiviert** mit dem Argument GL \_ Light *i* aktiviert und deaktiviert.

Es ist immer der Fall, dass GL \_ Light *i* = GL \_ LIGHT0 + *i*.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **gllightiv** -Funktion ab:

[**glgetlight**](glgetlight.md)

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

[**glcolormaterial**](glcolormaterial.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**gllightmodel**](gllightmodel-functions.md)
</dt> <dt>

[**glmaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





