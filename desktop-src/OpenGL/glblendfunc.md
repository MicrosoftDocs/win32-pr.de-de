---
title: glblendfunc-Funktion (GL. h)
description: Die Funktion "glblendfunc" gibt Pixel Arithmetik an.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- glblendfunc-Funktion OpenGL
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
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344476"
---
# <a name="glblendfunc-function"></a>glblendfunc-Funktion

Die Funktion " **glblendfunc** " gibt Pixel Arithmetik an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sfactor* 
</dt> <dd>

Gibt an, wie die Quell Mischungs Faktoren für Rot, grün, blau und Alpha berechnet werden. Neun symbolische Konstanten werden akzeptiert: GL \_ zero, GL \_ One, GL \_ DST \_ Color, GL \_ One \_ minus \_ DST \_ Color, GL \_ src \_ Alpha, GL \_ One \_ minus \_ src \_ Alpha, GL \_ DST \_ Alpha, GL \_ One \_ minus \_ DST \_ Alpha und GL \_ src \_ alpha \_ inteate.

</dd> <dt>

*Dfactor* 
</dt> <dd>

Gibt an, wie die roten, grünen, blauen und Alpha-zielmischungs Faktoren berechnet werden. Acht symbolische Konstanten werden akzeptiert: GL \_ zero, GL \_ One, GL \_ src \_ Color, GL \_ One \_ minus \_ src \_ Color, GL \_ src \_ Alpha, GL \_ One \_ minus \_ src \_ Alpha, GL \_ DST \_ Alpha und GL \_ One minus \_ \_ DST \_ alpha.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Sfactor* oder *Dfactor* war kein akzeptierter Wert.<br/>                                                                   |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Im RGB-Modus können Pixel mithilfe einer Funktion gezeichnet werden, die die eingehenden (Quell-) RGBA-Werte mit den RGBA-Werten kombiniert, die bereits im Frame Puffer (den Zielwerten) vorhanden sind. Standardmäßig ist Blending deaktiviert. Verwenden Sie [**glEnable**](glenable.md) und [**glEnable**](gldisable.md) mit dem GL- \_ Argument GL, um das Mischen zu aktivieren und zu deaktivieren.

Wenn diese Option aktiviert ist, definiert **glblendfunc** den Mischungs Vorgang. Der *sfactor* -Parameter gibt an, welche von neun Methoden zum Skalieren der Quell Farbkomponenten verwendet werden. Der *Dfactor* -Parameter gibt an, welche von acht Methoden zum Skalieren der Ziel Farbkomponenten verwendet werden. Die elf möglichen Methoden werden in der folgenden Tabelle beschrieben. Jede Methode definiert vier Skalierungsfaktoren für Rot, grün, blau und alpha.

In der Tabelle und in nachfolgenden Gleichungen werden Quell-und Ziel Farbkomponenten als (*R*? , *G*? , *B*? , *A*? ) und (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *a*<sub>d</sub> ). Sie haben einen ganzzahligen Wert zwischen 0 (null) und (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>r</sub> , *k*<sub>A</sub> ), wobei

*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1

*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1

*k*<sub>b</sub> = 2 <sup>Mio</sup>.*b* -1

*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1

und (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>a</sub> ) ist die Anzahl von roten, grünen, blauen und Alpha-bitflächen.

Quell-und zielskalierungs Faktoren werden als (*s*<sub>r</sub> , *s*<sub>g</sub> , *s*<sub>B</sub> , *s*<sub>a</sub> ) und (*d*<sub>r</sub> , *d*<sub>G</sub> , *d*<sub>b</sub> , *d*<sub>a</sub> ) bezeichnet. Die in der Tabelle beschriebenen Skalierungsfaktoren (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ) stellen entweder den Quell-oder den Ziel Faktor dar. Alle Skalierungsfaktoren haben den Bereich \[ 0, 1 \] .



| Parameter                  | (*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>a</sub>  )                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ null                   | (0, 0, 0, 0)                                                                                                                                                    |
| GL \_ 1                    | (1, 1, 1, 1)                                                                                                                                                    |
| GL- \_ src- \_ Farbe             | (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ 1 \_ minus \_ src- \_ Farbe | (1, 1, 1, 1)-(*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                             |
| GL- \_ DST- \_ Farbe             | (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *G*<sub>d</sub>  /  *k*<sub>G</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )             |
| GL \_ 1 \_ minus \_ DST- \_ Farbe | (1, 1, 1, 1)-(*R*<sub>d</sub>  /  *k*<sub>R</sub> , *G*<sub>d</sub>  /  *k*<sub>G</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> ) |
| GL \_ src \_ Alpha             | (*A*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>A</sub> )                                                         |
| GL \_ One \_ minus \_ src \_ Alpha | (1, 1, 1, 1)-(*A*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>A</sub> )                                             |
| GL- \_ DST- \_ Alpha             | (*A*<sub>d</sub>  /  *k*<sub>A</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> )             |
| GL \_ 1 \_ minus \_ DST- \_ Alpha | (1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> ) |
| GL \_ src \_ alpha- \_ vollständig   | (*i, i, i* , 1)                                                                                                                                                 |



 

In der Tabelle

*i* = min (*A*? , *k*<sub>a</sub>   -  <sub>d</sub> )/ *k*<sub>a</sub>

Zum Ermitteln der gemischten RGBA-Werte eines Pixels beim Zeichnen im RGBA-Modus verwendet das System die folgenden Gleichungen:

*R* (*d*) = min ( *k*<sub>r</sub> , *r*? *s*<sub>r</sub>  +  *r*<sub>d</sub> <sub>r</sub> )

*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  *g*<sub>d</sub> *d*<sub>g</sub> )

*B* (*d*) = min ( *k*<sub>B</sub> *, b*? *s*<sub>b</sub>  +  *b*<sub>d</sub> *b*<sub></sub> )

*A* (*d*) = min ( *k*<sub>A</sub> , *a*? *s*<sub>a</sub>  +  <sub>d</sub> <sub></sub> a)

Trotz der offensichtlichen Genauigkeit der obigen Gleichungen ist das Mischen von Arithmetik nicht genau angegeben, da die Mischung mit unpräzisen ganzzahligen Farbwerten arbeitet. Ein Blend-Faktor, der gleich 1 sein sollte, ist jedoch garantiert, dass seine multipktivität nicht geändert wird, und ein Blend-Faktor, der gleich 0 (null) ist, reduziert seinen Multiplikand auf NULL. Wenn *sfactor* z. b. "GL \_ src Alpha" ist \_ , ist " *Dfactor* " GL \_ One \_ minus \_ src \_ Alpha und "?" gleich *k*<sub>A</sub>. die Gleichungen verringern die einfache Ersetzung: 

*R*<sub>d</sub>  =  *r*?

*G*<sub>d</sub>  =  *g*?

B <sub>d</sub>  =  *b*?

*A*<sub>d</sub>  =  *a*?

## <a name="examples"></a>Beispiele

Transparenz wird am besten mithilfe von **glblendfunc**(GL \_ src \_ Alpha, GL \_ One \_ minus \_ src \_ Alpha) implementiert, wobei primitive vom weitesten zum nächsten sortiert werden. Beachten Sie, dass diese Transparenz Berechnung nicht erfordert, dass Alpha-bitflächen im Framebuffer vorhanden sind.

Sie können auch **glblendfunc**(GL \_ src \_ Alpha, GL \_ One \_ minus \_ src \_ Alpha) zum Rendern von Antialiasing Punkten und Zeilen in beliebiger Reihenfolge verwenden.

Um das Polygon-Antialiasing zu optimieren, verwenden Sie **glblendfunc**(GL \_ src \_ alpha \_ sätate, GL \_ One) mit Polygonen, die von der nächstgelegenen zu weit entfernten sortiert sind. (Siehe GL \_ . Polygon- \_ Smooth-Argument in [**glEnable**](glenable.md) für Informationen zum Polygon-Antialiasing.) Ziel-Alpha bitflächen, die vorhanden sein müssen, damit diese Blend-Funktion ordnungsgemäß funktioniert, speichern die akkumulierte Abdeckung.

Ein eingehender (Quelle) Alpha ist eine Material Deckkraft im Bereich von 1,0 (*K*<sub>a</sub> ), die eine komplette Deckkraft darstellt, bis 0,0 (0), die eine umfassende Transparenz darstellt.

Wenn Sie mehr als einen Farb Puffer für das Zeichnen aktivieren, wird jeder aktivierte Puffer separat gemischt, und der Inhalt des Puffers wird für die Zielfarbe verwendet. (Siehe [**gldrawbuffer**](gldrawbuffer.md).)

Blending wirkt sich nur auf das RGBA-Rendering aus. Sie wird von farbindexrenderatoren ignoriert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glblendfunc** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Blend \_ src

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Blend \_ DST

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Blend

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

[**glalphafunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**gldeaktivieren**](gldisable.md)
</dt> <dt>

[**gldrawbuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**gllogicop**](gllogicop.md)
</dt> <dt>

[**glstencilfunc**](glstencilfunc.md)
</dt> </dl>

 

 





