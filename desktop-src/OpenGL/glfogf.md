---
title: glFogf-Funktion (Gl.h)
description: Die GlFogf-Funktion und die -Funktion geben Parameter für die Metriken an.
ms.assetid: 69961d8f-385c-4353-aef3-38fb654c44f8
keywords:
- glFogf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFogf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 497a053584df3e6993a8c7cf3965345923e7df0745765b320972f7003bb15bde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580240"
---
# <a name="glfogf-function"></a>glFogf-Funktion

Die **GlFogf-Funktion** und die -Funktion geben Parameter für die Metriken an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFogf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pname* 
</dt> <dd>

Gibt einen einwertigen Parameter an.

Akzeptiert einen der folgenden Werte.



| Wert                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**\_GL-MODUS \_**</dt> </dl>          | Der *params-Parameter* ist ein einzelner Gleitkommawert, der die Gleichung angibt, mit der der Blendfaktor *f* berechnet werden soll. Es werden drei symbolische Konstanten akzeptiert: GL \_ LINEAR, GL \_ EXP und GL \_ EXP2. Die Gleichungen, die diesen symbolischen Konstanten entsprechen, werden im folgenden Abschnitt "Hinweise" definiert. Der Standardmodus ist GL \_ EXP.<br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**\_GL-DICHTE \_**</dt> </dl> | Der *params-Parameter* ist ein einzelner Gleitkommawert, der die *Dichte* angibt, die in beiden exponentiellen Gleitkommagleichungen verwendete Dichte der Dichte. Es werden nur nicht negative Dichten akzeptiert. Die Standardmäßige Dichte für Die Dichte beträgt 1,0.<br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**\_GL-START \_**</dt> </dl>       | Der *params-Parameter* ist ein einzelner Gleitkommawert, der *start* angibt. Dies ist der nahe Abstand, der in der linearen Gleitkommagleichung verwendet wird. Der Standardwert für near distance ist 0,0.<br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**GL \_ \_ VERSCHENKTE END**</dt> </dl>             | Der *params-Parameter* ist ein einzelner Gleitkommawert, der *end* angibt, den fernen Abstand, der in der linearen Gleitkommagleichung verwendet wird. Der standardweite Abstand beträgt 1,0.<br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**\_ \_ GLBULS INDEX**</dt> </dl>       | Der *params-Parameter* ist ein einzelner Gleitkommawert, der *i*<sub>f</sub> angibt, den Farbindex der Farben des Gleitkommawerts. Der Standardindex ist 0,0.<br/>                                                                                                                                                                                                           |



 

</dd> <dt>

*param* 
</dt> <dd>

Gibt den Wert an, auf den *pname* festgelegt wird.

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

Die **glFogf-Funktion** weist den Wert oder die Werte in *Parametern* dem durch *pname* angegebenen parameter -Parameter zu.

Blendet eine Farbtonfarbe mit der Posttexturfarbe jedes rasterisierten Pixelfragments unter Verwendung eines Mischungsfaktors *f.* Faktor *f* wird je nach Betriebsmodus auf drei Arten berechnet. Z  ist die Entfernung in Den Augenkoordinaten vom Ursprung zum fragmentierten Fragment. Die Gleichung für GL \_ LINEAR-Gleichung lautet:

![Gleichung, die den Wert von GL_LINEAR zeigt.](images/fog01.png)

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

 

 





