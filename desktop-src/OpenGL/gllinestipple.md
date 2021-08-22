---
title: glLineStipple-Funktion (Gl.h)
description: Die glLineStipple-Funktion gibt das Zeilenausschnittmuster an.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- glLineStipple-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f350611afa0621c1bf883e8f2ac7dc24e50362912296f15d1443e2c638b7bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493020"
---
# <a name="gllinestipple-function"></a>glLineStipple-Funktion

Die **glLineStipple-Funktion** gibt das Zeilenausschnittmuster an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Faktor* 
</dt> <dd>

Ein Multiplikator für jedes Bit im Zeilenausschnittmuster. Wenn *der Faktor* beispielsweise 3 ist, wird jedes Bit im Muster dreimal verwendet, bevor das nächste Bit im Muster verwendet wird. Der *Factor-Parameter* ist an den Bereich \[ 1, 256 und \] standardmäßig auf 1 festgelegt.

</dd> <dt>

*pattern* 
</dt> <dd>

Eine 16-Bit-Ganzzahl, deren Bitmuster bestimmt, welche Fragmente einer Linie gezeichnet werden, wenn die Linie rastert wird. Bit 0 wird zuerst verwendet, und das Standardmuster ist alle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glLineStipple-Funktion** gibt das Zeilenausschnittmuster an. Zeilenausschnitt maskiert bestimmte Fragmente, die durch Rasterung erzeugt werden. diese Fragmente werden nicht gezeichnet. Die Maskierung wird mithilfe von drei Parametern erreicht: dem 16-Bit-Muster des Zeilenausschnittmusters, dem Faktor für die Wiederholungsanzahl und einem ganzzahligen Ausschnittzähler *s*.  

Leistungsindikatoren *werden* immer dann auf 0 (null) zurückgesetzt, wenn [**glBegin**](glbegin.md) aufgerufen wird, und bevor jedes Liniensegment einer **glBegin**(GL \_ LINES)/glEnd-Sequenz generiert wird. Sie wird inkrementiert, nachdem jedes Fragment eines Liniensegments mit Einheitenbreite  mit Alias oder jedes *i-Fragment* eines Liniensegments mit i Breite generiert wurde. Die i-Fragmente, die count *s* zugeordnet sind, werden maskiert, wenn *pattern* bit (*s*   /  *factor*) mod 16 0 (null) ist. Andernfalls werden diese Fragmente an den Framepuffer gesendet. Bit 0 *(null)* des Musters ist das am wenigsten signifikante Bit.

Antialiasinglinien werden zum Ausschnitt als Sequenz von Rechtecke mit einer Breite von 1 x behandelt. *Rechtecksyntisieren* oder nicht basierend auf der für Aliaslinien beschriebenen Fragmentregel. sie zählt Rechtecke anstelle von Gruppen von Fragmenten.

Zeilenausschnitte werden mithilfe von [**glEnable**](glenable.md) und **glDisable** mit dem Argument GL \_ LINE \_ STIPPLE aktiviert oder deaktiviert. Wenn diese Option aktiviert ist, wird das Zeilenausschnittmuster wie oben beschrieben angewendet. Wenn sie deaktiviert ist, ist dies so, als ob es sich bei dem Muster um ein Muster handelte. Anfangs ist der Zeilenausschnitt deaktiviert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glLineStipple ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ LINE \_ STIPPLE \_ PATTERN

**glGet** mit Argument GL \_ LINE \_ STIPPLE \_ REPEAT

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ LINE \_ STIPPLE

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

[**glEnd**](glend.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





