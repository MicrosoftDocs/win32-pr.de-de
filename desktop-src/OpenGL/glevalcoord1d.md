---
title: glEvalCoord1d-Funktion (Gl.h)
description: Die glEvalCoord1d-Funktion wertet aktivierte eindimensionale Karten aus.
ms.assetid: 5e884f11-fb3f-4158-8041-6c71509bf7d5
keywords:
- glEvalCoord1d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54926b6a1a4f09f34034820b576e457a7484f6a3e053607e5a3eed44edbdd110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616227"
---
# <a name="glevalcoord1d-function"></a>glEvalCoord1d-Funktion

Die **glEvalCoord1d-Funktion wertet** aktivierte eindimensionale Karten aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEvalCoord1d(
   GLdouble u
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Ein -Wert, der die Domänenkoordinate *u* für die Basisfunktion ist, die in einer vorherigen [**glMap1-Funktion definiert**](glmap1.md) wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glEvalCoord1d-Funktion wertet** aktivierte eindimensionale Zuordnungen beim Argument *u aus.* Definieren Sie Zuordnungen [**mit glMap1.**](glmap1.md) Aktivieren oder deaktivieren Sie sie [**mit glEnable**](glenable.md) und [**glDisable**](gldisable.md).

Wenn eine der **glEvalCoord-Funktionen** ausgegeben wird, werden alle derzeit aktivierten Zuordnungen der angegebenen Dimension ausgewertet. Dann ist es für jede aktivierte Zuordnung so, als ob die entsprechende OpenGL-Funktion mit dem berechneten Wert ausgegeben würde. Das heißt, wenn GL \_ MAP1 \_ INDEX oder GL \_ MAP2 INDEX aktiviert \_ ist, wird eine [**glIndex-Funktion**](glindex-functions.md) simuliert. Wenn GL \_ MAP1 \_ COLOR \_ 4 oder GL MAP2 COLOR 4 aktiviert ist, wird eine \_ \_ \_ **glcolor-Funktion** simuliert. Wenn GL MAP1 NORMAL oder GL MAP2 NORMAL aktiviert ist, Ein normaler Vektor wird erzeugt, und wenn eine der FOLGENDEN Funktionen aktiviert ist: \_ \_ GL \_ \_ \_ MAP1 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 TEXTURE \_ \_ \_ \_ COORD 1, GL MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ \_ COORD 3 und GL \_ \_ MAP2 \_ TEXTURE \_ COORD \_ 4. [](gltexcoord-functions.md)

OpenGL verwendet ausgewertete Werte anstelle aktueller Werte für die aktivierten Auswertungen und aktuelle Werte andernfalls für Farb-, Farbindex-, Normal- und Texturkoordinaten. Die ausgewerteten Werte aktualisieren jedoch nicht die aktuellen Werte. Wenn also [**glVertex-Funktionen**](glvertex-functions.md) mit **glEvalCoord-Funktionen** interspersiert werden, werden die Farb-, Normal- und Texturkoordinaten, die den **glVertex-Funktionen** zugeordnet sind, nicht von den Werten beeinflusst, die von den **glEvalCoord-Funktionen** generiert werden, sondern nur von den neuesten [**glColor-,**](glcolor-functions.md) [**glIndex-,**](glindex-functions.md) [**glNormal-**](glnormal-functions.md)und [**glTexCoord-Funktionen.**](gltexcoord-functions.md)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glEvalCoord1d-Funktion** ab:

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP1 \_ VERTEX \_ 3

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP1 \_ VERTEX \_ 4

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ MAP1 \_ INDEX

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP1 COLOR \_ \_ 4

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP1 \_ NORMAL

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP1 TEXTURE \_ \_ COORD \_ 1

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP1 TEXTURE \_ \_ COORD \_ 3

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP1 TEXTURE \_ \_ COORD \_ 4

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP2 \_ VERTEX \_ 3

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ MAP2 \_ VERTEX \_ 4

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ MAP2 \_ INDEX

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ MAP2 \_ COLOR \_ 4

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP2 \_ NORMAL

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP2 TEXTURE \_ \_ COORD \_ 3

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP2 TEXTURE \_ \_ COORD \_ 4

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ AUTO \_ NORMAL

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

 

 





