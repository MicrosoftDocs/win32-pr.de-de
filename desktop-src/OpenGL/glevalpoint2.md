---
title: glEvalPoint2-Funktion (Gl.h)
description: Die Funktionen glEvalPoint1 und glEvalPoint2 generieren und werten einen einzelnen Punkt in einem Gitternetz aus. | glEvalPoint2-Funktion (Gl.h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- glEvalPoint2-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f0c188ec5f3e8171b8035e58b235bc0c5942e221d6d85a6dd4e5a8ff1786c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675560"
---
# <a name="glevalpoint2-function"></a>glEvalPoint2-Funktion

Die Funktionen [**glEvalPoint1**](glevalpoint.md) und **glEvalPoint2** generieren und werten einen einzelnen Punkt in einem Gitternetz aus.

## <a name="syntax"></a>Syntax


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*i* 
</dt> <dd>

Der ganzzahlige Wert für die Rasterdomänenvariable *i*.

</dd> <dt>

*j* 
</dt> <dd>

Der ganzzahlige Wert für die Rasterdomänenvariable *j* .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die Funktionen [**glMapGrid**](glmapgrid-functions.md) und [**glEvalMesh**](glevalmesh-functions.md) werden zusammen verwendet, um eine Reihe von gleichmäßigen Zuordnungsdomänenwerten effizient zu generieren und auszuwerten. Sie können **glEvalPoint** verwenden, um einen einzelnen Rasterpunkt im gleichen Rasterbereich auszuwerten, der von **glEvalMesh** durchlaufen wird. Das Aufrufen von [**glEvalPoint1**](glevalpoint.md) entspricht dem Aufrufen von .

**glEvalCoord1** (*i* ?*u*  + *u* 1 );

where

? *u* = (*u* 2 *u* 1 )/*n*

und *n*, *u* 1 und *u* 2 sind die Argumente für die neueste **glMapGrid1-Funktion.** Die einzige absolute numerische Anforderung besteht darin, dass bei *i*  =  *n* der Wert aus berechnet wird (*i* ?*u* + u1 ) ist genau *u* 2 .

Im zweidimensionalen Fall **glEvalPoint2**, let

? *u* = (*u* 2 *u* 1 )/*n*

? *v* = (*v* 2 *v* 1 *)/m*

wobei *n*, *u* 1, *u* 2 , *m*, *v* 1 und *v* 2 die Argumente für die neueste **glMapGrid2-Funktion** sind. Dann entspricht die **glEvalPoint2-Funktion** dem Aufrufen von .

**glEvalCoord2** (*i* ?*u*  +  *u* 1 , *j* ?*v*  +  *v* 1 );

Die einzigen absoluten numerischen Anforderungen sind folgende: Wenn *ich* = *n* habe, dann der Wert, der aus berechnet wurde (*i* ?*u*  +  *u* 1 ) ist genau u2, und wenn *j*  =  *m*, dann wird der Wert berechnet aus (*j* ?*v*  +  *v* 1 ) ist genau *v* 2 .

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glEvalPoint1**](glevalpoint.md) und **glEvalPoint2** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ MAP1 \_ GRID \_ DOMAIN

**glGet** mit argument GL \_ MAP2 \_ GRID \_ DOMAIN

**glGet** mit dem Argument GL \_ MAP1 \_ GRID \_ SEGMENTS

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

 

 





