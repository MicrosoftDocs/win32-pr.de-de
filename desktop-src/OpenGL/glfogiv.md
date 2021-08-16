---
title: glFogiv-Funktion (Gl.h)
description: Die glFogiv-Funktion gibt parameter an. | glFogiv-Funktion (Gl.h)
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

Die **glFogfv-Funktion** gibt parameter an.

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

Gibt einen Parameter an.

Akzeptiert einen der folgenden Werte.



| Wert                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**\_GL-MODUS \_**</dt> </dl>          | Der *parameter params-Parameter* ist ein einzelner ganzzahliger Wert, der die Gleichung angibt, die zum Berechnen des Blendfaktors der Blend-Formel verwendet werden *soll, f*. Es werden drei symbolische Konstanten akzeptiert: GL \_ LINEAR, GL \_ EXP und GL \_ EXP2. Die Diesen symbolischen Konstanten entsprechenden Gleichungen werden im folgenden Abschnitt "Hinweise" definiert. Der Standardmodus ist GL \_ EXP.<br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**\_ \_ GL-GL-GL-DICHTE**</dt> </dl> | Der *Parameter params* ist ein einzelner ganzzahliger Wert, der die Dichte angibt. Dies ist die Dichte, die in beiden exponentiellen Zahlengleichungen verwendet wird. Es werden nur nicht negative Dichten akzeptiert. Die Standarddichte des Messgeräts ist 1,0.<br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**GL \_ FOG \_ START**</dt> </dl>       | Der *Parameter params* ist ein einzelner ganzzahliger Wert, der *start* angibt. Dies ist die in der linearen Gleichung verwendete Entfernung in der Nähe. Der Standardwert für die Entfernung in der Nähe ist 0,0.<br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**\_GL-END \_**</dt> </dl>             | Der *parameter params-Parameter* ist ein einzelner ganzzahliger Wert, der *end* angibt, die in der linearen Gleichung verwendete Entfernung. Die Standardentfernung ist 1,0.<br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**GL \_ FOG \_ INDEX**</dt> </dl>       | Der *parameter params-Parameter* ist ein einzelner ganzzahliger Wert, der *i*<sub>f</sub> angibt, den Farbindex der Farbe . Der Standardindex ist 0,0.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <dt>**\_ \_ GL-FARBTON**</dt> </dl>       | Der *parameter params-Parameter* enthält vier ganzzahlige Werte oder Gleitkommawerte, die *C*<sub>f</sub> , die Farbe des Farbtons , angeben. Ganzzahlwerte werden linear zugeordnet, damit der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Nach der Konvertierung werden alle Farbkomponenten an den Bereich \[ 0,1 klammern. \] Die Standardfarbe ist (0,0,0,0).<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt den Wert oder die Werte an, die *pname zugewiesen werden sollen.* GL \_ COLOR ERFORDERT ein Array von vier \_ Werten. Alle anderen Parameter akzeptieren ein Array, das nur einen einzelnen Wert enthält.

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

Sie aktivieren und deaktivieren das -Argument [**mit glEnable**](glenable.md) und [**glDisable**](gldisable.md)mithilfe des Arguments GL \_ CHEAT. Während diese Option aktiviert ist, wirkt sich dies auf rasterisierte Geometrie, Bitmaps und Pixelblöcke aus, jedoch nicht auf Vorgänge mit Puffer clear.

Die **glFogiv-Funktion** weist den Wert oder die Werte in *Params* dem parameter an, der von *pname angegeben wird.*

Blenden kombiniert eine Farbenblendung mit der Posttexturfarbe jedes rasterisierten Pixelfragments mithilfe eines Blendingfaktors *f*. Faktor *f* wird auf eine von drei Arten berechnet, je nach Modus "Mode". Lassen *Sie z* den Abstand in den Augenkoordinaten vom Ursprung zum fragmentieren, das überschwemmt wird. Die Gleichung für GL \_ LINEARe Gleichung ist:

![Gleichung, die den Wert des Überblendungsfaktors im GL_LINEAR Modus als Funktion der Entfernung zeigt.](images/fog01.png)

Die Gleichung für GL \_ EXP-Gleichung ist:

![Gleichung, die den Wert des Überblendungsfaktors im GL_EXP modus zeigt.](images/fog02.png)

Die Gleichung für GL \_ EXP2-Gleichung ist:

![Gleichung, die den Wert des Überblendungsfaktors im GL_EXP2 modus zeigt.](images/fog03.png)

Unabhängig vom Mode wird *f* an den Bereich \[ 0,1 klammert, \] nachdem er berechnet wurde. Wenn sich OpenGL dann im RGBA-Farbmodus befindet, wird die Farbe *C*<sub>r</sub> des Fragments durch ersetzt.

![Gleichung, die die Farbe des geschwenkten Fragments als Funktion des Mischens von Faktor- und Farbton zeigt.](images/fog04.png)

Im Farbindexmodus wird der Farbindex des Fragments *i*<sub>r</sub> durch ersetzt.

![Gleichung, die den Farbindex des geschwenkten Fragments als Funktion des Überblendungsfaktors und der indizierten Farbe zeigt.](images/fog05.png)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit den **glFog-Funktionen** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ COLOR \_

**glGet** mit Dem Argument GL \_ INDEX \_

**glGet mit** dem Argument GL \_ DENSITY \_ DENSITY

**glGet** mit Argument GL \_ START \_

**glGet** mit Argument \_ GLENDE \_ END

**glGet** mit Argument GL \_ MODE \_

[**glIsEnabled mit**](glisenabled.md) Dem Argument \_ GLSCHLUSS

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

 

 





