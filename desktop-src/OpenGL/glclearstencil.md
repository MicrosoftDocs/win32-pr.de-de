---
title: glClearStencil-Funktion (Gl.h)
description: Die glClearStencil-Funktion gibt den eindeutigen Wert für den Schablonenpuffer an.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- glClearStencil-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4749a8d9c4844bd95181a7353bb0ce4559001fa47164fec3dbab5c188de8d994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618030"
---
# <a name="glclearstencil-function"></a>glClearStencil-Funktion

Die **glClearStencil-Funktion** gibt den eindeutigen Wert für den Schablonenpuffer an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*s* 
</dt> <dd>

Der Index, der beim Löschen des Schablonenpuffers verwendet wird. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glClearStencil-Funktion** gibt den Index an, der von [**glClear**](glclear.md) zum Löschen des Schablonenpuffers verwendet wird. Der *s-Parameter* wird mit 2 <sup>m</sup>  bis 1 maskiert, wobei *m* die Anzahl der Bits im Schablonenpuffer ist.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glClearStencil-Funktion** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ STENCIL \_ CLEAR \_ VALUE

**glGet** mit Argument GL \_ STENCIL \_ BITS

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





