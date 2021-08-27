---
title: glCallList-Funktion (Gl.h)
description: Die glCallList-Funktion führt eine Anzeigeliste aus.
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
ms.openlocfilehash: 67805ff50eb4566e8a2a186c10229f944f4003baaef1274e9d4f52dd3b9c2a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082120"
---
# <a name="glcalllist-function"></a>glCallList-Funktion

Die **glCallList-Funktion** führt eine Anzeigeliste aus.

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

Der ganzzahlige Name der anzuzeigenden Anzeigeliste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Aufrufen der **glCallList-Funktion** beginnt mit der Ausführung der benannten Anzeigeliste. Die in der Anzeigeliste gespeicherten Funktionen werden in der Reihenfolge ausgeführt, so als ob Sie sie ohne Verwendung einer Anzeigeliste aufgerufen hätten. Wenn *list* nicht als Anzeigeliste definiert wurde, **wird glCallList** ignoriert.

Die **glCallList-Funktion** kann in einer Anzeigeliste angezeigt werden. Um die Möglichkeit einer unendlichen Rekursion zu vermeiden, die sich aus dem Aufrufen von Anzeigelisten ergibt, wird während der Ausführung der Anzeigeliste ein Grenzwert für die Schachtelungsebene von Anzeigelisten gesetzt. Dieser Grenzwert beträgt mindestens 64, hängt jedoch von der Implementierung ab.

Der OpenGL-Status wird nicht gespeichert und über einen Aufruf von **glCallList wiederhergestellt.** Daher bleiben Änderungen am OpenGL-Zustand während der Ausführung einer Anzeigeliste nach Abschluss der Ausführung der Anzeigeliste erhalten. Verwenden Sie [**glPushAttrib,**](glpushattrib.md) [**glPopAttrib,**](glpopattrib.md) [**glPushMatrix**](glpushmatrix.md)und [**glPopMatrix,**](glpopmatrix.md)um den OpenGL-Zustand über **glCallList-Aufrufe** hinweg zu erhalten.

Sie können Anzeigelisten zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)ausführen, solange die Anzeigeliste nur Funktionen enthält, die in diesem Intervall zulässig sind.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glCallList ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MAX \_ LIST \_ NESTING

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

[**glCallLists**](glcalllists.md)
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

 

 





