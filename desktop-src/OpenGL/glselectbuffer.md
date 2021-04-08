---
title: glselectbuffer-Funktion (GL. h)
description: Die Funktion "glselectbuffer" stellt einen Puffer für Werte im Auswahlmodus her.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- glselectbuffer-Funktion OpenGL
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
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740040"
---
# <a name="glselectbuffer-function"></a>glselectbuffer-Funktion

Die Funktion " **glselectbuffer** " stellt einen Puffer für Werte im Auswahlmodus her.

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

Die Größe des *Puffers*.

</dd> <dt>

*ert* 
</dt> <dd>

Gibt die Auswahl Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Größe* war negativ.<br/>                                                                                                       |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde aufgerufen, während der Rendermodus "GL Select" war \_ .<br/>                                                              |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glselectbuffer** " verfügt über zwei Parameter: " *buffer* " ist ein Zeiger auf ein Array aus ganzen Zahlen ohne Vorzeichen und " *size* " gibt die Größe des Arrays an. Der *buffer* -Parameter gibt Werte aus dem Namen Stapel zurück (siehe [**glinitnames**](glinitnames.md), [**glloadname**](glloadname.md), [**glpushname**](glpushname.md)), wenn der Renderingmodus "GL Select" ist \_ (siehe [**glrendermode**](glrendermode.md)). Die Funktion " **glselectbuffer** " muss ausgegeben werden, bevor der Auswahlmodus aktiviert ist, und Sie darf nicht ausgegeben werden, während der Renderingmodus "GL Select" ist \_ .

Die Auswahl wird von einem Programmierer verwendet, um zu bestimmen, welche primitiven in einem Fensterbereich gezeichnet werden. Der Bereich wird durch die aktuelle Modelview-und perspektivische Matrizen definiert.

Im Auswahlmodus werden keine Pixel Fragmente aus der rasterisierung erzeugt. Wenn ein primitiv das Clip Volume überschneidet, das durch die Anzeige von "Frustum" und die benutzerdefinierten Clippingebenen definiert ist, verursacht dieser Primitive stattdessen eine Auswahl Treffer. (Bei Polygonen findet kein Treffer statt, wenn das Polygon gekullt ist.) Wenn eine Änderung am namens Stapel vorgenommen wird oder wenn " [**glrendermode**](glrendermode.md) " aufgerufen wird, wird ein Treffer Daten Satz in den *Puffer* kopiert, wenn seit dem letzten derartigen Ereignis (entweder eine namens Stapeländerung oder ein " **glrendermode** "-Aufruf) Treffer aufgetreten sind. Der Treffer Daten Satz besteht aus der Anzahl der Namen im Namen Stapel zum Zeitpunkt des Ereignisses. gefolgt von den minimalen und maximalen tiefen Werten aller Scheitel Punkte, die seit dem vorherigen Ereignis getroffen wurden. gefolgt vom Namen Stapel Inhalt, der untere Name wird zuerst angezeigt.

Zurückgegebene tiefen Werte werden so zugeordnet, dass der größte ganzzahlige Wert ohne Vorzeichen der Fenster Koordinaten Tiefe 1,0 entspricht und 0 (null) der Fenster Koordinaten Tiefe 0,0 entspricht.

Ein interner Index in den *Puffer* wird bei der Eingabe des Auswahlmodus auf 0 (null) zurückgesetzt. Jedes Mal, wenn ein Treffer Daten Satz in den *Puffer* kopiert wird, wird der Index inkrementiert, sodass er auf die Zelle unmittelbar nach dem Ende des Blocks von Namespace, d. h. der nächsten verfügbaren Zelle, verweist. Wenn der Treffer Daten Satz größer als die Anzahl der verbleibenden Speicherorte im *Puffer* ist, werden so viele Daten wie möglich kopiert und das Überlauf Kennzeichen festgelegt. Wenn der namens Stapel beim Kopieren eines Treffer Datensatzes leer ist, besteht dieser Datensatz aus 0, gefolgt von den minimalen und maximalen tiefen Werten.

Der Auswahlmodus wird beendet, indem **glrendermode** mit einem anderen Argument als GL \_ SELECT aufgerufen wird. Wenn " **glrendermode** " aufgerufen wird, während der Rendermodus "GL Select" ist \_ , gibt es die Anzahl der in den *Puffer* kopierten Treffer Datensätze zurück, setzt das Überlauf Kennzeichen und den Auswahl Puffer Zeiger zurück und initialisiert den namens Stapel, damit er leer ist. Wenn das Überlauf Bit beim Aufrufen von **glrendermode** festgelegt wurde, wird eine negative Treffer Daten Satz Anzahl zurückgegeben.

Der Inhalt des *Puffers* ist nicht definiert, bis [**glrendermode**](glrendermode.md) mit einem anderen Argument als GL SELECT aufgerufen wird \_ .

Die **glBegin** / -**glEnd** -primitive und Aufrufe von [**glRasterPos**](glrasterpos-functions.md) können zu Treffern führen.

Die folgende Funktion Ruft Informationen im Zusammenhang mit " **glselectbuffer**" ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Name \_ Stack- \_ Tiefe"

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

[**glEnd**](glend.md)
</dt> <dt>

[**glfeedbackbuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glinitnames**](glinitnames.md)
</dt> <dt>

[**glloadname**](glloadname.md)
</dt> <dt>

[**glpushname**](glpushname.md)
</dt> <dt>

[**glrendermode**](glrendermode.md)
</dt> </dl>

 

 





