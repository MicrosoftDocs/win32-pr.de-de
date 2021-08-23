---
title: glFinish-Funktion (Gl.h)
description: Die glFinish-Funktion wird blockiert, bis die gesamte OpenGL-Ausführung abgeschlossen ist.
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- glFinish-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99d4cb185beb09cb882667b80dbd06a25546fb9209da38a775cefa887443617
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580175"
---
# <a name="glfinish-function"></a>glFinish-Funktion

Die **glFinish-Funktion** wird blockiert, bis die gesamte OpenGL-Ausführung abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glFinish-Funktion** gibt erst dann zurück, wenn die Auswirkungen aller zuvor aufgerufenen OpenGL-Funktionen abgeschlossen sind. Zu diesen Auswirkungen gehören alle Änderungen am OpenGL-Zustand, alle Änderungen am Verbindungszustand und alle Änderungen am Framepufferinhalt.

Die **glFinish-Funktion** erfordert einen Roundtrip zum Server.

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

[**glFlush**](glflush.md)
</dt> </dl>

 

 





