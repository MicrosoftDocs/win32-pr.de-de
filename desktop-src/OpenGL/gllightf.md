---
title: gllightf-Funktion (GL. h)
description: Die gllightf-Funktion gibt Werte für helle Quellparameter zurück.
ms.assetid: d9f93fd9-6674-486f-a3fc-c10255dd37e7
keywords:
- gllightf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLightf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 099490461f5fbf6feb009e98c0228165938326d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743121"
---
# <a name="gllightf-function"></a>gllightf-Funktion

Die **gllightf** -Funktion gibt Werte für helle Quellparameter zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLightf(
   GLenum  light,
   GLenum  pname,
   GLfloat param
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

Ein einwertiger Light-Quellparameter für *Light*. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL- \_ Spot- \_ Exponent**</dt> </dl>                                                                                                                                                                             | Der Parameter *param* ist ein einzelner Gleit Komma Wert, der die Intensität des Lichts angibt. Gleit Komma Werte werden direkt zugeordnet. Nur Werte im Bereich von \[ 0, 128 \] werden akzeptiert. <br/> Die effektive Lichtintensität wird durch den Kosinus des Winkels zwischen der Richtung des Lichts und der Richtung vom Licht zum Vertex, der beleuchtet wird, und bis zur Potenz des Spot Exponenten verringert. Daher führen höhere Spot-expenten zu einer gezielteren Lichtquelle, unabhängig vom Punkt Umstellungs Winkel. Der standardmäßige Spot-Exponent ist 0 (null) und ergibt eine einheitliche Lichtverteilung.<br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL. \_ Spot- \_ cuumff**</dt> </dl>                                                                                                                                                                                   | Der Parameter *param* ist ein einzelner Gleit Komma Wert, der den maximalen breitenwinkel einer Lichtquelle angibt. Gleit Komma Werte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 90 \] und der spezielle Wert 180 werden akzeptiert. <br/> Wenn der Winkel zwischen der Richtung des Lichts und der Richtung vom Licht zum Scheitelpunkt größer als der Winkel Umstellungs Winkel ist, wird das Licht vollständig maskiert. Andernfalls wird die Intensität durch den Spot Exponent und die Dämpfungsfaktoren gesteuert. Der Standardwert für die Spot-Umstellungs Funktion ist 180, was eine einheitliche Lichtverteilung zur Folge hat.<br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**GL- \_ Konstante \_ Dämpfung, GL- \_ lineare \_ Dämpfung, GL- \_ quadratische \_ Dämpfung**</dt> </dl> | Der Parameter *param* ist ein einzelner Gleit Komma Wert, der einen der drei Licht Dämpfungsfaktoren angibt. Gleit Komma Werte werden direkt zugeordnet. Nur nicht negative Werte werden akzeptiert. <br/> Wenn das Licht positionell und nicht direktional ist, wird seine Intensität durch die gegenseitige Summe der Summe von verringert: der Konstante Faktor, der lineare Faktor multipliziert mit dem Abstand zwischen dem Licht und dem Vertex, der beleuchtet wird, und der quadratische Faktor multipliziert mit dem Quadrat desselben Abstands. Die standardmäßigen Dämpfungsfaktoren sind (1, 0, 0), was zu einer nicht Dämpfung führt.<br/>                   |



 

</dd> <dt>

*param* 
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

Die **gllightf** -Funktion legt den Wert oder die Werte einzelner Lichtquellen Parameter fest. Der *Light* -Parameter benennt das Licht und ist ein symbolischer Name der Form GL \_ Light *i*, wobei 0 = *i* < GL \_ Max \_ Lights ist.

Der *PName* -Parameter gibt einen der hellen Quellparameter an, und zwar erneut durch einen symbolischen Namen. Der Parameter *param* ist entweder ein einzelner Wert oder ein Zeiger auf ein Array, das die neuen Werte enthält.

Die Beleuchtungs Berechnung wird mithilfe von " [**glEnable**](glenable.md) " und " [**glEnable**](gldisable.md) " mit dem Argument "GL Beleuchtung" aktiviert \_ Wenn Beleuchtung aktiviert ist, tragen helle Quellen, die aktiviert sind, zur Beleuchtungs Berechnung bei. Light Source *i* wird mithilfe von **glEnable** und **gldeaktiviert** mit dem Argument GL \_ Light *i* aktiviert und deaktiviert.

Es ist immer der Fall, dass GL \_ Light *i* = GL \_ LIGHT0 + *i*.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **gllightf** -Funktion ab:

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

 

 





