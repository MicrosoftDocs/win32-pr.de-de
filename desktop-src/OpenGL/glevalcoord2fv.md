---
title: glEvalCoord2fv-Funktion (Gl.h)
description: Die glEvalCoord2fv-Funktion wertet aktivierte zweidimensionale Zuordnungen aus.
ms.assetid: fff786b4-a9e1-4f3e-a62e-36e89bc9c35d
keywords:
- glEvalCoord2fv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de18441f1b62bbd4084476dabec1cf14bd096c62ba1b26f35985208f19200b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888360"
---
# <a name="glevalcoord2fv-function"></a>glEvalCoord2fv-Funktion

Die **glEvalCoord2fv-Funktion** wertet aktivierte zweidimensionale Zuordnungen aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEvalCoord2fv(
   const GLfloat *u
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Ein Zeiger auf ein Array, das die Domänenkoordinate *u enthält.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glEvalCoord2fv-Funktion** wertet aktivierte zweidimensionale Zuordnungen mithilfe der beiden Domänenwerte *u* und *v aus.* Definieren Sie Zuordnungen [**mit glMap1.**](glmap1.md) Aktivieren oder deaktivieren Sie sie [**mit glEnable**](glenable.md) und [**glDisable**](gldisable.md).

Wenn eine der **glEvalCoord-Funktionen** ausgegeben wird, werden alle derzeit aktivierten Zuordnungen der angegebenen Dimension ausgewertet. Dann ist es für jede aktivierte Zuordnung so, als ob die entsprechende OpenGL-Funktion mit dem berechneten Wert ausgegeben würde. Das heißt, wenn GL \_ MAP1 \_ INDEX oder GL \_ MAP2 INDEX aktiviert \_ ist, wird eine [**glIndex-Funktion**](glindex-functions.md) simuliert. Wenn GL \_ MAP1 \_ COLOR \_ 4 oder GL MAP2 COLOR 4 aktiviert ist, wird eine \_ \_ \_ **glcolor-Funktion** simuliert. Wenn GL MAP1 NORMAL oder GL MAP2 NORMAL aktiviert ist, Ein normaler Vektor wird erzeugt, und wenn eine der FOLGENDEN Funktionen aktiviert ist: \_ \_ GL \_ \_ \_ MAP1 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 TEXTURE \_ \_ \_ \_ COORD 1, GL MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ \_ COORD 3 und GL \_ \_ MAP2 \_ TEXTURE \_ COORD \_ 4. [](gltexcoord-functions.md)

OpenGL verwendet ausgewertete Werte anstelle aktueller Werte für die aktivierten Auswertungen und aktuelle Werte andernfalls für Farb-, Farbindex-, Normal- und Texturkoordinaten. Die ausgewerteten Werte aktualisieren jedoch nicht die aktuellen Werte. Wenn also [**glVertex-Funktionen**](glvertex-functions.md) mit **glEvalCoord-Funktionen** interspersiert werden, werden die Farb-, Normal- und Texturkoordinaten, die den **glVertex-Funktionen** zugeordnet sind, nicht von den Werten beeinflusst, die von den **glEvalCoord-Funktionen** generiert werden, sondern nur von den neuesten [**glColor-,**](glcolor-functions.md) [**glIndex-,**](glindex-functions.md) [**glNormal-**](glnormal-functions.md)und [**glTexCoord-Funktionen.**](gltexcoord-functions.md)

Wenn die automatische normale Generierung aktiviert ist, ruft **glEvalCoord2fv** [**glEnable**](glenable.md) mit dem Argument GL AUTO NORMAL auf, um Oberflächennormals unabhängig vom Inhalt oder der Aktivierung der \_ GL \_ MAP2 NORMAL-Zuordnung analytisch zu \_ \_ generieren. Let

![Gleichung, die einen produktübergreifenden Wert für eine Karte m zeigt.](images/evlcrd01.png)

Der generierte normale **n** ist .

![Gleichung, die die generierte normale n für die Karte zeigt.](images/evlcrd02.png)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glEvalCoord2fv-Funktion** ab:

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

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP2 COLOR \_ \_ 4

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



## <a name="see-also"></a>Siehe auch

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

 

 





