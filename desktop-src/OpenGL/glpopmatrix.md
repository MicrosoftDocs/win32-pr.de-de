---
title: glPopMatrix-Funktion (GL. h)
description: Die Funktionen "glPushMatrix" und "glPopMatrix" schieben den aktuellen Matrix Stapel per Push und Pop. | glPopMatrix-Funktion (GL. h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- glPopMatrix-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41424a8af3ca6599edc7a66f9e498632640022c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106367305"
---
# <a name="glpopmatrix-function"></a>glPopMatrix-Funktion

Die Funktionen " [**glPushMatrix**](glpushmatrix.md) " und " **glPopMatrix** " schieben den aktuellen Matrix Stapel per Push und Pop.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Es ist ein Fehler, einen vollständigen Matrix Stapel per Push zu übersetzen oder einen Matrix Stapel zu popzen, der nur eine einzelne Matrix enthält. In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL. \_ Stapel \_ Unterlauf**</dt> </dl>   | Die Funktion wurde aufgerufen, während der aktuelle Matrix Stapel nur eine einzelne Matrix enthielt.<br/>                                     |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Für jeden Matrix Modus gibt es einen Stapel von Matrizen. Im GL- \_ Modelview-Modus ist die Stapel Tiefe mindestens 32. In den beiden anderen Modi, GL \_ Projection und GL \_ Texture, ist die Tiefe mindestens 2. Die aktuelle Matrix in einem beliebigen Modus ist die Matrix am oberen Rand des Stapels für diesen Modus.

Die [**glPushMatrix**](glpushmatrix.md) -Funktion schiebt den aktuellen Matrix Stapel um eins nach unten, wobei die aktuelle Matrix duplizieren wird. Das heißt, nach einem **glPushMatrix** -Befehl ist die Matrix am oberen Rand des Stapels mit der darunter liegenden Matrix identisch. Die Funktion " **glPopMatrix** " holt den aktuellen Matrix Stapel und ersetzt dabei die aktuelle Matrix durch die im Stapel unter dem Stapel. Anfänglich enthält jeder Stapel eine Matrix, eine Identitätsmatrix.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus

**glget** mit dem Argument GL \_ Modelview \_ Matrix

**glget** mit dem Argument GL- \_ Projektions \_ Matrix

**glget** mit Argument GL- \_ Textur \_ Matrix

**glget** mit Argument GL \_ Modelview \_ Stack- \_ Tiefe

**glget** mit der \_ \_ Stapel \_ Tiefe des Arguments GL

**glget** mit Argument GL- \_ Textur \_ Stapel \_ Tiefe

**glget** mit dem Argument GL \_ Max \_ Model View \_ Stack- \_ Tiefe

**glget** mit dem Argument GL \_ Max \_ Projection Stack- \_ \_ Tiefe

**glget** mit der \_ maximalen \_ Textur \_ Stapel \_ Tiefe des Arguments GL

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

[**glfrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glloadmatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**glortho**](glortho.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glrotation**](glrotate.md)
</dt> <dt>

[**glscale**](glscale.md)
</dt> <dt>

[**gltranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





