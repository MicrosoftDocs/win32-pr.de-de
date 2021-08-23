---
title: glFrustum-Funktion (Gl.h)
description: Die glFrustum-Funktion multipliziert die aktuelle Matrix mit einer Perspektivenmatrix.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- glFrustum-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1ca2375206165576405c96528d0590596f4d4d870121f0a30884c8e448ca93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625255"
---
# <a name="glfrustum-function"></a>glFrustum-Funktion

Die **glFrustum-Funktion** multipliziert die aktuelle Matrix mit einer Perspektivenmatrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Links* 
</dt> <dd>

Die Koordinate für die linke vertikale Clippingebene.

</dd> <dt>

*Richting* 
</dt> <dd>

Die Koordinate für die rechte vertikale Clippingebene.

</dd> <dt>

*Unteres* 
</dt> <dd>

Die Koordinate für die untere horizontale Ausschneideebene.

</dd> <dt>

*top* 
</dt> <dd>

Die Koordinate für die untere horizontale Ausschneideebene.

</dd> <dt>

*zNear* 
</dt> <dd>

Die Entfernungen zur Clippingebene mit nahezuer Tiefe. Muss positiv sein.

</dd> <dt>

*zFar* 
</dt> <dd>

Die Entfernungen zu den Abschneideebenen mit weiter Tiefe. Muss positiv sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *zNear* oder *zFar* war nicht postitive.<br/>                                                                                       |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glFrustum-Funktion** beschreibt eine Perspektivenmatrix, die eine perspektivische Projektion erzeugt. Die Parameter (*left*, *bottom*, *zNear*) und (*right*, *top*, *zNear*) geben die Punkte auf der mittleren Clippingebene an, die den unteren linken bzw. oberen rechten Ecken des Fensters zugeordnet sind, vorausgesetzt, das Auge befindet sich bei (0,0,0). Der *zFar-Parameter* gibt die Position der fernen Clippingebene an. Sowohl *zNear* als *auch zFar* müssen positiv sein. Die entsprechende Matrix ist in der folgenden Abbildung dargestellt.

![Diagramm der Perspektivmatrix, die eine Perspektivenprojektion erzeugt](images/frust01.png)![Gleichungen, die die glFrustum-Funktion zeigen, die eine Perspektivenmatrix beschreibt.](images/frust02.png)

Die **glFrustum-Funktion** multipliziert die aktuelle Matrix mit dieser Matrix, wobei das Ergebnis die aktuelle Matrix ersetzt. Das heißt, wenn M die aktuelle Matrix und F die Frustumperspektivenmatrix ist, ersetzt **glFrustum** M durch M F.

Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und [**glPopMatrix,**](glpopmatrix.md) um den aktuellen Matrixstapel zu speichern und wiederherzustellen.

Die Genauigkeit des Tiefenpuffers wird durch die für *zNear* und *zFar* angegebenen Werte beeinflusst. Je größer das Verhältnis von *zFar* zu *zNear* ist, desto weniger effektiv unterscheidet der Tiefenpuffer zwischen Oberflächen, die sich nahe beieinander befinden. If

![Gleichung, die das Verhältnis von "far" zu "near" zeigt.](images/frust03.png)

Ungefähr *protokollieren* 2 (*r*) Bits der Genauigkeit des Tiefenpuffers gehen verloren. Da *sich r* unendlich nähert, wenn *zNear* 0 (null) nähert, sollten Sie *zNear* nie auf 0 (null) festlegen.

Die folgenden Funktionen rufen Informationen zu **glFrustum** ab:

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





