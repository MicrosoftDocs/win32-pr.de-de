---
title: glFogiv-Funktion (Gl.h)
description: Die glFogiv-Funktion gibt Parameter für die Metriken an. | glFogiv-Funktion (Gl.h)
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
keywords:
- glFogiv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFogiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4e22fddbd6c89a219c296c4fa0161f3992be195a91b38ab512c493241430fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061713"
---
# <a name="glfogiv-function"></a>glFogiv-Funktion

Die **glFogfv-Funktion** gibt Parameter für die Gleitsicht an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFogiv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pname* 
</dt> <dd>

Gibt einen Parameter für die Metriken an.

Akzeptiert einen der folgenden Werte.



| Wert                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**\_GL-MODUS \_**</dt> </dl>          | Der *parameter-Parameter* ist ein einzelner ganzzahliger Wert, der die Gleichung angibt, die zum Berechnen des Mischungsfaktors "blend" *(f)* verwendet werden soll. Es werden drei symbolische Konstanten akzeptiert: GL \_ LINEAR, GL \_ EXP und GL \_ EXP2. Die Gleichungen, die diesen symbolischen Konstanten entsprechen, werden im folgenden Abschnitt "Hinweise" definiert. Der Standardmodus ist GL \_ EXP.<br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**\_GL-DICHTE \_**</dt> </dl> | Der *params-Parameter* ist ein einzelner ganzzahliger Wert, der *die Dichte* angibt, die in beiden exponentiellen Formeln verwendete Dichte. Es werden nur nicht negative Dichten akzeptiert. Die Standardmäßige Dichte für Die Dichte beträgt 1,0.<br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**\_GL-START \_**</dt> </dl>       | Der *params-Parameter* ist ein einzelner ganzzahliger Wert, der *start* angibt, die in der linearen Formel verwendete Entfernung in der Nähe. Der Standardwert für near distance ist 0,0.<br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**GL \_ \_ VERSCHENKTE END**</dt> </dl>             | Der *parameter-Parameter* ist ein einzelner ganzzahliger Wert, der *end* angibt, den fernen Abstand, der in der linearen Formel verwendet wird. Der standardweite Abstand beträgt 1,0.<br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**\_ \_ GLBULS INDEX**</dt> </dl>       | Der *parameter-Parameter* ist ein einzelner ganzzahliger Wert, der *i*<sub>f</sub> angibt, den Farbindex der Farbe "color". Der Standardindex ist 0,0.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <dt>**GL \_ FOG \_ COLOR**</dt> </dl>       | Der *params-Parameter* enthält vier ganzzahlige Werte oder Gleitkommawerte, die *C*<sub>f</sub> , die Farbtonfarbe, angeben. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Nach der Konvertierung werden alle Farbkomponenten an den Bereich \[ 0,1 \] klammern. Die Standardfarbe ist (0,0,0,0).<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt den Wert oder die Werte an, die *pname* zugewiesen werden sollen. GL \_ COLOR COLOR erfordert ein Array von vier \_ Werten. Alle anderen Parameter akzeptieren ein Array, das nur einen einzelnen Wert enthält.

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

Sie aktivieren und deaktivieren Dies ist mit [**glEnable**](glenable.md) und [**glDisable**](gldisable.md)möglich. Verwenden Sie dazu das Argument GL \_ CSV. Während diese Option aktiviert ist, wirkt sich dies auf gerasterte Geometrie, Bitmaps und Pixelblöcke aus, jedoch nicht auf Vorgänge zum Löschen von Puffern.

Die **glFogiv-Funktion** weist den Wert oder die Werte in *Parametern* dem durch *pname* angegebenen parameter -Parameter zu.

Blendet eine Farbtonfarbe mit der Posttexturfarbe jedes rasterisierten Pixelfragments unter Verwendung eines Mischungsfaktors *f.* Faktor *f* wird je nach Betriebsmodus auf drei Arten berechnet. Z  ist die Entfernung in Den Augenkoordinaten vom Ursprung zum fragmentierten Fragment. Die Gleichung für GL \_ LINEAR-Gleichung lautet:

![Gleichung, die den Wert des Mischungsfaktors im GL_LINEAR Mode der Mode mode as a function of distance (Abstandsfunktion) zeigt.](images/fog01.png)

Die Gleichung für GL \_ EXP-Gleichung lautet:

![Gleichung, die den Wert des Mischungsfaktors im GL_EXP Mode zeigt.](images/fog02.png)

Die Gleichung für GL \_ EXP2-Gleichung lautet:

![Gleichung, die den Wert des Mischungsfaktors im GL_EXP2 Mode zeigt.](images/fog03.png)

Unabhängig vom Modus wird *f* nach der Berechnung an den Bereich \[ 0,1 \] angepasst. Wenn sich OpenGL dann im RGBA-Farbmodus befindet, wird die Farbe *C*<sub>r</sub> des Fragments durch ersetzt.

![Gleichung, die die Farbe des verknüpften Fragments als Funktion der Mischungsfaktor- und Farbfarbe zeigt.](images/fog04.png)

Im Farbindexmodus <sub>wird</sub> der Farbindex des Fragments *durch* ersetzt.

![Gleichung, die den Farbindex des fragmentierten Fragments als Funktion des Mischungsfaktors und der indizierten Farbe zeigt.](images/fog05.png)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit den **glFog-Funktionen** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ COLOR \_

**glGet** mit dem Argument GL \_ \_ VERSCHENKUNGSINDEX

**glGet** mit dem Argument GL \_ DENSITY \_ DENSITY

**glGet** mit dem Argument GL \_ \_ VERSCHENKUNGSSTART

**glGet** mit dem Argument GL \_ BACKEND \_ END

**glGet** mit dem Argument GL \_ \_ VERSCHENKUNGSMODUS

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ VERSCHENK

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





