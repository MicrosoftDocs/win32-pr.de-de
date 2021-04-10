---
title: glcalllists-Funktion (GL. h)
description: Die Funktion "glcalllists" führt eine Liste von Anzeigelisten aus.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- glcalllists-Funktion OpenGL
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
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956606"
---
# <a name="glcalllists-function"></a>glcalllists-Funktion

Die Funktion " **glcalllists** " führt eine Liste von Anzeigelisten aus.

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

Die Anzahl der auszuführenden anzeigen Listen.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Werte in *Listen*. Die folgenden symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ Byte**</dt> </dl>                                | Der *lists* -Parameter wird als Array mit signierten Bytes behandelt, jeweils im Bereich von-128 bis 127.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL- \_ Byte ohne Vorzeichen \_**</dt> </dl>    | Der *lists* -Parameter wird als Array von Bytes ohne Vorzeichen behandelt, die jeweils im Bereich von 0 bis 255 liegen.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ Short**</dt> </dl>                             | Der *lists* -Parameter wird als Array von ganzen Zahlen mit Vorzeichen und 2 Bytes behandelt, jeweils im Bereich von-32768 bis 32767.<br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ unsigned \_ Short**</dt> </dl> | Der *lists* -Parameter wird als Array nicht signierter 2-Byte-Ganzzahlen behandelt, wobei jede im Bereich zwischen 0 und 65535 liegt.<br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Der *lists* -Parameter wird als Array von mit Vorzeichen enden 4-Byte-Ganzzahlen behandelt.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ unsigned \_ int**</dt> </dl>       | Der *lists* -Parameter wird als Array nicht signierter 4-Byte-Ganzzahlen behandelt.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ float**</dt> </dl>                             | Der *lists* -Parameter wird als Array von 4-Byte-Gleit Komma Werten behandelt.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <dt>**GL \_ 2 \_ Bytes**</dt> </dl>                      | Der *lists* -Parameter wird als Array nicht signierter Bytes behandelt. Jedes Byte paar gibt einen einzelnen anzeigen Listennamen an. Der Wert des Paars wird als 256-fache des nicht signierten Werts des ersten Bytes zuzüglich des unsignierten Werts des zweiten Bytes berechnet.<br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <dt>**GL. \_ 3 \_ Bytes**</dt> </dl>                      | Der *lists* -Parameter wird als Array nicht signierter Bytes behandelt. Jede dreier Größe von Bytes gibt einen einzelnen anzeigen Listennamen an. Der Wert der-Zeichenfolge wird als 65536-fache des unsignierten Werts des ersten Bytes zuzüglich 256 mal des unsignierten Werts des zweiten Bytes zuzüglich des Werts ohne Vorzeichen des dritten Bytes berechnet.<br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <dt>**GL \_ 4 \_ Bytes**</dt> </dl>                      | Der *lists* -Parameter wird als Array nicht signierter Bytes behandelt. Jedes Vierbeiner von Bytes gibt einen einzelnen anzeigen Listennamen an. Der Wert des quadrupleps wird als 16777216-fache des unsignierten Werts des ersten Bytes zuzüglich 65536 Mal des unsignierten Werts des zweiten Bytes Plus 256-mal des Werts ohne Vorzeichen des dritten Bytes und des Werts ohne Vorzeichen des vierten Bytes berechnet.<br/> |



 

</dd> <dt>

*aufli* 
</dt> <dd>

Die Adresse eines Arrays von namens Offsets in der Anzeigeliste. Der Zeigertyp ist "void", da die Offsets abhängig vom Wert des *Typs* bytes, kurze, int oder Gleit Komma Werte sein können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion **glcalllists** bewirkt, dass jede Anzeigeliste in der Liste der Namen ausgeführt wird, die als *Listen* übergeben werden. Folglich werden die in jeder Anzeigeliste gespeicherten Funktionen in der richtigen Reihenfolge ausgeführt, als würden Sie ohne Anzeigeliste aufgerufen werden. Namen von anzeigen Listen, die nicht definiert wurden, werden ignoriert.

Die Funktion **glcalllists** bietet eine effiziente Möglichkeit zum Ausführen von Anzeigelisten. Der Parameter " *n* " gibt die Anzahl der Listen mit verschiedenen namens Formaten an (angegeben durch den *Typparameter* ) " **glcalllists** " wird ausgeführt.

Die Liste der Namen der Anzeigenliste wird nicht mit Null beendet. Stattdessen gibt *n* an, wie viele Namen aus *Listen* entnommen werden sollen.

Die [**gllistbase**](gllistbase.md) -Funktion stellt eine zusätzliche dereferenzierungsstufe zur Verfügung. Die **gllistbase** -Funktion gibt einen nicht signierten Offset an, der in *Listen* vor der Ausführung der Anzeigeliste hinzugefügt wird.

Die Funktion " **glcalllists** " kann in einer Anzeigeliste angezeigt werden. Um die Möglichkeit der unendlichen Rekursion zu vermeiden, die sich aus Anzeigelisten ergibt, wird während der Ausführung der Anzeigeliste eine Beschränkung auf der Schachtelungs Ebene der Anzeigelisten platziert. Diese Beschränkung muss mindestens 64 betragen, und Sie hängt von der Implementierung ab.

Der OpenGL-Zustand wird nicht in einem Aufruf von **glcalllists** gespeichert und wieder hergestellt. Folglich verbleiben Änderungen, die während der Ausführung der Anzeigelisten am OpenGL-Zustand vorgenommen werden, nach Abschluss der Ausführung. Verwenden Sie " [**glpushattab**](glpushattrib.md)", " [**glpopatpub**](glpopattrib.md)", " [**glPushMatrix**](glpushmatrix.md)" und " [**glPopMatrix**](glpopmatrix.md) ", um den OpenGL-Zustand über **glcalllists** -Aufrufe beizubehalten.

Sie können Anzeigelisten zwischen einem Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden " [**glEnd**](glend.md)"-Befehl ausführen, solange die Anzeigeliste nur Funktionen enthält, die in diesem Intervall zulässig sind.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glcalllists** " ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument-GL- \_ Listen \_ Basis

**glget** mit dem Argument GL \_ Max. \_ Listen Schachtelung \_

[**glislist**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**gldelta etelists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgenlists**](glgenlists.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glislist**](glislist.md)
</dt> <dt>

[**gllistbase**](gllistbase.md)
</dt> <dt>

[**glnewlist**](glnewlist.md)
</dt> <dt>

[**glpopattenb**](glpopattrib.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glpushatpub**](glpushattrib.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





