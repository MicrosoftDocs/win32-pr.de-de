---
title: glBlendFunc-Funktion (Gl.h)
description: Die glBlendFunc-Funktion gibt die Pixelarithmetik an.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- glBlendFunc-Funktion OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4b079d0eb83f401eb7e906cb399fab18e5b2fd22f06299fcc62b1e6b4a02e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082130"
---
# <a name="glblendfunc-function"></a>glBlendFunc-Funktion

Die **glBlendFunc-Funktion** gibt die Pixelarithmetik an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SFACTOR* 
</dt> <dd>

Gibt an, wie die Faktoren rot, grün, blau und alpha für die Quellenmischung berechnet werden. Neun symbolische Konstanten werden akzeptiert: GL \_ ZERO, GL \_ ONE, GL \_ DST \_ COLOR, GL \_ ONE MINUS \_ \_ DST \_ COLOR, GL \_ SRC \_ ALPHA, GL ONE MINUS \_ \_ \_ SRC \_ ALPHA, GL \_ DST \_ ALPHA, GL ONE MINUS \_ \_ \_ DST ALPHA und GL \_ \_ SRC ALPHA \_ \_ SATURATE.

</dd> <dt>

*dfactor* 
</dt> <dd>

Gibt an, wie die Rot-, Grün-, Blau- und Alpha-Zielmischungsfaktoren berechnet werden. Acht symbolische Konstanten werden akzeptiert: GL \_ ZERO, GL \_ ONE, GL \_ SRC \_ COLOR, GL \_ ONE MINUS \_ \_ SRC \_ COLOR, GL \_ SRC \_ ALPHA, GL ONE MINUS \_ \_ \_ SRC \_ ALPHA, GL \_ DST ALPHA und GL ONE \_ MINUS \_ \_ \_ DST \_ ALPHA.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *Sfactor* oder *dfactor* war kein akzeptierter Wert.<br/>                                                                   |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Im RGB-Modus können Pixel mithilfe einer Funktion gezeichnet werden, die die eingehenden RGBA-Werte (Quelle) mit den RGBA-Werten kombiniert, die sich bereits im Framepuffer (den Zielwerten) befinden. Das Mischen ist standardmäßig deaktiviert. Verwenden Sie [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem GL \_ BLEND-Argument, um blending zu aktivieren und zu deaktivieren.

Wenn diese Option aktiviert ist, definiert **glBlendFunc** den Vorgang des Mischens. Der *sfactor-Parameter* gibt an, welche von neun Methoden zum Skalieren der Quellfarbkomponenten verwendet wird. Der *dfactor-Parameter* gibt an, welche von acht Methoden zum Skalieren der Zielfarbkomponenten verwendet wird. Die elf möglichen Methoden werden in der folgenden Tabelle beschrieben. Jede Methode definiert jeweils vier Skalierungsfaktoren für Rot, Grün, Blau und Alpha.

In der Tabelle und in nachfolgenden Gleichungen werden Quell- und Zielfarbkomponenten als (*R*? , *G*? , *B*? , *A*? ) und (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ). Es wird davon ausgegangen, dass sie ganzzahlige Werte zwischen 0 *(null)* und (k <sub>R,</sub> *k*<sub>G,</sub> *k*<sub>R,</sub> *k*<sub>A)</sub> aufweisen, wobei

*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1

*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1

*k*<sub>B</sub> = 2 <sup>m</sup>*B* - 1

*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1

und (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) ist die Anzahl der Rot-, Grün-, Blau- und Alphabitebenen.

Quell- und Zielskalierenfaktoren werden als (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) und (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ) bezeichnet. Die in der Tabelle beschriebenen Skalierungsfaktoren (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ) stellen entweder Quell- oder Zielfaktoren dar. Alle Skalierungsfaktoren haben einen Bereich von \[ 0,1 \] .



| Parameter                  | (*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ ZERO                   | (0,0,0,0)                                                                                                                                                    |
| GL \_ ONE                    | (1,1,1,1)                                                                                                                                                    |
| GL \_ SRC \_ COLOR             | (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ ONE \_ MINUS \_ SRC \_ COLOR | (1,1,1,1) - (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                             |
| GL \_ DST \_ COLOR             | (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *G*<sub>d</sub>  /  *k*<sub>G</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> )             |
| GL \_ ONE \_ MINUS \_ DST \_ COLOR | (1,1,1,1) – (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *G*<sub>d</sub>  /  *k*<sub>G</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> ) |
| GL \_ SRC \_ ALPHA             | (*A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ ONE \_ MINUS \_ SRC \_ ALPHA | (1,1,1,1) - (*A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> )                                             |
| GL \_ DST \_ ALPHA             | (*A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> )             |
| GL \_ ONE \_ MINUS \_ DST \_ ALPHA | (1,1,1,1) – (*A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>k A , A d  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> ) |
| GL \_ SRC \_ ALPHA \_ SATURATE   | (*i,i,i,* 1)                                                                                                                                                 |



 

In der Tabelle

*i* = min (*A*? , *k*<sub>A</sub>   -  *A*<sub>d</sub> ) / *k*<sub>A</sub>

Um die kombinierten RGBA-Werte eines Pixels beim Zeichnen im RGBA-Modus zu bestimmen, verwendet das System die folgenden Gleichungen:

*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub>  +  *R*<sub>d</sub> *d*<sub>R</sub> )

*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub>  +  *G*<sub>d</sub> *d*<sub>G</sub> )

*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub>  +  *B*<sub>d</sub> *d*<sub>B</sub> )

*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub>  +  *A*<sub>d</sub> *d*<sub>A</sub> )

Trotz der offensichtlichen Genauigkeit der obigen Gleichungen wird die Arithmetik nicht genau angegeben, da das Mischen mit unpräzise ganzzahligen Farbwerten funktioniert. Es ist jedoch garantiert, dass ein Mischungsfaktor, der gleich 1 sein sollte, seine Multiplikand nicht ändert, und ein Mischungsfaktor gleich 0 (null) reduziert die Multiplikand auf 0 (null). Wenn z. *B. Sfactor* GL \_ SRC \_ ALPHA ist, *dfactor* GL \_ ONE MINUS \_ \_ SRC ALPHA und \_ *A*? gleich *k*<sub>A</sub>ist, reduzieren sich die Gleichungen auf einfache Ersetzung:

*R*<sub>d</sub>  =  *R*?

*G*<sub>d</sub>  =  *G*?

B <sub>d</sub>  =  *B*?

*A*<sub>d</sub>  =  *A*?

## <a name="examples"></a>Beispiele

Transparenz wird am besten mit **glBlendFunc**(GL \_ SRC \_ ALPHA, GL \_ ONE MINUS \_ \_ SRC \_ ALPHA) mit Primitiven implementiert, die vom längsten zum nächsten sortiert sind. Beachten Sie, dass diese Transparenzberechnung nicht das Vorhandensein von Alphabitplanen im Framepuffer erfordert.

Sie können auch **glBlendFunc**(GL \_ SRC ALPHA, GL ONE MINUS SRC ALPHA) verwenden, um \_ \_ \_ \_ Antialiasingpunkte und Linien in \_ beliebiger Reihenfolge zu rendern.

Um polygonale Antialiasing zu optimieren, verwenden Sie **glBlendFunc**(GL \_ SRC \_ ALPHA \_ SATURATE, GL ONE) mit Polygonen, die vom nächsten zum \_ längsten sortiert sind. (Siehe GL \_ POLYGON \_ SMOOTH-Argument in [**glEnable**](glenable.md) für Informationen zum Antialiasing von Polygonen.) Ziel-Alphabitplanen, die vorhanden sein müssen, damit diese Blend-Funktion ordnungsgemäß funktioniert, speichern die akkumulierte Abdeckung.

Eingehendes Alpha (Quell alpha) ist eine Materialdurchlässigkeit im Bereich von 1,0 (*K*<sub>A</sub> ), die die vollständige Deckkraft darstellt, bis zu 0,0 (0), die vollständige Transparenz darstellt.

Wenn Sie mehrere Farbpuffer zum Zeichnen aktivieren, wird jeder aktivierte Puffer separat gemischt, und der Inhalt des Puffers wird für die Zielfarbe verwendet. (Siehe [**glDrawBuffer**](gldrawbuffer.md).)

Blending wirkt sich nur auf das RGBA-Rendering aus. Sie wird von Farbindexrenderern ignoriert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glBlendFunc ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ BLEND \_ SRC

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ BLEND \_ DST

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ BLEND

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





