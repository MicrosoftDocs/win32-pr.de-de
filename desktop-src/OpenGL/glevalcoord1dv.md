---
title: glEvalCoord1dv-Funktion (Gl.h)
description: Die glEvalCoord1dv-Funktion wertet aktivierte eindimensionale Zuordnungen aus.
ms.assetid: 6f966141-d4e6-4b54-b465-3ced33b57caf
keywords:
- glEvalCoord1dv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9611a43b5f17eb5c5ac3d520f13ab3fb34fc516b850c37943c1ad75478db1527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616237"
---
# <a name="glevalcoord1dv-function"></a>glEvalCoord1dv-Funktion

Die [**glEvalCoord1dv-Funktion**](glevalcoord1d.md) wertet aktivierte eindimensionale Zuordnungen aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEvalCoord1dv(
   const GLdouble *u
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Ein Zeiger auf ein Array, das die Domänenkoordinate *u* enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glEvalCoord1dv-Funktion** wertet aktivierte eindimensionale Zuordnungen am Argument *u* aus. Definieren Sie Zuordnungen mit [**glMap1.**](glmap1.md) Aktivieren oder deaktivieren Sie sie mit [**glEnable**](glenable.md) und [**glDisable**](gldisable.md).

Wenn eine der **glEvalCoord-Funktionen** ausgegeben wird, werden alle derzeit aktivierten Zuordnungen der angegebenen Dimension ausgewertet. Dann ist es für jede aktivierte Zuordnung so, als ob die entsprechende OpenGL-Funktion mit dem berechneten Wert ausgegeben worden wäre. Das heißt, wenn GL \_ MAP1 \_ INDEX oder GL \_ MAP2 INDEX aktiviert \_ ist, wird eine [**glIndex-Funktion**](glindex-functions.md) simuliert. Wenn GL \_ MAP1 \_ COLOR \_ 4 oder GL \_ MAP2 \_ COLOR \_ 4 aktiviert ist, wird eine **glcolor-Funktion** simuliert. Wenn GL \_ MAP1 \_ NORMAL oder GL \_ MAP2 NORMAL aktiviert \_ ist, Ein normaler Vektor wird erstellt, und wenn einer der GL \_ MAP1 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 3 und GL \_ MAP2 TEXTURE \_ \_ COORD \_ 4 aktiviert ist, wird eine entsprechende [**glTexCoord-Funktion**](gltexcoord-functions.md) simuliert.

OpenGL verwendet ausgewertete Werte anstelle der aktuellen Werte für die aktivierten Auswertungen, und aktuelle Werte andernfalls für Farb-, Farbindex-, Normal- und Texturkoordinaten. Die ausgewerteten Werte aktualisieren die aktuellen Werte jedoch nicht. Wenn [**glVertex-Funktionen**](glvertex-functions.md) also mit **glEvalCoord-Funktionen** durchsetzt werden, werden die den **glVertex-Funktionen** zugeordneten Farb-, Normal- und Texturkoordinaten nicht von den Werten beeinflusst, die von den **glEvalCoord-Funktionen** generiert werden, sondern nur von den neuesten [**glColor-,**](glcolor-functions.md) [**glIndex-,**](glindex-functions.md) [**glNormal-**](glnormal-functions.md)und [**glTexCoord-Funktionen.**](gltexcoord-functions.md)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glEvalCoord1dv-Funktion** ab:

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP1 \_ VERTEX \_ 3

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP1 \_ VERTEX \_ 4

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP1 \_ INDEX

[**glIsEnabled**](glisenabled.md) mit argument GL \_ MAP1 \_ COLOR \_ 4

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP1 \_ NORMAL

[**glIsEnabled**](glisenabled.md) mit argument GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled**](glisenabled.md) mit argument GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled**](glisenabled.md) mit argument GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP2 \_ VERTEX \_ 3

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP2 \_ VERTEX \_ 4

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP2 \_ INDEX

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP2 \_ COLOR \_ 4

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP2 \_ NORMAL

[**glIsEnabled**](glisenabled.md) mit argument GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled**](glisenabled.md) mit argument GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled**](glisenabled.md) mit argument GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled**](glisenabled.md) mit argument GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled**](glisenabled.md) mit argument GL \_ AUTO \_ NORMAL

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





