---
title: glOrtho-Funktion (Gl.h)
description: Die glOrtho-Funktion multipliziert die aktuelle Matrix mit einer orthografischen Matrix.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- glOrtho-Funktion OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1e06c1740e908c34652a6d39bc7a2334763199d222ff9d1dc00ae733803ada0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795223"
---
# <a name="glortho-function"></a>glOrtho-Funktion

Die **glOrtho-Funktion** multipliziert die aktuelle Matrix mit einer orthografischen Matrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glOrtho(
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

Die Koordinaten für die linke vertikale Clippingebene.

</dd> <dt>

*Richting* 
</dt> <dd>

Die Koordinaten für die vertikale Clippingebene.

</dd> <dt>

*Unteres* 
</dt> <dd>

Die Koordinaten für die untere horizontale Ausschneideebene.

</dd> <dt>

*top* 
</dt> <dd>

Die Koordinaten für die oberen horizontalen Ausschneidepläne.

</dd> <dt>

*zNear* 
</dt> <dd>

Die Entfernungen zur näheren Abschneideebene der Tiefe. Dieser Abstand ist negativ, wenn sich die Ebene hinter dem Viewer befinden soll.

</dd> <dt>

*zFar* 
</dt> <dd>

Die Entfernungen zur weiter entfernten Tiefenabschneideebene. Dieser Abstand ist negativ, wenn sich die Ebene hinter dem Viewer befinden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glOrtho-Funktion** beschreibt eine Perspektivenmatrix, die eine parallele Projektion erzeugt. Die Parameter (*links*, *unten*, *in der Nähe*) und (*rechts*, *oben*, in *der Nähe*) geben die Punkte auf der nähen Clippingebene an, die den unteren linken bzw. oberen rechten Ecken des Fensters zugeordnet sind, vorausgesetzt, das Auge befindet sich bei (0, 0, 0). Der *far-Parameter* gibt die Position der fernen Clippingebene an. Sowohl *zNear* als *auch zFar* können entweder positiv oder negativ sein. Die entsprechende Matrix ist in der folgenden Abbildung dargestellt.

![Diagramm der perspektivenmatrix, die von der glOrtho-Funktion beschrieben wird.](images/ortho1.png)

where

![Gleichungen, die die Perspektivenmatrix beschreiben.](images/ortho2.png)

Die aktuelle Matrix wird mit dieser Matrix multipliziert, wobei das Ergebnis die aktuelle Matrix ersetzt. Das heißt, wenn M die aktuelle Matrix und O die Orthomatrix ist, wird M durch M O ersetzt.

Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix,** um den aktuellen Matrixstapel zu speichern und wiederherzustellen. Verwenden Sie [**glMatrixMode,**](glmatrixmode.md) um die aktuelle Matrix festzulegen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glOrtho** ab:

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





