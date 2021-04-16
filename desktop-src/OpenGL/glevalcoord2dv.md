---
title: glEvalCoord2dv-Funktion (GL. h)
description: Die glEvalCoord2dv-Funktion wertet aktivierte zweidimensionale Zuordnungen aus.
ms.assetid: 726a0c0c-d69e-46dc-b78e-a0d1e9ad97cd
keywords:
- glEvalCoord2dv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a685606fb1445c6841efdf506a1f2d4747da838
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104558691"
---
# <a name="glevalcoord2dv-function"></a>glEvalCoord2dv-Funktion

Die **glEvalCoord2dv** -Funktion wertet aktivierte zweidimensionale Zuordnungen aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEvalCoord2dv(
   const GLdouble *u
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Ein Zeiger auf ein Array, das die Domänen Koordinate *u* enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **glEvalCoord2dv** -Funktion wertet aktivierte zweidimensionale Karten mit zwei Domänen Werten aus: *u* und *v*. Definieren von Maps mit [**glMap1**](glmap1.md). Aktivieren oder deaktivieren Sie Sie mit [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md).

Wenn eine der Funktionen von **glevalcoord** ausgegeben wird, werden alle derzeit aktivierten Zuordnungen der aufgeführten Dimension ausgewertet. Dann ist es für jede aktivierte Zuordnung so, als ob die entsprechende OpenGL-Funktion mit dem berechneten Wert ausgegeben wurde. Das heißt, wenn der GL \_ zuordnung1 \_ Index oder der GL \_ map2- \_ Index aktiviert ist, wird eine [**glindex**](glindex-functions.md) -Funktion simuliert. Wenn gl \_ zuordnung1 \_ Color \_ 4 oder GL \_ map2 \_ Color \_ 4 aktiviert ist, wird eine **glcolor** -Funktion simuliert. Wenn gl \_ zuordnung1 \_ Normal oder GL \_ map2 \_ Normal aktiviert ist, wird ein normaler Vektor erzeugt. und wenn eine von GL zuordnung1 Textur coord \_ \_ \_ \_ 1, GL \_ zuordnung1 \_ Texture \_ coord \_ 2, GL \_ zuordnung1 \_ Texture \_ coord \_ 3, GL \_ zuordnung1 \_ Texture \_ coord \_ 4, GL \_ map2 \_ Texture \_ coord \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL \_ map2 \_ Texture \_ coord \_ 3 und GL \_ map2 \_ Texture \_ coord \_ 4 aktiviert ist, wird eine entsprechende [**gltexcoord**](gltexcoord-functions.md) -Funktion simuliert.

OpenGL verwendet ausgewertete Werte anstelle der aktuellen Werte für die aktivierten Auswertungen und die aktuellen Werte für Farbe, Farbindex, normale und Texturkoordinaten. Die ausgewerteten Werte aktualisieren jedoch nicht die aktuellen Werte. Wenn daher die [**glVertex**](glvertex-functions.md) -Funktionen mit **glevalcoord** -Funktionen vermischt werden, werden die den **glVertex** -Funktionen zugeordneten Farb-, normal-und Texturkoordinaten nicht von den Werten beeinflusst, die von den Funktionen von **glevalcoord** generiert werden, sondern nur durch die neuesten Funktionen von [**glcolor**](glcolor-functions.md), [**glindex**](glindex-functions.md), [**glnormal**](glnormal-functions.md)und [**gltexcoord**](gltexcoord-functions.md) .

Wenn die automatische normale Generierung aktiviert ist, ruft **glEvalCoord2dv** [**glEnable**](glenable.md) mit dem Argument GL \_ Auto \_ Normal auf, um Oberflächen normale zu generieren, unabhängig vom Inhalt oder der Aktivierung der GL \_ map2 \_ Normal Karte. Let

![Gleichung, die einen produktübergreifenden Wert für eine Karte m anzeigt.](images/evlcrd01.png)

Die generierte normale **n** ist

![Gleichung mit dem generierten normalen n für die Karte.](images/evlcrd02.png)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glEvalCoord2dv** -Funktion ab:

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 3

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 4

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Index

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Farbe \_ 4

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Normal

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 1

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 2

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 3

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 4

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Vertex \_ 3

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Vertex \_ 4

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Index

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Farbe \_ 4

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Normal

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 1

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 2

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 3

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 4

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Auto \_ Normal

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

[**glcolor**](glcolor-functions.md)
</dt> <dt>

[**gldeaktivieren**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glevalmesh**](glevalmesh-functions.md)
</dt> <dt>

[**glevalpoint**](glevalpoint.md)
</dt> <dt>

[**glgetmap**](glgetmap.md)
</dt> <dt>

[**glindex**](glindex-functions.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glmapgrid**](glmapgrid-functions.md)
</dt> <dt>

[**glnormal**](glnormal-functions.md)
</dt> <dt>

[**gltexcoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





