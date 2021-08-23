---
title: glTranslatef-Funktion (Gl.h)
description: Die glTranslatef-Funktion multipliziert die aktuelle Matrix mit einer Übersetzungsmatrix.
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
ms.openlocfilehash: 12975095aa78d143aaaf096e8b0141f37d45a56286e7d607a9253e59e27ba5bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489844"
---
# <a name="gltranslatef-function"></a>glTranslatef-Funktion

Die [**glTranslatef-Funktion**](gltranslate.md) multipliziert die aktuelle Matrix mit einer Übersetzungsmatrix.

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

Die  x-Koordinate eines Übersetzungsvektors.

</dd> <dt>

*y* 
</dt> <dd>

Die  y-Koordinate eines Übersetzungsvektors.

</dd> <dt>

*z* 
</dt> <dd>

Die  z-Koordinate eines Übersetzungsvektors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glTranslatef-Funktion** erzeugt die von angegebene Übersetzung (*x*, *y*, *z*). Der Übersetzungsvektor wird verwendet, um eine 4x4-Übersetzungsmatrix zu berechnen:

![Diagramm der 4x4-Übersetzungsmatrix, angegeben durch x, y, z.](images/trans01.png)

Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Übersetzungsmatrix multipliziert, wobei das Produkt die aktuelle Matrix ersetzt. Das heißt, wenn M die aktuelle Matrix und T die Übersetzungsmatrix ist, wird M durch M T ersetzt.

Wenn der Matrixmodus entweder GL \_ MODELVIEW oder GL PROJECTION ist, werden alle Objekte übersetzt, die nach dem Aufruf von \_ **glTranslatef** gezeichnet wurden. Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix,** um das nicht übersetzte Koordinatensystem zu speichern und wiederherzustellen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glTranslated**](gltranslate.md) und **glTranslatef ab:**

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

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> </dl>

 

 





