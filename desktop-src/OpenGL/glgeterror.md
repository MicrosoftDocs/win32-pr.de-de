---
title: glgeterror-Funktion (GL. h)
description: Die glgeterror-Funktion gibt Fehlerinformationen zurück.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- glgeterror-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957023"
---
# <a name="glgeterror-function"></a>glgeterror-Funktion

Die **glgeterror** -Funktion gibt Fehlerinformationen zurück.

## <a name="syntax"></a>Syntax


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die **glgeterror** -Funktion gibt einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                           | Beschreibung                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Für ein Enumerationsobjekt ist ein unzulässiger Wert angegeben. Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.<br/>         |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Ein numerisches Argument liegt außerhalb des zulässigen Bereichs. Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.<br/>                                    |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Der angegebene Vorgang ist im aktuellen Zustand nicht zulässig. Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.<br/>           |
| <dl> <dt>**GL \_ - \_ Fehler**</dt> </dl>          | Es wurde kein Fehler aufgezeichnet. Der Wert dieser symbolischen Konstante ist garantiert 0 (null).<br/>                                                                         |
| <dl> <dt>**GL- \_ Stapel \_ Überlauf**</dt> </dl>    | Diese Funktion würde zu einem Stapelüberlauf führen. Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.<br/>                            |
| <dl> <dt>**GL. \_ Stapel \_ Unterlauf**</dt> </dl>   | Diese Funktion würde einen Stapel Unterlauf verursachen. Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.<br/>                           |
| <dl> <dt>**\_nicht genügend \_ Arbeits \_ Speicher für GL**</dt> </dl>    | Es ist nicht genügend Arbeitsspeicher zum Ausführen der Funktion vorhanden. Der Status OpenGL ist nicht definiert, außer dem Zustand der Fehlerflags, nachdem dieser Fehler aufgezeichnet wurde.<br/> |



 

Beachten Sie, dass " **glgeterror** " den Vorgang "GL invalid" zurückgibt, \_ \_ Wenn er zwischen einem Aufruf von [**glBegin**](glbegin.md) und seinem entsprechenden Aufruf von " [**glEnd**](glend.md)" aufgerufen

## <a name="remarks"></a>Bemerkungen

Jedem erkennbaren Fehler wird ein numerischer Code und ein symbolischer Name zugewiesen. Wenn ein Fehler auftritt, wird das Fehlerflag auf den entsprechenden Fehler Codewert festgelegt. Es werden keine weiteren Fehler aufgezeichnet, bis " **glgeterror** " aufgerufen wird. der Fehlercode wird zurückgegeben, und das Flag wird auf "GL No error" zurückgesetzt \_ \_ . Wenn bei einem Aufrufen von **glgeterror** der Befehl "GL \_ no error" zurück \_ gegeben wird, ist seit dem letzten Aufrufen von " **glgeterror**" bzw. seit dem Initialisieren von OpenGL ein Fehler aufgetreten.

Um verteilte Implementierungen zu ermöglichen, gibt es möglicherweise mehrere Fehlerflags. Wenn ein einzelnes Fehlerflag einen Fehler aufgezeichnet hat, wird der Wert dieses Flags zurückgegeben, und dieses Flag wird auf "GL No error" zurückgesetzt, \_ \_ Wenn " **glgeterror** " aufgerufen wird. Wenn mehr als ein Flag einen Fehler aufgezeichnet hat, gibt **glgeterror** einen beliebigen Fehlerflag-Wert zurück und löscht ihn. Wenn alle Fehlerflags zurückgesetzt werden sollen, sollten Sie in einer Schleife immer " **glgeterror** " aufrufen, bis "GL No error" zurückgegeben wird \_ \_ .

Anfänglich werden alle Fehlerflags auf "GL \_ no error" festgelegt \_ .

Wenn ein Fehlerflag festgelegt ist, sind die Ergebnisse eines OpenGL-Vorgangs nur dann definiert, wenn nicht genügend Arbeitsspeicher verfügbar ist \_ \_ \_ . In allen anderen Fällen wird die Funktion, die den Fehler erzeugt, ignoriert und hat keine Auswirkung auf den OpenGL-Zustand oder Frame Puffer-Inhalt.

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
</dt> </dl>

 

 





