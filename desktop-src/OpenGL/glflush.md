---
title: glflush-Funktion (GL. h)
description: Die glflush-Funktion erzwingt die Ausführung von OpenGL-Funktionen in endlicher Zeit.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- glflush-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743873"
---
# <a name="glflush-function"></a>glflush-Funktion

Die **glflush** -Funktion erzwingt die Ausführung von OpenGL-Funktionen in endlicher Zeit.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Verschiedene OpenGL-Implementierungen Puffern Befehle an verschiedenen Stellen, einschließlich Netzwerkpuffern und Grafikbeschleuniger selbst. Die Funktion " **glflush** " Leert alle diese Puffer und bewirkt, dass alle ausgestellten Befehle so schnell ausgeführt werden, wie Sie von der tatsächlichen Renderingengine akzeptiert werden. Obwohl diese Ausführung möglicherweise nicht in einem bestimmten Zeitraum abgeschlossen ist, wird Sie in einer begrenzten Zeitspanne abgeschlossen.

Da jedes OpenGL-Programm über ein Netzwerk oder eine Zugriffstaste, die Befehle puffert, ausgeführt werden kann, müssen Sie in allen Programmen, die erfordern, dass alle zuvor ausgestellten Befehle abgeschlossen wurden, " **glflush** " aufzurufen. Nennen Sie z. b. **glflush** , bevor Sie auf Benutzereingaben warten, die vom generierten Bild abhängen.

Die **glflush** -Funktion kann jederzeit zurückgeben. Er wartet nicht, bis die Ausführung aller zuvor ausgestellten OpenGL-Funktionen vollständig ist.

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

[**glfinish**](glfinish.md)
</dt> </dl>

 

 





