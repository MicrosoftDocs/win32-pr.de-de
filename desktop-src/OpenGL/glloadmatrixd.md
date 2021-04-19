---
title: glloadmatrixd Function (GL. h)
description: Die Funktion "glloadmatrixd" ersetzt die aktuelle Matrix durch eine beliebige Matrix. | glloadmatrixd Function (GL. h)
ms.assetid: 66c499f7-3f55-4de2-b67b-5b775b5854e0
keywords:
- glloadmatrixd Function OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4715da159dff60024adb3c7331cbf03c7c3759ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353657"
---
# <a name="glloadmatrixd-function"></a>glloadmatrixd-Funktion

Die Funktionen " **glloadmatrixd** " und " [**glloadmatrixf**](glloadmatrixf.md) " ersetzen die aktuelle Matrix durch eine beliebige Matrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLoadMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*m* 
</dt> <dd>

Ein Zeiger auf eine 4 x 4-Matrix, die in Spalten Hauptreihen Folge als 16 aufeinander folgende Werte gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glloadmatrix** " ersetzt die aktuelle Matrix durch die in *m* angegebene. Die aktuelle Matrix ist die Projektions Matrix, die Modelview-Matrix oder die Textur Matrix, die durch den aktuellen Matrix Modus bestimmt wird (siehe [**glMatrixMode**](glmatrixmode.md)).

Der *m* -Parameter verweist auf eine 4 x 4-Matrix mit Gleit Komma Werten mit einfacher Genauigkeit oder Gleit Komma Werten mit doppelter Genauigkeit, die in der Spalte-Haupt Reihenfolge gespeichert sind. Das heißt, die Matrix wird wie in der folgenden Abbildung dargestellt gespeichert.

![Diagramm mit der 4 x 4-Matrix, auf die der m-Parameter zeigt.](images/load02.png)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glloadmatrix** ab:

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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





