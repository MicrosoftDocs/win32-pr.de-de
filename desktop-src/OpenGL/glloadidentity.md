---
title: glLoadIdentity-Funktion (Gl.h)
description: Die glLoadIdentity-Funktion ersetzt die aktuelle Matrix durch die Identitätsmatrix.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- glLoadIdentity-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c0917dae2ae21acd61b6931bcb683a4f3f85f88af45c20fe6137e464254f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493004"
---
# <a name="glloadidentity-function"></a>glLoadIdentity-Funktion

Die **glLoadIdentity-Funktion** ersetzt die aktuelle Matrix durch die Identitätsmatrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLoadIdentity(void);
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

Die **glLoadIdentity-Funktion** ersetzt die aktuelle Matrix durch die Identitätsmatrix. Sie entspricht semantisch dem Aufrufen [**von glLoadMatrix**](glloadmatrix.md) mit der folgenden Identitätsmatrix.

![Diagramm, das die Identitätsmatrix zeigt, die glLoadIdentity aufruft.](images/load01.png)

In einigen Fällen ist dies jedoch effizienter.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glLoadIdentity ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MATRIX \_ MODE

**glGet** mit Argument GL \_ MODELVIEW \_ MATRIX

**glGet** mit Argument GL \_ PROJECTION \_ MATRIX

**glGet** mit Argument GL \_ TEXTURE \_ MATRIX

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

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





