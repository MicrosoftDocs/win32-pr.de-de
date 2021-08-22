---
title: glLoadMatrixf-Funktion (Gl.h)
description: Die glLoadMatrixf-Funktion ersetzt die aktuelle Matrix durch eine beliebige Matrix. | glLoadMatrixf-Funktion (Gl.h)
ms.assetid: 6e1337b0-d1e7-4002-a561-d959d7f70942
keywords:
- glLoadMatrixf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3d822d784d6e24b15296a29da1c77b37b55af4211d2d9b5ce40a3c6a43c7fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492844"
---
# <a name="glloadmatrixf-function"></a>glLoadMatrixf-Funktion

Die Funktionen [**glLoadMatrixd**](glloadmatrixd.md) und **glLoadMatrixf** ersetzen die aktuelle Matrix durch eine beliebige Matrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLoadMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*m* 
</dt> <dd>

Ein Zeiger auf eine 4x4-Matrix, die in Spaltenhauptreihenfolge als 16 aufeinander folgende Werte gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glLoadMatrix-Funktion** ersetzt die aktuelle Matrix durch die in *m* angegebene Matrix. Die aktuelle Matrix ist die Projektionsmatrix, Modellansichtsmatrix oder Texturmatrix, die durch den aktuellen Matrixmodus bestimmt wird (siehe [**glMatrixMode**](glmatrixmode.md)).

Der *m-Parameter* zeigt auf eine 4x4-Matrix von Gleitkommawerten mit einfacher oder doppelter Genauigkeit, die in Spaltenhauptreihenfolge gespeichert sind. Das heißt, die Matrix wird wie in der folgenden Abbildung dargestellt gespeichert.

![Diagramm der 4x4-Matrix, auf die der m-Parameter zeigt.](images/load02.png)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glLoadMatrix** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ MATRIX \_ MODE

**glGet** mit argument GL \_ MODELVIEW \_ MATRIX

**glGet** mit argument GL \_ PROJECTION \_ MATRIX

**glGet** mit argument GL \_ TEXTURE \_ MATRIX

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





