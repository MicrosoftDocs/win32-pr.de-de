---
title: glRotated-Funktion (Gl.h)
description: Die glRotated-Funktion multipliziert die aktuelle Matrix mit einer Rotationsmatrix.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- glRotated-Funktion OpenGL
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
ms.openlocfilehash: 32216eab9a7c7613f082470360d3f938bbdeaf8ae38cd875d84cd0338dfa78c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491770"
---
# <a name="glrotated-function"></a>glRotated-Funktion

Die **glRotated-Funktion** multipliziert die aktuelle Matrix mit einer Rotationsmatrix.

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

Die *x-Koordinate* eines Vektors.

</dd> <dt>

*y* 
</dt> <dd>

Die *y-Koordinate* eines Vektors.

</dd> <dt>

*Z* 
</dt> <dd>

Die *z-Koordinate* eines Vektors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glRotated-Funktion** berechnet eine Matrix, die eine  gegen den Uhrzeigersinn erfolgende Drehung von Winkelgraden um den Vektor vom Ursprung bis zum Punkt ausführt (*x*, *y*, *z*).

Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Rotationsmatrix multipliziert, während das Produkt die aktuelle Matrix ersetzt. Das heißt, wenn M die aktuelle Matrix und R die Übersetzungsmatrix ist, wird M durch M R ersetzt.

Wenn der Matrixmodus entweder GL MODELVIEW oder GL PROJECTION ist, werden alle Objekte gedreht, die nach dem Aufgerufenen \_ \_ von **glRotated** gezeichnet wurden. Verwenden [**Sie glPushMatrix**](glpushmatrix.md) und [**glPopMatrix,**](glpopmatrix.md) um das nichtrotierte Koordinatensystem zu speichern und wiederherzustellen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glRotated ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ RENDER \_ MODE

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MATRIX \_ MODE

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MODELVIEW \_ MATRIX

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ PROJECTION \_ MATRIX

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ TEXTURE \_ MATRIX

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





