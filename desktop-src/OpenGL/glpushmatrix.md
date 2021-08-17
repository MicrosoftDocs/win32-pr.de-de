---
title: glPushMatrix-Funktion (Gl.h)
description: Die Funktionen glPushMatrix und glPopMatrix pushen und popen den aktuellen Matrixstapel. | glPushMatrix-Funktion (Gl.h)
ms.assetid: 97d8e644-50bb-4130-b6b7-d87df4468e73
keywords:
- glPushMatrix-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPushMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0d6af41bb02c82a28b667a2b5ad62d942c036c7f744a68fa9bb79188e26ae8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795135"
---
# <a name="glpushmatrix-function"></a>glPushMatrix-Funktion

Die **Funktionen glPushMatrix** und [**glPopMatrix**](glpopmatrix.md) pushen und popen den aktuellen Matrixstapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPushMatrix(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Es ist ein Fehler, einen vollständigen Matrixstapel zu pushen oder einen Matrixstapel zu popen, der nur eine einzelne Matrix enthält. In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | Die Funktion wurde aufgerufen, während der aktuelle Matrixstapel voll war.<br/>                                                           |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Für jeden Matrixmodus gibt es einen Stapel von Matrizen. Im GL \_ MODELVIEW-Modus beträgt die Stapeltiefe mindestens 32. In den anderen beiden Modi GL PROJECTION und GL TEXTURE beträgt die Tiefe \_ mindestens \_ 2. Die aktuelle Matrix in einem beliebigen Modus ist die Matrix am Anfang des Stapels für diesen Modus.

Die **glPushMatrix-Funktion** pusht den aktuellen Matrixstapel um eins nach unten und dupliziert die aktuelle Matrix. Das heißt, nach einem **glPushMatrix-Aufruf** ist die Matrix oben im Stapel mit der darunter stehenden Matrix identisch. Die **glPopMatrix-Funktion** popt den aktuellen Matrixstapel und ersetzt die aktuelle Matrix durch die untere Matrix auf dem Stapel. Anfänglich enthält jeder der Stapel eine Matrix, eine Identitätsmatrix.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPushMatrix** und **glPopMatrix ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MATRIX \_ MODE

**glGet** mit Argument GL \_ MODELVIEW \_ MATRIX

**glGet** mit Argument GL \_ PROJECTION \_ MATRIX

**glGet** mit Argument GL \_ TEXTURE \_ MATRIX

**glGet mit** Argument GL \_ MODELVIEW \_ STACK \_ DEPTH

**glGet mit** argument GL \_ PROJECTION STACK \_ \_ DEPTH

**glGet mit** Argument GL \_ TEXTURE STACK \_ \_ DEPTH

**glGet** mit argument GL \_ MAX \_ MODELVIEW \_ STACK \_ DEPTH

**glGet mit** argument GL \_ MAX PROJECTION STACK \_ \_ \_ DEPTH

**glGet** mit argument GL \_ MAX TEXTURE STACK \_ \_ \_ DEPTH

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

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





