---
title: glPushName-Funktion (Gl.h)
description: Die Funktionen glPushName und glPopName pushen und popen den Namensstapel. | glPushName-Funktion (Gl.h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- glPushName-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447c4b36822e25d70f0aa387040a76738f280a2b22393b53732941a087ff45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358330"
---
# <a name="glpushname-function"></a>glPushName-Funktion

Die **Funktionen glPushName** und [**glPopName**](glpopname.md) pushen und popen den Namensstapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* 
</dt> <dd>

Ein Name, der auf den Namensstapel pusht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | Die Funktion wurde aufgerufen, während der aktuelle Matrixstapel voll war.<br/>                                                           |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glPushName-Funktion** bewirkt, dass name auf den Namenstapel pusht wird, der anfänglich leer ist. Die [**glPopName-Funktion**](glpopname.md) popt einen Namen aus dem Stapel. Der Namensstapel wird im Auswahlmodus verwendet, um eine eindeutige Bezeichnung von Sätzen von Renderingbefehlen zu ermöglichen. Sie besteht aus einem geordneten Satz von ganzen Zahlen ohne Vorzeichen.

Der Namensstapel ist immer leer, während der Rendermodus nicht GL \_ SELECT ist. Aufrufe **von glPushName oder** [**glPopName,**](glpopname.md) während der Rendermodus nicht GL \_ SELECT ist, werden ignoriert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPushName** und [**glPopName ab:**](glpopname.md)

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ NAME STACK \_ \_ DEPTH

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MAX NAME STACK \_ \_ \_ DEPTH

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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





