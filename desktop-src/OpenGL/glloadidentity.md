---
title: glLoadIdentity-Funktion (GL. h)
description: Die Funktion "glLoadIdentity" ersetzt die aktuelle Matrix durch die Identitätsmatrix.
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
ms.openlocfilehash: 0a2afde8ae06602933d6790c4fce33e9130a78cb
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568574"
---
# <a name="glloadidentity-function"></a>glLoadIdentity-Funktion

Die Funktion " **glLoadIdentity** " ersetzt die aktuelle Matrix durch die Identitätsmatrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLoadIdentity(void);
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

Die Funktion " **glLoadIdentity** " ersetzt die aktuelle Matrix durch die Identitätsmatrix. Es ist semantisch äquivalent zum Aufrufen von [**glloadmatrix**](glloadmatrix.md) mit der folgenden Identitätsmatrix.

![Diagramm, das die Identitätsmatrix anzeigt, die von glLoadIdentity aufgerufen wird.](images/load01.png)

In einigen Fällen ist es jedoch effizienter.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glLoadIdentity** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus

**glget** mit dem Argument GL \_ Modelview \_ Matrix

**glget** mit dem Argument GL- \_ Projektions \_ Matrix

**glget** mit Argument GL- \_ Textur \_ Matrix

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

[**glloadmatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





