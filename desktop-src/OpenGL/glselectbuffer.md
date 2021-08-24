---
title: glSelectBuffer-Funktion (Gl.h)
description: Die glSelectBuffer-Funktion richtet einen Puffer für Auswahlmoduswerte ein.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- glSelectBuffer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c40030c34ece43f4e24ac6937c35400fed7ab7acc005e99c653b233e08b69e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519820"
---
# <a name="glselectbuffer-function"></a>glSelectBuffer-Funktion

Die **glSelectBuffer-Funktion** richtet einen Puffer für Auswahlmoduswerte ein.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*size* 
</dt> <dd>

Die Größe des *Puffers.*

</dd> <dt>

*Puffer* 
</dt> <dd>

Gibt die Auswahldaten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *size* war negativ.<br/>                                                                                                       |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde aufgerufen, während der Rendermodus GL \_ SELECT lautete.<br/>                                                              |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glSelectBuffer-Funktion** verfügt über zwei Parameter: *buffer* ist ein Zeiger auf ein Array von ganzen Zahlen ohne Vorzeichen, und *size* gibt die Größe des Arrays an. Der *Pufferparameter* gibt Werte aus dem Namensstapel zurück (siehe [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)), wenn der Renderingmodus GL SELECT ist \_ (siehe [**glRenderMode**](glrendermode.md)). Die **glSelectBuffer-Funktion** muss ausgegeben werden, bevor der Auswahlmodus aktiviert wird, und sie darf nicht ausgegeben werden, während der Renderingmodus GL \_ SELECT lautet.

Die Auswahl wird von einem Programmierer verwendet, um zu bestimmen, welche Primitive in einen Bereich eines Fensters gezeichnet werden. Der Bereich wird durch die aktuelle Modellansicht und die aktuellen Perspektivenmatrizen definiert.

Im Auswahlmodus werden keine Pixelfragmente aus der Rasterung erstellt. Wenn ein primitiver stattdessen das durch das Anzeigen des Frustums definierte Clipvolume und die benutzerdefinierten Clippingebenen überschneidet, verursacht dieses Primitive einen Auswahltreffer. (Bei Polygonen tritt kein Treffer auf, wenn das Polygon gekäutert wird.) Wenn eine Änderung am Namensstapel vorgenommen wird oder [**glRenderMode**](glrendermode.md) aufgerufen wird, wird ein Trefferdatensatz in den *Puffer* kopiert, wenn seit dem letzten Solchen Ereignis Treffer aufgetreten sind (entweder eine Namensstapeländerung oder ein **glRenderMode-Aufruf).** Der Trefferdatensatz besteht aus der Anzahl der Namen im Namensstapel zum Zeitpunkt des Ereignisses. gefolgt von den minimalen und maximalen Tiefenwerten aller Scheitelpunkte, die seit dem vorherigen Ereignis erreicht wurden; gefolgt vom Inhalt des Namensstapels, unterer Name zuerst.

Zurückgegebene Tiefenwerte werden so zugeordnet, dass der größte ganzzahlige Wert ohne Vorzeichen der Fensterkoordinatentiefe 1,0 und 0 (null) der Fensterkoordinatentiefe 0,0 entspricht.

Ein interner Index in *buffer* wird immer dann auf 0 (null) zurückgesetzt, wenn der Auswahlmodus aktiviert wird. Jedes Mal, wenn ein Trefferdatensatz in den *Puffer* kopiert wird, wird der Index inkrementiert, um auf die Zelle direkt hinter dem Ende des Namensblocks zu zeigen, d.h. auf die nächste verfügbare Zelle. Wenn der Trefferdatensatz größer als die Anzahl der verbleibenden Speicherorte im *Puffer* ist, werden so viele Daten wie geeignet kopiert, und das Überlaufflag wird festgelegt. Wenn der Namensstapel beim Kopieren eines Trefferdatensatzes leer ist, besteht dieser Datensatz aus 0 (null), gefolgt von den minimalen und maximalen Tiefenwerten.

Der Auswahlmodus wird beendet, indem **glRenderMode** mit einem anderen Argument als GL SELECT aufgerufen \_ wird. Wenn **glRenderMode** aufgerufen wird, während der Rendermodus GL \_ SELECT lautet, gibt es die Anzahl der Trefferdatensätze zurück, die in *den Puffer* kopiert wurden, setzt das Überlaufflag und den Auswahlpufferzeiger zurück und initialisiert den Namensstapel als leer. Wenn das Überlaufbit beim Aufruf von **glRenderMode** festgelegt wurde, wird eine negative Trefferdatensatzanzahl zurückgegeben.

Der Inhalt des *Puffers* ist nicht definiert, bis [**glRenderMode**](glrendermode.md) mit einem anderen Argument als GL SELECT aufgerufen \_ wird.

Die **glBegin** / **glEnd-Primitive** und Aufrufe von [**glRasterPos**](glrasterpos-functions.md) können zu Treffern führen.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glSelectBuffer** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ NAME \_ STACK \_ DEPTH

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

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





