---
title: glDepthMask-Funktion (Gl.h)
description: Die glDepthMask-Funktion aktiviert oder deaktiviert das Schreiben in den Tiefenpuffer.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- glDepthMask-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0e774917d47cecdbb276b19dbc97a7c8c7620e04e0a044cf6932aa83167e325
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625720"
---
# <a name="gldepthmask-function"></a>glDepthMask-Funktion

Die **glDepthMask-Funktion** aktiviert oder deaktiviert das Schreiben in den Tiefenpuffer.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*flag* 
</dt> <dd>

Gibt an, ob der Tiefenpuffer zum Schreiben aktiviert ist. Wenn *das Flag* 0 (null) ist, ist das Schreiben von Tiefenpuffern deaktiviert. Andernfalls ist sie aktiviert. Anfangs ist tiefenpufferbasiertes Schreiben aktiviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die folgende Funktion ruft Informationen im Zusammenhang mit **glDepthMask ab:**

**glGet** mit Argument GL \_ DEPTH \_ WRITEMASK

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

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





