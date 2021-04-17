---
title: glrorofunktion (GL. h)
description: Die Funktion "glrotiert" multipliziert die aktuelle Matrix mit einer Rotations Matrix.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- glgedreht-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d0678e9da6f0b68047708f45fda1c9da66d8139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519031"
---
# <a name="glrotated-function"></a>glrorofunktion

Die Funktion " **glrotiert** " multipliziert die aktuelle Matrix mit einer Rotations Matrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*angle* 
</dt> <dd>

Der Drehwinkel in Grad.

</dd> <dt>

*x* 
</dt> <dd>

Die *x* -Koordinate eines Vektors.

</dd> <dt>

*y* 
</dt> <dd>

Die *y* -Koordinate eines Vektors.

</dd> <dt>

*z* 
</dt> <dd>

Die *z* -Koordinate eines Vektors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glrotiert** " berechnet eine Matrix, die eine Drehung gegen den Uhrzeigersinn in *Winkel* Graden um den Vektor vom Ursprung bis zum Punkt (*x*, *y*, *z*) ausführt.

Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Rotations Matrix multipliziert, und das Produkt ersetzt die aktuelle Matrix. Das heißt, wenn m die aktuelle Matrix und R die Übersetzungs Matrix ist, wird m durch m r ersetzt.

Wenn der Matrix Modus entweder eine GL \_ Modelview-oder GL- \_ Projektion ist, werden alle Objekte, die nach dem Aufruf von **glrotiert** gezeichnet werden, gedreht. Verwenden Sie zum Speichern und Wiederherstellen des ungedrehten Koordinatensystems [**glPushMatrix**](glpushmatrix.md) und [**glPopMatrix**](glpopmatrix.md) .

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glrotiert** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Rendermodus

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Modelview \_ Matrix

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Projektions \_ Matrix

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Textur \_ Matrix

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glscale**](glscale.md)
</dt> <dt>

[**gltranslate**](gltranslate.md)
</dt> </dl>

 

 





