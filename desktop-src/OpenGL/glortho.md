---
title: glortho-Funktion (GL. h)
description: Die glortho-Funktion multipliziert die aktuelle Matrix mit einer orthografischen Matrix.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- glortho-Funktion OpenGL
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
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104560255"
---
# <a name="glortho-function"></a>glortho-Funktion

Die **glortho** -Funktion multipliziert die aktuelle Matrix mit einer orthografischen Matrix.

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

*linken* 
</dt> <dd>

Die Koordinaten für die linke vertikale Clippingebene.

</dd> <dt>

*Richting* 
</dt> <dd>

Die Koordinaten für die vertikale Clippingebene.

</dd> <dt>

*unten* 
</dt> <dd>

Die Koordinaten für die untere horizontale Clippingebene.

</dd> <dt>

*top* 
</dt> <dd>

Die Koordinaten für die oberen horizontalen clippingpläne.

</dd> <dt>

*znear* 
</dt> <dd>

Die Abstände zur näheren Ausschneide Ebene. Diese Distanz ist negativ, wenn sich die Ebene hinter dem Viewer befinden soll.

</dd> <dt>

*zfar* 
</dt> <dd>

Die Abstände zur weiteren tiefen Clippingebene. Diese Distanz ist negativ, wenn sich die Ebene hinter dem Viewer befinden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glortho** -Funktion beschreibt eine perspektivische Matrix, die eine parallele Projektion erzeugt. Mit den Parametern (*left*, *Bottom*, *near*) und (*right*, *Top*, *near*) werden die Punkte auf der Near Clipping-Ebene angegeben, die der unteren linken und oberen rechten Ecke des Fensters zugeordnet sind, vorausgesetzt, das Auge befindet sich bei (0, 0,0). Der *Far* -Parameter gibt den Speicherort der weit entfernten Clippingebene an. *Znear* und *zfar* können entweder positiv oder negativ sein. Die entsprechende Matrix ist in der folgenden Abbildung dargestellt.

![Diagramm mit der Perspektiven Matrix, die von der Funktion "glortho" beschrieben wird.](images/ortho1.png)

where

![Gleichungen, die die Perspektiven Matrix beschreiben.](images/ortho2.png)

Die aktuelle Matrix wird mit dieser Matrix multipliziert, wobei die aktuelle Matrix durch das Ergebnis ersetzt wird. Das heißt, wenn m die aktuelle Matrix und O die Ortho-Matrix ist, wird m durch m o ersetzt.

Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix** , um den aktuellen Matrix Stapel zu speichern und wiederherzustellen. Verwenden Sie [**glMatrixMode**](glmatrixmode.md) , um die aktuelle Matrix festzulegen.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glortho** abgerufen:

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

[**glfrustum**](glfrustum.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





