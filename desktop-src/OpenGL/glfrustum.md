---
title: glfrustum-Funktion (GL. h)
description: Die glfrustum-Funktion multipliziert die aktuelle Matrix mit einer perspektivischen Matrix.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- glfrustum-Funktion OpenGL
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
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104566703"
---
# <a name="glfrustum-function"></a>glfrustum-Funktion

Die **glfrustum** -Funktion multipliziert die aktuelle Matrix mit einer perspektivischen Matrix.

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

*linken* 
</dt> <dd>

Die Koordinate für die linke vertikale Clippingebene.

</dd> <dt>

*Richting* 
</dt> <dd>

Die Koordinate für die Rechte vertikale Clippingebene.

</dd> <dt>

*unten* 
</dt> <dd>

Die Koordinate für die untere horizontale Clippingebene.

</dd> <dt>

*top* 
</dt> <dd>

Die Koordinate für die untere horizontale Clippingebene.

</dd> <dt>

*znear* 
</dt> <dd>

Die Abstände zur fast tiefen Clippingebene. Muss positiv sein.

</dd> <dt>

*zfar* 
</dt> <dd>

Die Entfernungen zu den äußersten Ausschneide Flächen. Muss positiv sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *znear* oder *zfar* war nicht Positionen.<br/>                                                                                       |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glfrustum** -Funktion beschreibt eine Perspektiven Matrix, die eine perspektivische Projektion erzeugt. Mit den Parametern (*left*, *Bottom*, *znear*) und (*right*, *Top*, *znear*) werden die Punkte auf der Near Clipping-Ebene angegeben, die der unteren linken und oberen rechten Ecke des Fensters zugeordnet sind, vorausgesetzt, das Auge befindet sich bei (0,0). Der *zfar* -Parameter gibt den Speicherort der weit entfernten Clippingebene an. *Znear* und *zfar* müssen positiv sein. Die entsprechende Matrix ist in der folgenden Abbildung dargestellt.

![Diagramm mit der Perspektiven Matrix, die eine perspektivische Projektion erzeugt.](images/frust01.png)![Gleichungen, die die glfrustum-Funktion zeigen, die eine Perspektiven Matrix beschreibt.](images/frust02.png)

Die **glfrustum** -Funktion multipliziert die aktuelle Matrix mit dieser Matrix, wobei die aktuelle Matrix durch das Ergebnis ersetzt wird. Das heißt, wenn m die aktuelle Matrix und F die Frustum-perspektivische Matrix ist, ersetzt **glfrustum** m durch m F.

Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und [**glPopMatrix**](glpopmatrix.md) , um den aktuellen Matrix Stapel zu speichern und wiederherzustellen.

Die Genauigkeit des tiefen Puffers wird von den für *znear* und *zfar* angegebenen Werten beeinflusst. Je größer das Verhältnis von *zfar* zu *znear* ist, desto weniger effektiv ist der tiefen Puffer, um zwischen Oberflächen zu unterscheiden, die sich nahe beieinander befinden. Wenn

![Gleichung, die das Verhältnis von "weit zu nah" anzeigt.](images/frust03.png)

ungefähr alle *Log* 2 (*r*)-Bits der tiefen Puffer Genauigkeit gehen verloren. Da *r* unendlich ist, wenn *znear* den Wert 0 (null) erreicht, sollten Sie *znear* nie auf NULL festlegen.

Mit den folgenden Funktionen werden Informationen zu **glfrustum** abgerufen:

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

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**glortho**](glortho.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





