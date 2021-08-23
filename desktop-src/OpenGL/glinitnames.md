---
title: glInitNames-Funktion (Gl.h)
description: Die glInitNames-Funktion initialisiert den Namensstapel.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- glInitNames-Funktion OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a567242431fc90be3b60d8ae08875b585ff6a81794899a6c9eb69e7a0a03daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012118"
---
# <a name="glinitnames-function"></a>glInitNames-Funktion

Die **glInitNames-Funktion** initialisiert den Namensstapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glInitNames-Funktion** bewirkt, dass der Namensstapel in seinen standardmäßig leeren Zustand initialisiert wird. Der Namensstapel wird im Auswahlmodus verwendet, um eine eindeutige Bezeichnung von Sätzen von Renderingbefehlen zu ermöglichen. Sie besteht aus einem geordneten Satz von ganzen Zahlen ohne Vorzeichen.

Der Namensstapel ist immer leer, während der Rendermodus nicht GL \_ SELECT ist. Aufrufe **von glInitNames,** während der Rendermodus nicht GL \_ SELECT ist, werden ignoriert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glInitNames ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ NAME STACK \_ \_ DEPTH

**glGet** mit Argument GL \_ MAX NAME STACK \_ \_ \_ DEPTH

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

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





