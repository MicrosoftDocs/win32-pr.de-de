---
title: glMultMatrixd-Funktion (Gl.h)
description: Die glMultMatrixd-Funktion multipliziert die aktuelle Matrix mit einer beliebigen Matrix. | glMultMatrixd-Funktion (Gl.h)
ms.assetid: 1f6cf4e4-e7bd-470c-b1f4-b9ccc1fb756e
keywords:
- glMultMatrixd-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd31b3f84bbc8c75a3622b7b87f7a7577a33927bd489a06b8691377badaf0b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358798"
---
# <a name="glmultmatrixd-function"></a>glMultMatrixd-Funktion

Die **Funktionen glMultMatrixd** und [**glMultMatrixf**](glmultmatrixf.md) multiplizieren die aktuelle Matrix mit einer beliebigen Matrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMultMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*m* 
</dt> <dd>

Ein Zeiger auf eine 4x4-Matrix, die in Spalten-Hauptordnung als 16 aufeinander folgende Werte gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glMultMatrix-Funktion** multipliziert die aktuelle Matrix mit der in *m angegebenen* Matrix. Das heißt, wenn M die aktuelle Matrix und T die Matrix ist, die **an glMultMatrix** übergeben wird, wird M durch M T ersetzt.

Die aktuelle Matrix ist die Projektionsmatrix, Modellansichtsmatrix oder Texturmatrix, die vom aktuellen Matrixmodus bestimmt wird (siehe [**glMatrixMode**](glmatrixmode.md)).

Der *m-Parameter* zeigt auf eine 4x4-Matrix mit Gleitkommawerten mit einzelner oder doppelter Genauigkeit, die in spalten wichtiger Reihenfolge gespeichert sind. Das heißt, die Matrix wird wie in der folgenden Abbildung gezeigt gespeichert.

![! [Diagramm der 4x4-Matrix, auf die der m-Parameter zeigt.]](images/multi01.png)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glMultMatrix ab:**

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





