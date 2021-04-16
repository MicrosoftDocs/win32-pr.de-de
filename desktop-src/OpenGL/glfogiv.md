---
title: glFogiv-Funktion (Gl.h)
description: Die Funktion "glfogiv" gibt Nebel Parameter an. | glfogiv-Funktion (GL. h)
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
keywords:
- glfogiv-Funktion OpenGL
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
ms.openlocfilehash: 67fa4fefece05529cf5ff3906f19c5ad6e444249
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530692"
---
# <a name="glfogiv-function"></a>glfogiv-Funktion

Die Funktion " **glfogfv** " gibt Nebel Parameter an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFogiv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Gibt einen Nebel Parameter an.

Akzeptiert einen der folgenden Werte.



| Wert                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**GL- \_ Nebel \_ Modus**</dt> </dl>          | Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der die Gleichung angibt, die zum Berechnen des Nebel Blend Faktors *f* verwendet wird. Drei symbolische Konstanten werden akzeptiert: GL \_ linear, GL \_ exp und GL \_ exp2. Die Gleichungen, die diesen symbolischen Konstanten entsprechen, werden im folgenden Abschnitt mit Hinweisen definiert. Der standardnebelmodus ist GL \_ Exp.<br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**GL- \_ Nebel \_ Dichte**</dt> </dl> | Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der die *Dichte* angibt, die in beiden exponentiellen Nebel Gleichungen verwendete Nebeldichte. Nur nicht negative dichten werden akzeptiert. Die standardmäßige Nebeldichte ist 1,0.<br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**GL. \_ Nebel \_ Anfang**</dt> </dl>       | Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der den *Start* angibt, wobei der Near Distance in der linearen Nebel Gleichung verwendet wird. Der Standardwert für fast Distance ist 0,0.<br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**GL- \_ Nebel \_ Ende**</dt> </dl>             | Der Parameter " *para* meters" ist ein einzelner ganzzahliger Wert, der " *End*" angibt, d. h. der Abstand in der linearen Nebel Gleichung. Der Standardabstand ist 1,0.<br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**GL- \_ Nebel \_ Index**</dt> </dl>       | Der Parameter " *para* meters" ist ein einzelner ganzzahliger Wert, der *i*<sub>f</sub> angibt, dem Nebel Farbindex. Der standardmäßige Nebel Index ist 0,0.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <dt>**GL- \_ Nebel \_ Farbe**</dt> </dl>       | Der Parameter *para* meters enthält vier ganzzahlige Werte oder Gleit Komma Werte, die *C*<sub>f</sub> , die Nebelfarbe, angeben. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0. Gleit Komma Werte werden direkt zugeordnet. Nach der Konvertierung werden alle Farbkomponenten an den Bereich \[ 0, 1 gebunden \] . Die standardmäßige Nebelfarbe ist (0,0).<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt den Wert oder die Werte an, die *PName* zugewiesen werden sollen. Die GL- \_ Nebel \_ Farbe erfordert ein Array mit vier Werten. Alle anderen Parameter akzeptieren ein Array, das nur einen einzelnen Wert enthält.

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

Sie aktivieren und deaktivieren den Nebel mit [**glEnable**](glenable.md) und [**glEnable**](gldisable.md)mithilfe des Arguments GL \_ Fog. Wenn Sie aktiviert ist, wirkt sich der Nebel auf rasterisierte Geometrie, Bitmaps und Pixelblöcke aus, aber nicht auf Puffer Löschvorgänge.

Die Funktion " **glfogiv** " weist den Wert oder die Werte in den *para* Metern dem durch " *PName*" angegebenen Nebel Parameter zu.

Der Nebel kombiniert eine arrayfarbe mit der Post texturturfarbe jedes rasterisierten Pixel Fragments mithilfe eines Mischungs Faktors *f*. Der Faktor *f* wird auf eine von drei Arten berechnet, abhängig vom Nebel Modus. Lassen Sie *z* den Abstand in den Augen Koordinaten vom Ursprung zum Fragment, das gefockt wird, angegeben werden. Die Gleichung für den \_ linearen GL-Nebel lautet:

![Gleichung, die den Wert des Mischungs Faktors in GL_LINEAR Nebelmodus als Funktion der Entfernung anzeigt.](images/fog01.png)

Die Gleichung für GL \_ Exp Nebel lautet:

![Gleichung, die den Wert des Mischungs Faktors in GL_EXP Nebel Modus anzeigt.](images/fog02.png)

Die Gleichung für GL \_ exp2 Nebel lautet:

![Gleichung, die den Wert des Mischungs Faktors in GL_EXP2 Nebel Modus anzeigt.](images/fog03.png)

Unabhängig vom Nebel Modus wird *f* an den Bereich \[ 0, 1, \] nach der Berechnung gebunden. Wenn sich OpenGL im RGBA-Farbmodus befindet, wird die Farbe *C*<sub>r</sub> des Fragments durch ersetzt.

![Gleichung, die die Farbe des Foto Fragments als Funktion der Mischungs Faktor-und Nebelfarbe anzeigt.](images/fog04.png)

Im Farb Index Modus wird der Farb Index *i*<sub>r</sub> des Fragments durch ersetzt.

![Gleichung, die den Farb Index des fogged-Fragments als Funktion des Mischungs Faktors und der indizierten Farbe anzeigt.](images/fog05.png)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit den **glfog** -Funktionen ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Nebelfarbe

**glget** mit dem Argument GL- \_ Nebel \_ Index

**glget** mit dem Argument GL- \_ Nebel \_ Dichte

**glget** mit dem Argument GL \_ Nebel \_ Start

**glget** mit dem Argument GL- \_ Nebel \_ Ende

**glget** mit dem Argument GL- \_ Nebel \_ Modus

[**glisenabled**](glisenabled.md) mit Argument GL \_ Nebel

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

[**gldeaktivieren**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> </dl>

 

 





