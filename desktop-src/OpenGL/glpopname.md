---
title: glPopName-Funktion (Gl.h)
description: Die Funktionen glPushName und glPopName pushen und poppen den Namenstapel. | glPopName-Funktion (Gl.h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- glPopName-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe30aa09d401fc8ef35a3671e02a898776af26111ae0f8e31cd1f6ad3bff70b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290170"
---
# <a name="glpopname-function"></a>glPopName-Funktion

Die [**Funktionen glPushName**](glpushname.md) und **glPopName** pushen und poppen den Namenstapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | Die Funktion wurde aufgerufen, während der aktuelle Matrixstapel nur eine einzelne Matrix enthielt.<br/>                                     |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die [**glPushName-Funktion**](glpushname.md) bewirkt, dass name auf den Namenstapel pusht wird, der anfänglich leer ist. Die **glPopName-Funktion** popt einen Namen aus dem Stapel. Der Namensstapel wird im Auswahlmodus verwendet, um eine eindeutige Bezeichnung von Sätzen von Renderingbefehlen zu ermöglichen. Sie besteht aus einem geordneten Satz von ganzen Zahlen ohne Vorzeichen.

Der Namensstapel ist immer leer, während der Rendermodus nicht GL \_ SELECT ist. Aufrufe [**von glPushName oder**](glpushname.md) **glPopName,** während der Rendermodus nicht GL \_ SELECT ist, werden ignoriert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glPushName**](glpushname.md) und **glPopName ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ NAME \_ STACK \_ DEPTH

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MAX NAME STACK \_ \_ \_ DEPTH

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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





