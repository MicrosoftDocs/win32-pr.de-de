---
title: glRotatef-Funktion (Gl.h)
description: Die glRotatef-Funktion multipliziert die aktuelle Matrix mit einer Rotationsmatrix.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- glRotatef-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f466ca73a826d9a12f97093c90c41cd1c753b01f25853096dd3f3219628654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937930"
---
# <a name="glrotatef-function"></a>glRotatef-Funktion

Die **glRotatef-Funktion** multipliziert die aktuelle Matrix mit einer Rotationsmatrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
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

Die **glRotatef-Funktion** berechnet eine Matrix, die eine  gegen den Uhrzeigersinn erfolgende Drehung von Winkelgraden um den Vektor vom Ursprung bis zum Punkt ausführt (*x*, *y*, *z*).

Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Rotationsmatrix multipliziert, während das Produkt die aktuelle Matrix ersetzt. Das heißt, wenn M die aktuelle Matrix und R die Übersetzungsmatrix ist, wird M durch M R ersetzt.

Wenn der Matrixmodus GL MODELVIEW oder GL PROJECTION ist, werden alle Objekte gedreht, die nach dem Aufgerufenen \_ \_ von **glRotatef** gezeichnet werden. Verwenden [**Sie glPushMatrix**](glpushmatrix.md) und [**glPopMatrix,**](glpopmatrix.md) um das nichtrotierte Koordinatensystem zu speichern und wiederherzustellen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glRotatef ab:**

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



## <a name="see-also"></a>Weitere Informationen

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

 

 





