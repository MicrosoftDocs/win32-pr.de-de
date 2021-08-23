---
title: glLightf-Funktion (Gl.h)
description: Die glLightf-Funktion gibt Light Source-Parameterwerte zurück.
ms.assetid: d9f93fd9-6674-486f-a3fc-c10255dd37e7
keywords:
- glLightf-Funktion OpenGL
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
ms.openlocfilehash: cde2bbee996183ad39067aed3b98a64dd5abb40f87c6746d7dda305bdb0e7438
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012108"
---
# <a name="gllightf-function"></a>glLightf-Funktion

Die **glLightf-Funktion** gibt Light Source-Parameterwerte zurück.

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

Der Bezeichner eines Lichts. Die Anzahl möglicher Beleuchtungen hängt von der Implementierung ab, aber es werden mindestens acht Beleuchtungen unterstützt. Sie werden durch symbolische Namen der Form GL LIGHT i identifiziert, wobei i ein Wert \_ ist: 0 bis GL MAX LIGHTS -  \_ \_ 1.

</dd> <dt>

*pname* 
</dt> <dd>

Ein einwertigen Light Source-Parameter für *light*. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL \_ SPOT \_ EXPONENT**</dt> </dl>                                                                                                                                                                             | Der *Parameter param* ist ein einzelner Gleitkommawert, der die Intensitätsverteilung des Lichts angibt. Gleitkommawerte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 128 \] werden akzeptiert. <br/> Die effektive Lichtstärke wird durch den Kosinus des Winkels zwischen der Lichtrichtung und der Richtung vom Licht zum scheitelierten Scheitelpunkt abgedämpft, der zur Potenz des Spot-Exponenten erhöht wird. Daher führen höhere Spot-Exponenten unabhängig vom Spot-Abschneidewinkel zu einer fokussierteren Lichtquelle. Der Standard-Spot-Exponent ist 0, was zu einer gleichmäßigen Lichtverteilung führt.<br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                                                                                                                                                                                   | Der *Parameter param* ist ein einzelner Gleitkommawert, der den maximalen Strichwinkel einer Lichtquelle angibt. Gleitkommawerte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 90 und dem \] Sonderwert 180 werden akzeptiert. <br/> Wenn der Winkel zwischen der Lichtrichtung und der Richtung vom Licht zum scheitelierten Scheitelpunkt größer ist als der Abschneidewinkel, wird das Licht vollständig maskiert. Andernfalls wird die Intensität durch den Spot-Exponenten und die Dämpfungsfaktoren gesteuert. Der Standard-Spot-Cutoff ist 180, was zu einer gleichmäßigen Lichtverteilung führt.<br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**GL \_ CONSTANT \_ ATTENUATION, GL \_ LINEAR \_ ATTENUATION, GL \_ QUADRATIC \_ ATTENUATION**</dt> </dl> | Der *Parameter param* ist ein einzelner Gleitkommawert, der einen der drei Lichtdämpfungsfaktoren angibt. Gleitkommawerte werden direkt zugeordnet. Es werden nur nicht negative Werte akzeptiert. <br/> Wenn das Licht positional und nicht direktional ist, wird seine Intensität durch den Kehreffekt der Summe von abgedämpft: der konstante Faktor, der lineare Faktor multipliziert mit dem Abstand zwischen dem Licht und dem scheitelierten Scheitelpunkt und der quadratische Faktor multipliziert mit dem Quadrat desselben Abstands. Die Standarddämpfungsfaktoren sind (1,0,0), was zu keiner Dämpfung führt.<br/>                   |



 

</dd> <dt>

*param* 
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

Die **glLightf-Funktion** legt den Wert oder die Werte einzelner Lichtquellenparameter fest. Der *Lichtparameter* benennt das Licht und ist ein symbolischer Name der Form GL \_ LIGHT *i,* wobei 0 = *i <* GL \_ MAX \_ LIGHTS.

Der *pname-Parameter* gibt einen der Light Source-Parameter an, wiederum durch symbolischen Namen. Der *Parameter param* ist entweder ein einzelner Wert oder ein Zeiger auf ein Array, das die neuen Werte enthält.

Die Beleuchtungsberechnung wird mit [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL LIGHTING aktiviert und \_ deaktiviert. Wenn die Beleuchtung aktiviert ist, tragen die aktivierten Lichtquellen zur Beleuchtungsberechnung bei. Die Lichtquelle *i ist* aktiviert und deaktiviert, **indem glEnable** und **glDisable** mit dem Argument GL \_ LIGHT i verwendet *werden.*

Es ist immer der Fall, dass GL \_ LIGHT *i* = GL \_ LIGHT0 + *i* ist.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glLightf-Funktion** ab:

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



## <a name="see-also"></a>Siehe auch

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

 

 





