---
title: glMapGrid2f-Funktion (Gl.h)
description: Definiert ein eindimensionales Gitternetz. | glMapGrid2f-Funktion (Gl.h)
ms.assetid: f9bc2b0c-dec5-4762-8c99-46546a81893e
keywords:
- glMapGrid2f-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37975e7ca88f829286872b5352ff3e59d84fd4d123d457defb01b6d14003dad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358937"
---
# <a name="glmapgrid2f-function"></a>glMapGrid2f-Funktion

Definiert ein eindimensionales Gitternetz.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMapGrid2f(
   GLint   un,
   GLfloat u1,
   GLfloat u2,
   GLint   vn,
   GLfloat v1,
   GLfloat v2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*un* 
</dt> <dd>

Die Anzahl der Partitionen im Rasterbereichsintervall \[ u1, u2 \] . Dieser Wert muss positiv sein.

</dd> <dt>

*u1* 
</dt> <dd>

Ein -Wert, der als Zuordnung für den Domänenwert des ganzzahligen Rasters i = 0 verwendet wird.

</dd> <dt>

*u2* 
</dt> <dd>

Ein -Wert, der als Zuordnung für den Domänenwert des ganzzahligen Rasters i = un verwendet wird.

</dd> <dt>

*vn* 
</dt> <dd>

Die Anzahl der Partitionen im Rasterbereichsintervall \[ v1, \] v2.

</dd> <dt>

*v1* 
</dt> <dd>

Ein -Wert, der als Zuordnung für den Ganzzahlrasterdomänenwert j = 0 verwendet wird.

</dd> <dt>

*v2* 
</dt> <dd>

Ein -Wert, der als Zuordnung für den Domänenwert des ganzzahligen Rasters j = vn verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Entweder *un* oder *vn* war nicht positiv.<br/>                                                                                      |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die Funktionen **glMapGrid** und [glEvalMesh](glevalmesh-functions.md) werden zusammen verwendet, um eine Reihe von gleichmäßigen Zuordnungsdomänenwerten effizient zu generieren und auszuwerten. Die glEvalMesh-Funktion durchgehen die ganzzahlige Domäne eines ein- oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungszuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden.

Die Funktionen [**glMapGrid1**](glmapgrid1d.md) und [**glMapGrid2**](glmapgrid2d.md) geben die linearen Rasterzuordnungen zwischen den ganzzahligen Rasterkoordinaten i (oder i und j) für die u-Koordinaten (oder Sie und v) der Gleitkommaauswertungskarte an. Unter [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md) finden Sie Details dazu, wie Sie und v-Koordinaten ausgewertet werden.

Die [**glMapGrid1-Funktion**](glmapgrid1d.md) gibt eine einzelne lineare Zuordnung an, sodass die ganzzahlige Rasterkoordinate 0 genau u1 und die ganzzahlige Rasterkoordinate genau *u2* entspricht.  Alle anderen Ganzzahlrasterkoordinaten *i* werden so zugeordnet, dass:

*u = i(u2 u1)/un + u1*

Die [**glMapGrid2-Funktion**](glmapgrid2d.md) gibt zwei solcher linearen Zuordnungen an. Eine ordnet die ganzzahlige Rasterkoordinate *i = 0* genau zu *u1* und die ganzzahlige Rasterkoordinate *i = un* genau zu *u2* zu. Die andere ordnet die ganzzahlige Rasterkoordinate *j = 0* genau zu *v1* und die ganzzahlige Rasterkoordinate *j = vn* genau zu *v2* zu. Andere ganzzahlige Rasterkoordinaten i und j werden so zugeordnet, dass

*u = i(u2 u1)/un + u1*

*v = j (v2 v1)/vn + v1*

Die von [**glMapGrid**](glmapgrid1d.md) angegebenen Zuordnungen werden von [glEvalMesh](glevalmesh-functions.md) und [**glEvalPoint**](glevalpoint.md)identisch verwendet.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glMapGrid**](glmapgrid1d.md)ab:

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ MAP1 \_ GRID \_ DOMAIN  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ MAP2 \_ GRID \_ DOMAIN  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ MAP1 \_ GRID \_ SEGMENTS  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ MAP2 \_ GRID \_ SEGMENTS  
</dl>

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[glEvalMesh](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





