---
title: glMultMatrixf-Funktion (Gl.h)
description: Die glMultMatrixf-Funktion multipliziert die aktuelle Matrix mit einer beliebigen Matrix. | glMultMatrixf-Funktion (Gl.h)
ms.assetid: fea5e557-09bd-4c45-89cc-9f3739b577bb
keywords:
- glMultMatrixf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ea38c08d051a2363699643f3b68ea5999fc5014c65716f974e3df6e6d83938
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128200"
---
# <a name="glmultmatrixf-function"></a>glMultMatrixf-Funktion

Die [**Funktionen glMultMatrixd**](glmultmatrixd.md) und **glMultMatrixf** multiplizieren die aktuelle Matrix mit einer beliebigen Matrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMultMatrixf(
   const GLfloat *m
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



## <a name="see-also"></a>Siehe auch

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

 

 





