---
title: glMapGrid1d-Funktion (Gl.h)
description: Definiert ein eindimensionales Gitter. | glMapGrid1d-Funktion (Gl.h)
ms.assetid: a0bc822e-dd98-4586-a322-2779e11f38ca
keywords:
- glMapGrid1d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71fcf2ac8871ab1008a5f0e31c6264383cc790edaebd3decc29dbc2ca39845fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128260"
---
# <a name="glmapgrid1d-function"></a>glMapGrid1d-Funktion

Definiert ein eindimensionales Gitter.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMapGrid1d(
   GLint    un,
   GLdouble u1,
   GLdouble u2
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

Ein -Wert, der als Zuordnung für den ganzzahligen Rasterdomänenwert i = 0 verwendet wird.

</dd> <dt>

*u2* 
</dt> <dd>

Ein -Wert, der als Zuordnung für den ganzzahligen Rasterdomänenwert i = un verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Entweder *un* oder *vn* war nicht positiv.<br/>                                                                                      |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Verwenden Sie **die Funktionen glMapGrid** und [glEvalMesh](glevalmesh-functions.md) zusammen, um eine Reihe von Domänenwerten mit gleichmäßigen Leerzeichen effizient zu generieren und zu bewerten. Die funktion glEvalMesh durchgibt die ganzzahlige Domäne eines ein- oder zweidimensionalen Rasters, dessen Bereich der Domäne der auswertungszuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2 angegeben werden.**](glmap2.md)

Die **Funktionen glMapGrid1** und [**glMapGrid2**](glmapgrid2d.md) geben die linearen Rasterzuordnungen zwischen den Koordinaten der ganzzahligen Rasterkoordinaten i (oder i und j) zu den Koordinaten der Gleitkommaauswertungskarte u (oder Sie und v) an. Unter [**glMap1 und**](glmap1.md) [**glMap2 finden**](glmap2.md) Sie Details dazu, wie Sie und V-Koordinaten ausgewertet werden.

Die **glMapGrid1-Funktion** gibt eine einzelne lineare Zuordnung an, damit die ganzzahlige Rasterkoordinate 0 genau u1 und die ganzzahlige Rasterkoordinate *un* genau *u2 zuteil wird.* Alle anderen ganzzahligen *Rasterkoordinaten i* werden so zugeordnet, dass:

*u = i(u2 u1)/un + u1*

Die [**glMapGrid2-Funktion**](glmapgrid2d.md) gibt zwei solche linearen Zuordnungen an. Eine ordnet die ganzzahlige *Rasterkoordinate i = 0* genau *u1* zu, und die ganzzahlige Rasterkoordinate *i = un genau* zu *u2.* Die andere ordnet die ganzzahlige Rasterkoordinate *j = 0* genau *zu v1* und die ganzzahlige Rasterkoordinate *j = vn* genau *zu v2 zu.* Andere ganzzahlige Rasterkoordinaten i und j werden so zugeordnet, dass

*u = i(u2 u1)/un + u1*

*v = j (v2 v1)/vn + v1*

Die von **glMapGrid angegebenen Zuordnungen** werden von [glEvalMesh](glevalmesh-functions.md) und [**glEvalPoint identisch verwendet.**](glevalpoint.md)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glMapGrid ab:**

<dl>

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ MAP1 \_ GRID \_ DOMAIN  
[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ MAP2 \_ GRID \_ DOMAIN  
[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) dem Argument GL \_ MAP1 \_ GRID \_ SEGMENTS  
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



## <a name="see-also"></a>Siehe auch

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

 

 





