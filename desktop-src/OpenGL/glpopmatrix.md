---
title: glPopMatrix-Funktion (Gl.h)
description: Die Funktionen glPushMatrix und glPopMatrix pushen und popen den aktuellen Matrixstapel. | glPopMatrix-Funktion (Gl.h)
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
ms.openlocfilehash: d1c0f10456c1038da46d9070689713a8237f876bec7ce7da40acf3d81d89ad15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128020"
---
# <a name="glpopmatrix-function"></a>glPopMatrix-Funktion

Die Funktionen [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix** pushen und popen den aktuellen Matrixstapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Es ist ein Fehler, einen vollständigen Matrixstapel zu pushen oder einen Matrixstapel zu popen, der nur eine einzelne Matrix enthält. In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | Die Funktion wurde aufgerufen, während der aktuelle Matrixstapel nur eine einzige Matrix enthielt.<br/>                                     |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Es gibt einen Stapel von Matrizen für jeden Matrixmodus. Im GL \_ MODELVIEW-Modus beträgt die Stapeltiefe mindestens 32. In den anderen beiden Modi GL \_ PROJECTION und GL TEXTURE beträgt die Tiefe mindestens \_ 2. Die aktuelle Matrix in einem beliebigen Modus ist die Matrix oben im Stapel für diesen Modus.

Die [**glPushMatrix-Funktion**](glpushmatrix.md) pusht den aktuellen Matrixstapel um eins nach unten, wodurch die aktuelle Matrix dupliziert wird. Das heißt, nach einem **glPushMatrix-Aufruf** ist die Matrix oben im Stapel identisch mit der matrix darunter. Die **glPopMatrix-Funktion** füllt den aktuellen Matrixstapel auf und ersetzt die aktuelle Matrix durch die matrix darunter auf dem Stapel. Anfänglich enthält jeder der Stapel eine Matrix, eine Identitätsmatrix.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ MATRIX \_ MODE

**glGet** mit argument GL \_ MODELVIEW \_ MATRIX

**glGet** mit argument GL \_ PROJECTION \_ MATRIX

**glGet** mit argument GL \_ TEXTURE \_ MATRIX

**glGet** mit dem Argument GL \_ MODELVIEW \_ STACK \_ DEPTH

**glGet** mit argument GL \_ PROJECTION \_ STACK \_ DEPTH

**glGet** mit argument GL \_ TEXTURE \_ STACK \_ DEPTH

**glGet** mit argument GL \_ MAX \_ MODELVIEW \_ STACK \_ DEPTH

**glGet** mit argument GL \_ MAX PROJECTION STACK \_ \_ \_ DEPTH

**glGet** mit argument GL \_ MAX TEXTURE STACK \_ \_ \_ DEPTH

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





