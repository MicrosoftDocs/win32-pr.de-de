---
title: glLighti-Funktion (Gl.h)
description: Die glLighti-Funktion gibt Parameterwerte für die Lichtquelle zurück.
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
keywords:
- glLighti-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLighti
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94ec260f0e4e5475cc834c786bc1ba7249b30fabd087030caf3426273adc3012
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493310"
---
# <a name="gllighti-function"></a>glLighti-Funktion

Die **glLighti-Funktion** gibt Parameterwerte für die Lichtquelle zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLighti(
   GLenum light,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*light* 
</dt> <dd>

Der Bezeichner eines Lichts. Die Anzahl der möglichen Beleuchtung hängt von der Implementierung ab, aber mindestens acht Beleuchtungen werden unterstützt. Sie werden durch symbolische Namen der Form GL \_ LIGHT *i* identifiziert, wobei *i* ein Wert ist: 0 bis GL MAX LIGHTS \_ - \_ 1.

</dd> <dt>

*pname* 
</dt> <dd>

Ein einwertiger Lichtquellenparameter für *light*. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL \_ SPOT \_ EXPONENT**</dt> </dl>                                                                                                                                                                             | Der *Parameter param* ist ein einzelner ganzzahliger Wert, der die Intensitätsverteilung des Lichts angibt. Ganzzahl- und Gleitkommawerte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 128 \] werden akzeptiert. <br/> Die effektive Lichtdichte wird durch den Kosinus des Winkels zwischen der Lichtrichtung und der Richtung vom Licht bis zum scheitelpunkt, der ausgelöst wird, auf die Potenz des Spot-Exponenten erhöht. Daher führen höhere Spot-Exponenten zu einer fokussierteren Lichtquelle, unabhängig vom Winkel des Spot-Cutoffs. Der Standard-Spot-Exponent ist 0, was zu einer gleichmäßigen Lichtverteilung führt.<br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                                                                                                                                                                                   | Der *Parameter param* ist ein einzelner ganzzahliger Wert, der den maximalen Verteilungswinkel einer Lichtquelle angibt. Ganzzahl- und Gleitkommawerte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 90 \] und dem Sonderwert 180 werden akzeptiert. <br/> Wenn der Winkel zwischen der Richtung des Lichts und der Richtung vom Licht bis zum scheitelpunkt, der hell wird, größer als der Winkel des Spot-Cutoffs ist, wird das Licht vollständig maskiert. Andernfalls wird die Intensität durch den Spot-Exponenten und die Dämpfungsfaktoren gesteuert. Der Standardmäßige Spot-Cutoff ist 180, was zu einer gleichmäßigen Lichtverteilung führt.<br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**GL \_ CONSTANT \_ ATTENUATION, GL \_ LINEAR \_ ATTENUATION, GL \_ QUADRATIC \_ ATTENUATION**</dt> </dl> | Der *param-Parameter* ist ein einzelner ganzzahliger Wert, der einen der drei lichten Dämpfungsfaktoren angibt. Ganzzahl- und Gleitkommawerte werden direkt zugeordnet. Es werden nur nicht negative Werte akzeptiert. <br/> Wenn das Licht positional und nicht direktional ist, wird seine Intensität durch den Reziprok der Summe von abgeschwägt: den konstanten Faktor, den linearen Faktor multipliziert mit dem Abstand zwischen dem Licht und dem scheitelpunkt, der ausgelöst wird, und den quadratischen Faktor multipliziert mit dem Quadrat des gleichen Abstands. Die Standardfaktoren für die Dämpfung sind (1,0,0), was zu keiner Dämpfung führt.<br/>                   |



 

</dd> <dt>

*param* 
</dt> <dd>

Gibt den Wert an, auf den der Parameter *pname* des *Lichts* der Lichtquelle festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *light* oder *pname* war kein akzeptierter Wert.<br/>                                                                                                                                                                  |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Ein Spot-Exponentwert wurde außerhalb des Bereichs \[ 0, 128 \] oder spot cutoff außerhalb des Bereichs \[ 0, 90 \] (mit Ausnahme des Sonderwerts 180) angegeben, oder es wurde ein negativer Dämpfungsfaktor angegeben.<br/> |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                                                     |



## <a name="remarks"></a>Hinweise

Die **glLighti-Funktion** legt den Wert oder die Werte einzelner Lichtquellenparameter fest. Der *Light-Parameter* benennt das Licht und ist ein symbolischer Name der Form GL \_ LIGHT *i*, wobei 0 = *i* < GL MAX \_ LIGHTS \_ ist.

Der *pname-Parameter* gibt einen der Light Source-Parameter an, wiederum anhand des symbolischen Namens. Der *Parameter param* ist entweder ein einzelner Wert oder ein Zeiger auf ein Array, das die neuen Werte enthält.

Die Beleuchtungsberechnung wird mit [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL LIGHTING aktiviert und \_ deaktiviert. Wenn die Beleuchtung aktiviert ist, tragen die aktivierten Datenquellen zur Beleuchtungsberechnung bei. Die Lichtquelle *i* ist mit **glEnable** und **glDisable** mit dem Argument GL LIGHT i aktiviert und \_ deaktiviert.

Es ist immer der Fall, dass GL \_ LIGHT *i* = GL \_ LIGHT0 + *i* ist.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glLighti-Funktion** ab:

[**glGetLight**](glgetlight.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





