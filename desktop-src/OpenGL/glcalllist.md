---
title: glCallList-Funktion (GL. h)
description: Die Funktion "glCallList" führt eine Anzeigeliste aus.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- glCallList-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104132"
---
# <a name="glcalllist-function"></a>glCallList-Funktion

Die Funktion " **glCallList** " führt eine Anzeigeliste aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*list* 
</dt> <dd>

Der ganzzahlige Name der auszuführenden Anzeigeliste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Aufrufen der Funktion " **glCallList** " beginnt mit der Ausführung der benannten Anzeigeliste. Die in der Anzeigeliste gespeicherten Funktionen werden in der richtigen Reihenfolge ausgeführt, als würden Sie ohne Anzeigeliste aufgerufen. Wenn *List* nicht als Anzeigeliste definiert wurde, wird **glCallList** ignoriert.

Die Funktion " **glCallList** " kann in einer Anzeigeliste angezeigt werden. Um die Möglichkeit der unendlichen Rekursion zu vermeiden, die sich aus Anzeigelisten ergibt, wird während der Ausführung der Anzeigeliste eine Beschränkung auf der Schachtelungs Ebene der Anzeigelisten platziert. Dieser Grenzwert ist mindestens 64, hängt jedoch von der Implementierung ab.

Der OpenGL-Zustand wird nicht in einem Aufruf von **glCallList** gespeichert und wieder hergestellt. Folglich verbleiben Änderungen, die während der Ausführung einer Anzeigeliste an dem OpenGL-Zustand vorgenommen werden, nach Abschluss der Ausführung der Anzeigeliste. Um den OpenGL-Zustand über **glCallList** -Aufrufe beizubehalten, verwenden Sie " [**glpushattab**](glpushattrib.md)", " [**glpopattab**](glpopattrib.md)", " [**glPushMatrix**](glpushmatrix.md)" und " [**glPopMatrix**](glpopmatrix.md)".

Sie können Anzeigelisten zwischen einem Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden " [**glEnd**](glend.md)"-Befehl ausführen, solange die Anzeigeliste nur Funktionen enthält, die in diesem Intervall zulässig sind.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit " **glCallList**" ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max. \_ Listen Schachtelung \_

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

[**glcalllists**](glcalllists.md)
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

 

 





