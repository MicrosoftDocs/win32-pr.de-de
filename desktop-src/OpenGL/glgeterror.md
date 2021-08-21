---
title: glGetError-Funktion (Gl.h)
description: Die glGetError-Funktion gibt Fehlerinformationen zurück.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- glGetError-Funktion OpenGL
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
ms.openlocfilehash: 212a76930e87d5a83c32a2f6707def8e2af40b89c5ede621ec0c31159d3aa0c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962400"
---
# <a name="glgeterror-function"></a>glGetError-Funktion

Die **glGetError-Funktion** gibt Fehlerinformationen zurück.

## <a name="syntax"></a>Syntax


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die **glGetError-Funktion** gibt einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                           | Beschreibung                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | Für ein aufzählbares Argument wird ein unzulässiger Wert angegeben. Die anstößige Funktion wird ignoriert und hat keine nebenwirkung, außer das Fehlerflag festzulegen.<br/>         |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Ein numerisches Argument liegt außerhalb des Bereichs. Die anstößige Funktion wird ignoriert und hat keine nebenwirkung, außer das Fehlerflag festzulegen.<br/>                                    |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Der angegebene Vorgang ist im aktuellen Zustand nicht zulässig. Die anstößige Funktion wird ignoriert und hat keine nebenwirkung, außer das Fehlerflag festzulegen.<br/>           |
| <dl> <dt>**GL \_ NO \_ ERROR**</dt> </dl>          | Es wurde kein Fehler aufgezeichnet. Der Wert dieser symbolischen Konstante ist garantiert 0 (null).<br/>                                                                         |
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | Diese Funktion würde einen Stapelüberlauf verursachen. Die anstößige Funktion wird ignoriert und hat keine nebenwirkung, außer das Fehlerflag festzulegen.<br/>                            |
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | Diese Funktion würde einen Stapelunterlauf verursachen. Die anstößige Funktion wird ignoriert und hat keine nebenwirkung, außer das Fehlerflag festzulegen.<br/>                           |
| <dl> <dt>**NICHT \_ \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>    | Es ist nicht mehr genügend Arbeitsspeicher zum Ausführen der Funktion vorhanden. Der Zustand von OpenGL ist nicht definiert, mit Ausnahme des Status der Fehlerflags, nachdem dieser Fehler aufgezeichnet wurde.<br/> |



 

Beachten Sie, dass **glGetError** GL \_ INVALID OPERATION zurückgibt, wenn es zwischen einem Aufruf von \_ [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen wird.

## <a name="remarks"></a>Hinweise

Jedem erkennbaren Fehler werden ein numerischer Code und ein symbolischer Name zugewiesen. Wenn ein Fehler auftritt, wird das Fehlerflag auf den entsprechenden Fehlercodewert festgelegt. Es werden keine weiteren Fehler aufgezeichnet, bis **glGetError** aufgerufen wird, der Fehlercode zurückgegeben wird und das Flag auf GL NO ERROR zurückgesetzt \_ \_ wird. Wenn ein Aufruf von **glGetError** GL \_ NO ERROR zurückgibt, ist seit dem letzten Aufruf von \_ **glGetError** oder seit der Initialisierung von OpenGL kein Fehler erkennbar.

Um verteilte Implementierungen zu ermöglichen, gibt es möglicherweise mehrere Fehlerflags. Wenn ein einzelnes Fehlerflag einen Fehler aufgezeichnet hat, wird der Wert dieses Flags zurückgegeben, und dieses Flag wird auf GL \_ NO ERROR zurückgesetzt, wenn \_ **glGetError** aufgerufen wird. Wenn mehr als ein Flag einen Fehler aufgezeichnet hat, gibt **glGetError** einen beliebigen Fehlerflagwert zurück und löscht einen beliebigen Fehlerflagwert. Wenn alle Fehlerflags zurückgesetzt werden sollen, sollten Sie **glGetError** immer in einer Schleife aufrufen, bis GL NO ERROR zurückgegeben \_ \_ wird.

Anfänglich werden alle Fehlerflags auf GL \_ NO \_ ERROR festgelegt.

Wenn ein Fehlerflag festgelegt ist, sind die Ergebnisse eines OpenGL-Vorgangs nur dann nicht definiert, wenn GL \_ OUT OF MEMORY aufgetreten \_ \_ ist. In allen anderen Fällen wird die Funktion, die den Fehler generiert, ignoriert und hat keine Auswirkungen auf den OpenGL-Zustand oder framebuffer-Inhalt.

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
</dt> </dl>

 

 





