---
title: glCallLists-Funktion (Gl.h)
description: Die glCallLists-Funktion führt eine Liste von Anzeigelisten aus.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- glCallLists-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e15c382b23558786443f03f57349b2504ad251301e3e195885e276d7dbebe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082110"
---
# <a name="glcalllists-function"></a>glCallLists-Funktion

Die **glCallLists-Funktion** führt eine Liste von Anzeigelisten aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Anzahl der auszuführenden Anzeigelisten.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Werte in *listet* auf. Die folgenden symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | Der *lists-Parameter* wird als Array von Bytes mit Vorzeichen behandelt, die jeweils im Bereich von -128 bis 127 liegen.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | Der *lists-Parameter* wird als Array von Bytes ohne Vorzeichen behandelt, die jeweils im Bereich von 0 bis 255 liegen.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | Der *lists-Parameter* wird als Array von 2-Byte-Ganzzahlen mit Vorzeichen behandelt, die jeweils im Bereich von -32768 bis 32767 liegen.<br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | Der *lists-Parameter* wird als Array von 2-Byte-Ganzzahlen ohne Vorzeichen behandelt, die jeweils im Bereich von 0 bis 65535 liegen.<br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | Der *lists-Parameter* wird als Array von 4-Byte-Ganzzahlen mit Vorzeichen behandelt.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | Der *lists-Parameter* wird als Array von 4-Byte-Ganzzahlen ohne Vorzeichen behandelt.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | Der *lists-Parameter* wird als Array von 4-Byte-Gleitkommawerten behandelt.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <dt>**GL \_ 2 \_ BYTES**</dt> </dl>                      | Der *lists-Parameter* wird als Array von Bytes ohne Vorzeichen behandelt. Jedes Bytepaar gibt einen einzelnen Anzeigelistennamen an. Der Wert des Paars wird als das 256-fache des Werts ohne Vorzeichen des ersten Byte plus des Werts ohne Vorzeichen des zweiten Byte berechnet.<br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <dt>**GL \_ 3 \_ BYTES**</dt> </dl>                      | Der *lists-Parameter* wird als Array von Bytes ohne Vorzeichen behandelt. Jedes Triplet von Bytes gibt einen einzelnen Anzeigelistennamen an. Der Wert des Triplets wird als das 65536-fache des Werts ohne Vorzeichen des ersten Byte sowie das 256-fache des Werts ohne Vorzeichen des zweiten Byte plus des Werts ohne Vorzeichen des dritten Byte berechnet.<br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <dt>**GL \_ 4 \_ BYTES**</dt> </dl>                      | Der *lists-Parameter* wird als Array von Bytes ohne Vorzeichen behandelt. Jedes Quadruplet von Bytes gibt einen einzelnen Anzeigelistennamen an. Der Wert des Quadruplets wird berechnet, wenn 16777216 mal der Wert ohne Vorzeichen des ersten Byte plus das 65536-fache des werts ohne Vorzeichen des zweiten Byte plus das 256-fache des werts ohne Vorzeichen des dritten Byte plus des Werts ohne Vorzeichen des vierten Bytes ist.<br/> |



 

</dd> <dt>

*Listen* 
</dt> <dd>

Die Adresse eines Arrays von Namensoffsets in der Anzeigeliste. Der Zeigertyp ist void, da die Offsets je nach Wert des *Typs* Bytes, Shorts, Ints oder Floats sein können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glCallLists-Funktion** bewirkt, dass jede Anzeigeliste in der Liste der als *Listen* übergebenen Namen ausgeführt wird. Daher werden die in jeder Anzeigeliste gespeicherten Funktionen in der reihenfolge ausgeführt, als ob sie aufgerufen würden, ohne eine Anzeigeliste zu verwenden. Namen von Anzeigelisten, die nicht definiert wurden, werden ignoriert.

Die **glCallLists-Funktion** stellt eine effiziente Möglichkeit zum Ausführen von Anzeigelisten bereit. Der *n-Parameter* gibt die Anzahl der Listen mit verschiedenen Namenformaten (angegeben durch den *Typparameter)* an, die **von glCallLists** ausgeführt werden.

Die Liste der Anzeigelistennamen ist nicht NULL-terminiert. Stattdessen gibt *n* an, wie viele Namen aus *Listen* entnommen werden sollen.

Die [**glListBase-Funktion**](gllistbase.md) stellt eine zusätzliche Dekonstruktionsebene zur Verfügung. Die **glListBase-Funktion** gibt einen Offset ohne Vorzeichen an, der jedem Anzeigelistennamen hinzugefügt wird, der in *Listen* angegeben ist, bevor diese Anzeigeliste ausgeführt wird.

Die **glCallLists-Funktion** kann in einer Anzeigeliste angezeigt werden. Um die Möglichkeit einer unendlichen Rekursion zu vermeiden, die sich aus aufrufenden Anzeigelisten ergibt, wird während der Ausführung der Anzeigeliste ein Grenzwert auf der Schachtelungsebene von Anzeigelisten festgelegt. Dieser Grenzwert muss mindestens 64 sein und hängt von der Implementierung ab.

Der OpenGL-Zustand wird nicht über einen Aufruf von **glCallLists** gespeichert und wiederhergestellt. Daher bleiben Änderungen, die während der Ausführung der Anzeigelisten am OpenGL-Zustand vorgenommen werden, nach Abschluss der Ausführung erhalten. Verwenden Sie [**glPushAttrib,**](glpushattrib.md) [**glPopAttrib,**](glpopattrib.md) [**glPushMatrix**](glpushmatrix.md)und [**glPopMatrix,**](glpopmatrix.md) um den OpenGL-Zustand über **glCallLists-Aufrufe** hinweg beizubehalten.

Sie können Anzeigelisten zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)ausführen, solange die Anzeigeliste nur Funktionen enthält, die in diesem Intervall zulässig sind.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glCallLists-Funktion** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ LIST \_ BASE

**glGet** mit argument GL \_ MAX \_ LIST \_ NESTING

[**glIsList**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glListBase**](gllistbase.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





