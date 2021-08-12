---
title: glEvalMesh2-Funktion (Gl.h)
description: Berechnet ein zweidimensionales Raster von Punkten oder Linien.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- glEvalMesh2-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5f1a16b1ceda2c13f24a779032b0e920d364db46167a9dc02ca2b27277262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616106"
---
# <a name="glevalmesh2-function"></a>glEvalMesh2-Funktion

Berechnet ein zweidimensionales Raster von Punkten oder Linien.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Ein -Wert, der angibt, ob ein zweidimensionales Gitternetz aus Punkten, Linien oder Polygonen berechnet werden soll. Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ POINT, GL \_ LINE und GL \_ FILL.

</dd> <dt>

*i1* 
</dt> <dd>

Der erste ganzzahlige Wert für die Rasterdomänenvariable i.

</dd> <dt>

*i2* 
</dt> <dd>

Der letzte ganzzahlige Wert für die Rasterdomänenvariable i.

</dd> <dt>

*j1* 
</dt> <dd>

Der erste ganzzahlige Wert für die Rasterdomänenvariable j.

</dd> <dt>

*j2* 
</dt> <dd>

Der letzte ganzzahlige Wert für die Rasterdomänenvariable j.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | Gibt an, dass *mode* kein akzeptierter Wert ist. <br/>                                                                            |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen. <br/> |



## <a name="remarks"></a>Hinweise

Verwenden Sie [**glMapGrid**](glmapgrid-functions.md) und [**glEvalMesh**](glevalmesh-functions.md) zusammen, um effizient eine Reihe von gleichmäßigen Zuordnungsdomänenwerten zu generieren und auszuwerten. Die **glEvalMesh-Funktion** durchgehen die ganzzahlige Domäne eines ein- oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungszuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden. Der Mode-Parameter bestimmt, ob die resultierenden Scheitelpunkte als Punkte, Linien oder gefüllte Polygone verbunden sind.

Im zweidimensionalen Fall **glEvalMesh2**, let

? u = (u2 u1)/n

? v = (v2 v1)/m,

wobei n, u1, u2, m, v1 und v2 die Argumente für die neueste [**glMapGrid2-Funktion**](glmapgrid-functions.md) sind. Wenn der *Modus* GL \_ FILL lautet, entspricht **glEvalMesh2** Folgendem:

für (j = j1; j < j2; j += 1)

{

[**glBegin**](glbegin.md)(GL \_ QUAD \_ STRIP);

für (i = i1; i <= i2; i += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ? v + v1);

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ? v + v1);

}

[**glEnd**](glend.md)( ); }

Wenn *der Modus* GL LINE \_ ist, entspricht ein Aufruf von **glEvalMesh2** Folgendem:

für (j = j1; j <= j2; j += 1)

{

[**glBegin**](glbegin.md)(GL \_ LINE \_ STRIP);

für (i = i1; i <= i2; i += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);

}

[**glEnd**](glend.md)( );

}

für (i = i1; i <= i2; i += 1)

{

[**glBegin**](glbegin.md)(GL \_ LINE \_ STRIP);

for (j = j1; j <= j1; j += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);

}

glEnd( );

}

Wenn der *Modus* GL \_ POINT ist, entspricht schließlich ein Aufruf von **glEvalMesh2:**

[**glBegin**](glbegin.md)(GL \_ POINTS);

für (j = j1; j <= j2; j += 1)

{

für (i = i1; i <= i2; i += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);

}

}

[**glEnd**](glend.md)( );

In allen drei Fällen sind die einzigen absoluten numerischen Anforderungen: Wenn i = n ist, dann der Wert, der aus i berechnet wird? u + u1 ist genau u2, und wenn j = m ist, dann der aus j berechnete Wert? v + v1 ist genau v2. Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glEvalMesh ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ MAP1 \_ GRID \_ DOMAIN

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ MAP2 \_ GRID \_ DOMAIN

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ MAP1 \_ GRID \_ SEGMENTS

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ MAP2 \_ GRID \_ SEGMENTS

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

 





