---
title: glMapGrid1d-Funktion (GL. h)
description: Definiert ein eindimensionales Mesh. | glMapGrid1d-Funktion (GL. h)
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
ms.openlocfilehash: 30b1900f5597e8c516100504ca7288137ed99ded
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869712"
---
# <a name="glmapgrid1d-function"></a>glMapGrid1d-Funktion

Definiert ein eindimensionales Mesh.

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

Die Anzahl der Partitionen im Raster Bereichs Intervall \[ U1, U2 \] . Dieser Wert muss positiv sein.

</dd> <dt>

*U1* 
</dt> <dd>

Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert i = 0 verwendet wird.

</dd> <dt>

*hinweg* 
</dt> <dd>

Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert i = UN verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Entweder ' *UN* ' oder ' *VN* ' war nicht positiv.<br/>                                                                                      |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Funktionen " **glmapgrid** " und " [glevalmesh](glevalmesh-functions.md) ", um eine Reihe von gleichmäßig getrennten Zuordnungs Domänen Werten effizient zu generieren und auszuwerten. Die glevalmesh-Funktion durchläuft die ganzzahlige Domäne eines ein-oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungs Zuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden.

Die **glMapGrid1** -Funktion und die [**glMapGrid2**](glmapgrid2d.md) -Funktion geben die linearen Raster Zuordnungen zwischen den ganzzahligen Raster Koordinaten i (bzw. i und j) und den Kartenkoordinaten für die Gleit Komma Auswertung von u (oder v) an. Ausführliche Informationen zur Auswertung von und v-Koordinaten finden Sie unter [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md) .

Die **glMapGrid1** *-* Funktion gibt eine einzelne lineare Zuordnung so an, dass die ganzzahlige Raster Koordinate 0 genau zu U1 zugeordnet ist, und die ganzzahlige Raster Koordinate werden genau auf *U2* Alle anderen ganzzahligen Raster Koordinaten, die *mir* zugeordnet sind:

*u = i (U2 U1)/un + U1*

Die [**glMapGrid2**](glmapgrid2d.md) -Funktion gibt zwei lineare Zuordnungen an. Eine ordnet eine ganzzahlige Raster Koordinate *i = 0* genau auf *U1* an, und die ganzzahlige Raster Koordinate *i =* ist genau auf *U2*. Der andere ordnet die ganzzahlige Raster Koordinate *j = 0* exakt auf *v1* und die ganzzahlige Raster Koordinate *j = VN* exakt auf *v2* zu. Andere ganzzahlige Raster Koordinaten i und j werden zugeordnet, damit

*u = i (U2 U1)/un + U1*

*v = j (V2 V1)/VN + v1*

Die von **glmapgrid** angegebenen Zuordnungen werden von [glevalmesh](glevalmesh-functions.md) und [**glevalpoint**](glevalpoint.md)identisch verwendet.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glmapgrid** abgerufen:

<dl>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Domäne  
[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Domäne  
[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Segmente  
[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Segmente  
</dl>

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

[**glevalcoord**](glevalcoord-functions.md)
</dt> <dt>

[glevalmesh](glevalmesh-functions.md)
</dt> <dt>

[**glevalpoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





