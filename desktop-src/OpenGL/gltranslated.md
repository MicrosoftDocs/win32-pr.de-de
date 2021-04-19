---
title: glsetzte-Funktion (GL. h)
description: Die gltranslation-Funktion multipliziert die aktuelle Matrix mit einer Übersetzungs Matrix.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- glsetzenfunktion OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106373412"
---
# <a name="gltranslated-function"></a>glsetzte-Funktion

Die **gltranslation** -Funktion multipliziert die aktuelle Matrix mit einer Übersetzungs Matrix.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
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

Die **gltranslation** -Funktion erzeugt die durch angegebene Übersetzung (*x*, *y*, *z*). Der Übersetzungs Vektor wird verwendet, um eine 4 x 4-Übersetzungs Matrix zu berechnen:

![Diagramm, das die durch x, y, z angegebene 4 x 4-Übersetzungs Matrix anzeigt.](images/trans01.png)

Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Übersetzungs Matrix multipliziert, und das Produkt ersetzt die aktuelle Matrix. Das heißt, wenn m die aktuelle Matrix und T die Übersetzungs Matrix ist, wird m durch m T ersetzt.

Wenn der Matrix Modus entweder eine GL \_ Modelview-oder GL- \_ Projektion ist, werden alle Objekte, die nach dem Aufruf von **glübersetzt** gezeichnet werden, übersetzt. Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix** , um das nicht übersetzte Koordinatensystem zu speichern und wiederherzustellen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glübersetzt**](gltranslate.md)ab:

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

 

 





