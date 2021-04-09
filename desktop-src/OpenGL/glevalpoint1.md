---
title: glEvalPoint1-Funktion (GL. h)
description: Die glEvalPoint1-Funktion und die glEvalPoint2-Funktion generieren und evaluieren einen einzelnen Punkt in einem Mesh. | glEvalPoint1-Funktion (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- glEvalPoint1-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870004"
---
# <a name="glevalpoint1-function"></a>glEvalPoint1-Funktion

Die [**glEvalPoint1**](glevalpoint.md) -Funktion und die **glEvalPoint2** -Funktion generieren und evaluieren einen einzelnen Punkt in einem Mesh.

## <a name="syntax"></a>Syntax


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*i* 
</dt> <dd>

Der ganzzahlige Wert für die Raster Domänen Variable *i*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktionen [**glmapgrid**](glmapgrid-functions.md) und [**glevalmesh**](glevalmesh-functions.md) werden zusammen verwendet, um eine Reihe von Zuordnungs Domänen Werten, die gleichmäßig verteilt sind, effizient zu generieren und auszuwerten. Mithilfe von **glevalpoint** können Sie einen einzelnen Raster Punkt im gleichen Raster Bereich auswerten, der von **glevalmesh** durchlaufen wird. Das Aufrufen von [**glEvalPoint1**](glevalpoint.md) entspricht dem Aufrufen von.

**glEvalCoord1** (*i* *) u*  + 1);

where

? *u* = (*u* 2 *u* 1)/*n*

und *n*, *u* 1 und *u* 2 sind die Argumente der neuesten **glMapGrid1** -Funktion. Eine absolute numerische Anforderung besteht darin, dass bei *i*  =  *n* der Wert, der von berechnet wird (*i* ?*u* + U1) ist genau *u* 2.

Im zweidimensionalen Fall, **glEvalPoint2**, Let

? *u* = (*u* 2 *u* 1)/*n*

? *v* = (*v* 2 *v* 1)/*m*

dabei *sind n*, *u* 1, *u* 2, *m*, *v* 1 und *v* 2 die Argumente der neuesten **glMapGrid2** -Funktion. Die **glEvalPoint2** -Funktion entspricht dem Aufrufen von.

**glEvalCoord2** (*i* *) u*  +  1, *j* ?*v*  +  *v* 1);

Die einzigen absoluten numerischen Anforderungen sind, dass bei *i* = *n* der Wert, der von berechnet wird (*i* ?*u*  +  1) ist genau U2, und wenn *j*  =  *m* ist, dann wird der von (j?) berechnete Wert (*j* ?*v*  +  *v* 1) ist genau *v* 2.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glEvalPoint1**](glevalpoint.md) und **glEvalPoint2** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Domäne

**glget** mit Argument GL \_ map2 \_ Raster \_ Domäne

**glget** mit Argument GL \_ zuordnung1 \_ Raster \_ Segmente

**glget** mit Argument GL \_ map2 \_ Raster \_ Segmente

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

[**glevalcoord**](glevalcoord-functions.md)
</dt> <dt>

[**glevalmesh**](glevalmesh-functions.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glmapgrid**](glmapgrid-functions.md)
</dt> </dl>

 

 





