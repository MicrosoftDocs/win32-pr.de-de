---
title: glLightiv-Funktion (Gl.h)
description: Die glLightiv-Funktion gibt Light Source-Parameterwerte zurück.
ms.assetid: 927f6a7e-be42-46ab-9c23-6ce87f96bd8a
keywords:
- glLightiv-Funktion OpenGL
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
ms.openlocfilehash: b1b497c6cbac510b57814303f07ee060398e255b02dd1c8f9d7cd129f386d776
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493250"
---
# <a name="gllightiv-function"></a>glLightiv-Funktion

Die **glLightiv-Funktion** gibt Light Source-Parameterwerte zurück.

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

Der Bezeichner eines Lichts. Die Anzahl möglicher Beleuchtungen hängt von der Implementierung ab, aber es werden mindestens acht Beleuchtungen unterstützt. Sie werden durch symbolische Namen der Form GL LIGHT i identifiziert, wobei i ein Wert \_ ist: 0 bis GL MAX LIGHTS -  \_ \_ 1.

</dd> <dt>

*pname* 
</dt> <dd>

Ein Light Source-Parameter für *light*. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                                                                                                                                                                                                | Der *Parameter params* enthält vier ganzzahlige Werte, die die RGBA-Umgebungsstärke des Lichts angeben. Ganzzahlwerte werden linear zugeordnet, damit der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige werte noch Gleitkommawerte werden an die Klammern klammern. Die Standardmäßige Umgebungslichtstärke ist (0,0, 0,0, 0,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                                                                                                                                                                                                | Der *Parameter params* enthält vier ganzzahlige Werte, die die diffuse RGBA-Intensität des Lichts angeben. Ganzzahlwerte werden linear zugeordnet, damit der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige werte noch Gleitkommawerte werden an die Klammern klammern. Die standardmäßige diffuse Intensität ist (0,0, 0,0, 0,0, 1,0) für alle Anderen als lichten Nullen. Die standardmäßige diffuse Intensität des lichten Nullpunkts ist (1,0, 1,0, 1,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                                                                                                                                                                                             | Der *Parameter params* enthält vier ganzzahlige Werte, die die rgba-Intensität des Lichts angeben. Ganzzahlwerte werden linear zugeordnet, damit der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert 1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige werte noch Gleitkommawerte werden an die Klammern klammern. Die Standardmäßige Specular-Intensität ist (0,0, 0,0, 0,0, 1,0) für alle Anderen als lichten Nullen. Die Standardmäßige Specular-Intensität des Lichts 0 ist (1,0, 1,0, 1,0, 1,0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**GL \_ POSITION**</dt> </dl>                                                                                                                                                                                             | Der *Parameter params* enthält vier ganzzahlige Werte, die die Position des Lichts in homogenen Objektkoordinaten angeben. Sowohl ganzzahlige als auch Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige werte noch Gleitkommawerte werden an die Klammern klammern. <br/> Die Position wird von der ModelView-Matrix transformiert, wenn [**glLightiv**](gllightfv.md) aufgerufen wird (als wäre es ein Punkt), und sie wird in Augenkoordinaten gespeichert. Wenn die *w-Komponente* der Position 0,0 ist, wird das Licht als direktionale Quelle behandelt. Bei diffusen und specularen Beleuchtungsberechnungen wird die Richtung des Lichts, aber nicht seine tatsächliche Position berücksichtigt, und die Dämpfung wird deaktiviert. Andernfalls basieren diffuse und speculare Beleuchtungsberechnungen auf der tatsächlichen Position des Lichts in Augenkoordinaten, und die Dämpfung ist aktiviert. Die Standardposition ist (0,0,1,0); Daher ist die Standardlichtquelle richtungs- und parallel zur - z-Achse.<br/> |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**GL \_ SPOT \_ DIRECTION**</dt> </dl>                                                                                                                                                                          | Der *Parameter params* enthält drei ganzzahlige Werte, die die Richtung des Lichts in homogenen Objektkoordinaten angeben. Sowohl ganzzahlige als auch Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige werte noch Gleitkommawerte werden an die Klammern klammern. <br/> Die Spot-Richtung wird durch die Umkehrung der Modellansichtsmatrix transformiert, wenn **glLightiv** aufgerufen wird (genau so, als wäre es ein Normalfall), und sie wird in Augenkoordinaten gespeichert. Dies ist nur wichtig, wenn GL \_ SPOT \_ CUTOFF nicht 180 beträgt, was standardmäßig der Standard ist. Die Standardrichtung ist (0,0,1).<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL \_ SPOT \_ EXPONENT**</dt> </dl>                                                                                                                                                                             | Der *Parameter params* ist ein einzelner ganzzahliger Wert, der die Intensitätsverteilung des Lichts angibt. Ganzzahl- und Gleitkommawerte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 128 \] werden akzeptiert. <br/> Die effektive Lichtstärke wird durch den Kosinus des Winkels zwischen der Lichtrichtung und der Richtung vom Licht zum scheitelierten Scheitelpunkt abgedämpft, der zur Potenz des Spot-Exponenten erhöht wird. Daher führen höhere Spot-Exponenten unabhängig vom Spot-Abschneidewinkel zu einer fokussierteren Lichtquelle. Der Standard-Spot-Exponent ist 0, was zu einer gleichmäßigen Lichtverteilung führt.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                                                                                                                                                                                   | Der *Parameter params* ist ein einzelner ganzzahliger Wert, der den maximalen Strichwinkel einer Lichtquelle angibt. Ganzzahl- und Gleitkommawerte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 90 und dem \] Sonderwert 180 werden akzeptiert. <br/> Wenn der Winkel zwischen der Lichtrichtung und der Richtung vom Licht zum scheitelierten Scheitelpunkt größer ist als der Abschneidewinkel, wird das Licht vollständig maskiert. Andernfalls wird die Intensität durch den Spot-Exponenten und die Dämpfungsfaktoren gesteuert. Der Standard-Spot-Cutoff ist 180, was zu einer gleichmäßigen Lichtverteilung führt.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**GL \_ CONSTANT \_ ATTENUATION, GL \_ LINEAR \_ ATTENUATION, GL \_ QUADRATIC \_ ATTENUATION**</dt> </dl> | Der *Parameter params* ist ein einzelner ganzzahliger Wert, der einen der drei Lichtdämpfungsfaktoren angibt. Ganzzahl- und Gleitkommawerte werden direkt zugeordnet. Es werden nur nicht negative Werte akzeptiert. <br/> Wenn das Licht positional und nicht direktional ist, wird seine Intensität durch den Kehreffekt der Summe von abgedämpft: der konstante Faktor, der lineare Faktor multipliziert mit dem Abstand zwischen dem Licht und dem scheitelierten Scheitelpunkt und der quadratische Faktor multipliziert mit dem Quadrat desselben Abstands. Die Standarddämpfungsfaktoren sind (1,0,0), was zu keiner Dämpfung führt.<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt den Wert an, auf  den *der Parameter pname* der Lichtquelle festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *light* oder *pname* war kein akzeptierter Wert.<br/>                                                                                                                                                                  |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Ein Spot-Exponentwert wurde außerhalb des Bereichs von 0, 128 oder spot cutoff außerhalb des Bereichs 0, 90 (mit Ausnahme des Sonderwerts \[ \] \[ 180) angegeben, oder es wurde ein negativer Dämpfungsfaktor \] angegeben.<br/> |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/>                                                                                     |



## <a name="remarks"></a>Hinweise

Die **glLightiv-Funktion** legt den Wert oder die Werte einzelner Lichtquellenparameter fest. Der *Lichtparameter* benennt das Licht und ist ein symbolischer Name der Form GL \_ LIGHT *i,* wobei 0 = *i <* GL MAX \_ LIGHTS \_ ist.

Der *pname-Parameter* gibt einen der Light Source-Parameter an, wiederum durch symbolischen Namen. Der *Parameter params* ist entweder ein einzelner Wert oder ein Zeiger auf ein Array, das die neuen Werte enthält.

Die Beleuchtungsberechnung wird mit [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL LIGHTING aktiviert und \_ deaktiviert. Wenn die Beleuchtung aktiviert ist, tragen die aktivierten Lichtquellen zur Beleuchtungsberechnung bei. Die Lichtquelle *i ist* aktiviert und deaktiviert, **indem glEnable** und **glDisable** mit dem Argument GL \_ LIGHT i verwendet *werden.*

Es ist immer der Fall, dass GL \_ LIGHT *i* = GL \_ LIGHT0 + *i* ist.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glLightiv-Funktion** ab:

[**glGetLight**](glgetlight.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





