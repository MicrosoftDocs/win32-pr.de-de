---
title: glLoadName-Funktion (Gl.h)
description: Die glLoadName-Funktion lädt einen Namen in den Namenstapel.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- glLoadName-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f362862d2d4b57c43e12e522e2dac1767bbd36d88bda4ce3fb27f3c525fb3ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520390"
---
# <a name="glloadname-function"></a>glLoadName-Funktion

Die **glLoadName-Funktion** lädt einen Namen in den Namenstapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* 
</dt> <dd>

Ein Name, der den obersten Wert im Namensstapel ersetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde aufgerufen, während der Namensstapel leer war.<br/>                                                                    |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glLoadName-Funktion** *bewirkt, dass name* den Wert oben im Namensstapel ersetzt, der anfänglich leer ist. Der Namensstapel wird im Auswahlmodus verwendet, um eine eindeutige Bezeichnung von Sätzen von Renderingbefehlen zu ermöglichen. Sie besteht aus einem geordneten Satz von ganzen Zahlen ohne Vorzeichen.

Der Namensstapel ist immer leer, während der Rendermodus nicht GL \_ SELECT ist. Aufrufe **von glLoadName,** während der Rendermodus nicht GL \_ SELECT ist, werden ignoriert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glLoadName ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ NAME \_ STACK \_ DEPTH

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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





