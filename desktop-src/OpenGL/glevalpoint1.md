---
title: glEvalPoint1-Funktion (Gl.h)
description: Die Funktionen glEvalPoint1 und glEvalPoint2 generieren und werten einen einzelnen Punkt in einem Gitternetz aus. | glEvalPoint1-Funktion (Gl.h)
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
ms.openlocfilehash: db152c34f9ff3a9b5ad0d157507750302c73f066b32d289cadec4f117485dbe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081490"
---
# <a name="glevalpoint1-function"></a>glEvalPoint1-Funktion

Die [**Funktionen glEvalPoint1**](glevalpoint.md) und **glEvalPoint2** generieren und werten einen einzelnen Punkt in einem Gitternetz aus.

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

Der ganzzahlige Wert für die Rasterdomänenvariable *i*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**Funktionen glMapGrid**](glmapgrid-functions.md) und [**glEvalMesh**](glevalmesh-functions.md) werden zusammen verwendet, um eine Reihe von Domänenwerten mit gleichmäßigem Abstand effizient zu generieren und zu bewerten. Sie können **glEvalPoint** verwenden, um einen einzelnen Rasterpunkt in demselben Gridspace zu bewerten, der von **glEvalMesh durchlaufen wird.** Das [**Aufrufen von glEvalPoint1**](glevalpoint.md) entspricht dem Aufrufen von

**glEvalCoord1** (*i* ?*u*  + *u* 1 );

where

? *u* = (*u* 2 *u* 1 )/*n*

und *n,* *u* 1 und *u* 2 sind die Argumente für die neueste **glMapGrid1-Funktion.** Die einzige absolute numerische Anforderung ist, dass bei  =  *i n* der wert aus berechnet wird (*i* ?*u* + u1 ) ist genau *u* 2 .

Im zweidimensionalen Fall **glEvalPoint2**, let

? *u* = (*u* 2 *u* 1 )/*n*

? *v* = (*v2* *v* 1 )/*m*

Dabei *sind n,* *u* 1, *u* 2, *m,* *v1* und *v2* die Argumente für die neueste **glMapGrid2-Funktion.** Anschließend entspricht die **glEvalPoint2-Funktion** dem Aufrufen von .

**glEvalCoord2** (*i* ?*u*  +  *u* 1 , *j* ?*v*  +  *v1*);

Die einzigen absoluten numerischen Anforderungen sind, dass bei = *i n* der wert aus berechnet wird (*i* ?*u*  +  *u* 1 ) ist genau u2, und wenn *j*  =  *m*, dann der wert berechnet aus ( j ?*v*  +  *v* 1 ) ist genau *v2*.

Die folgenden Funktionen rufen Informationen zu [**glEvalPoint1 und**](glevalpoint.md) **glEvalPoint2 ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ MAP1 \_ GRID \_ DOMAIN

**glGet mit** argument GL \_ MAP2 \_ GRID \_ DOMAIN

**glGet mit** dem Argument GL \_ MAP1 \_ GRID \_ SEGMENTS

**glGet** mit dem Argument GL \_ MAP2 \_ GRID \_ SEGMENTS

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> </dl>

 

 





