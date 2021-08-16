---
title: glFlush-Funktion (Gl.h)
description: Die glFlush-Funktion erzwingt die Ausführung von OpenGL-Funktionen in endlicher Zeit.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- glFlush-Funktion OpenGL
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
ms.openlocfilehash: ece5f0aa96140b6fa16b5fbde1a857f1e14f1570ad7fc734626a27ac660a65ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360407"
---
# <a name="glflush-function"></a>glFlush-Funktion

Die **glFlush-Funktion** erzwingt die Ausführung von OpenGL-Funktionen in endlicher Zeit.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFlush(void);
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

Verschiedene OpenGL-Implementierungen puffern Befehle an verschiedenen Speicherorten, einschließlich Netzwerkpuffern und dem Grafikbeschleuniger selbst. Die **glFlush-Funktion** leert alle diese Puffer, sodass alle ausgegebenen Befehle so schnell ausgeführt werden, wie sie von der tatsächlichen Rendering-Engine akzeptiert werden. Obwohl diese Ausführung in einem bestimmten Zeitraum möglicherweise nicht abgeschlossen wird, wird sie in einem begrenzten Zeitraum abgeschlossen.

Da jedes OpenGL-Programm über ein Netzwerk oder eine Zugriffstaste ausgeführt werden kann, die Befehle puffert, müssen Sie **glFlush** in allen Programmen aufrufen, die erfordern, dass alle zuvor ausgegebenen Befehle abgeschlossen wurden. Rufen Sie beispielsweise **glFlush** auf, bevor Sie auf Benutzereingaben warten, die vom generierten Image abhängen.

Die **glFlush-Funktion** kann jederzeit zurückgeben. Sie wartet nicht, bis die Ausführung aller zuvor ausgegebenen OpenGL-Funktionen abgeschlossen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFinish**](glfinish.md)
</dt> </dl>

 

 





