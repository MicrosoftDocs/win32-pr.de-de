---
title: glTranslatef-Funktion (GL. h)
description: Die glTranslatef-Funktion multipliziert die aktuelle Matrix mit einer Übersetzungs Matrix.
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- glTranslatef-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5b52c3890b70ecb931211af1788afe2b8e6ad4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869388"
---
# <a name="gltranslatef-function"></a>glTranslatef-Funktion

Die [**glTranslatef**](gltranslate.md) -Funktion multipliziert die aktuelle Matrix mit einer Übersetzungs Matrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Die *x* -Koordinate eines Übersetzungs Vektors.

</dd> <dt>

*y* 
</dt> <dd>

Die *y* -Koordinate eines Übersetzungs Vektors.

</dd> <dt>

*z* 
</dt> <dd>

Die *z* -Koordinate eines Übersetzungs Vektors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **glTranslatef** -Funktion erzeugt die durch (*x*, *y*, *z*) angegebene Übersetzung. Der Übersetzungs Vektor wird verwendet, um eine 4 x 4-Übersetzungs Matrix zu berechnen:

![Diagramm, das die durch x, y, z angegebene 4 x 4-Übersetzungs Matrix anzeigt.](images/trans01.png)

Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Übersetzungs Matrix multipliziert, und das Produkt ersetzt die aktuelle Matrix. Das heißt, wenn m die aktuelle Matrix und T die Übersetzungs Matrix ist, wird m durch m T ersetzt.

Wenn der Matrix Modus entweder eine GL \_ Modelview-oder GL- \_ Projektion ist, werden alle Objekte, die nach dem Aufruf von **glTranslatef** gezeichnet werden, übersetzt. Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix** , um das nicht übersetzte Koordinatensystem zu speichern und wiederherzustellen.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit [**glübersetzt**](gltranslate.md) und **glTranslatef** abgerufen:

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glrotation**](glrotate.md)
</dt> <dt>

[**glscale**](glscale.md)
</dt> </dl>

 

 





