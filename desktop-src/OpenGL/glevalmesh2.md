---
title: glEvalMesh2-Funktion (GL. h)
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
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740672"
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

Ein-Wert, der angibt, ob ein zweidimensionales Gitter von Punkten, Linien oder Polygonen berechnet werden soll. Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ Point, GL \_ Line und GL \_ Fill.

</dd> <dt>

*I1* 
</dt> <dd>

Der erste ganzzahlige Wert für die Raster Domänen Variable i.

</dd> <dt>

*I2* 
</dt> <dd>

Der letzte ganzzahlige Wert für die Raster Domänen Variable i.

</dd> <dt>

*j1* 
</dt> <dd>

Der erste ganzzahlige Wert für die Raster Domänen Variable j.

</dd> <dt>

*j2* 
</dt> <dd>

Der letzte ganzzahlige Wert für die Raster Domänen Variable j.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Gibt an, dass der *Modus* kein akzeptierter Wert ist. <br/>                                                                            |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen. <br/> |



## <a name="remarks"></a>Bemerkungen

Verwenden Sie " [**glmapgrid**](glmapgrid-functions.md) " und " [**glevalmesh**](glevalmesh-functions.md) " gemeinsam, um eine Reihe von gleichmäßig getrennten Zuordnungs Domänen Werten effizient zu generieren und auszuwerten. Die **glevalmesh** -Funktion durchläuft die ganzzahlige Domäne eines ein-oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungs Zuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden. Der Mode-Parameter bestimmt, ob die resultierenden Scheitel Punkte als Punkte, Linien oder gefüllte Polygone miteinander verbunden sind.

Im zweidimensionalen Fall, **glEvalMesh2**, Let

? u = (U2 U1)/n

? v = (V2 V1)/m,

Dabei sind n, U1, U2, m, v1 und v2 die Argumente der neuesten [**glMapGrid2**](glmapgrid-functions.md) -Funktion. Wenn der *Modus* dann "GL \_ Fill" ist, entspricht **glEvalMesh2** dem folgenden:

for (j = J1; j < J2; j + = 1)

{

[**glBegin**](glbegin.md)(GL \_ Quad \_ Strip);

for (i = I1; i <= I2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), j? v + v1);

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), (j + 1)? v + v1);

}

[**glEnd**](glend.md)(); }

Wenn der *Modus* "GL" ist \_ , entspricht ein **glEvalMesh2** -Rückruf dem folgenden:

for (j = J1; j <= J2; j + = 1)

{

[**glBegin**](glbegin.md)(GL- \_ Zeilen \_ Streifen);

for (i = I1; i <= I2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

[**glEnd**](glend.md)();

}

for (i = I1; i <= I2; i + = 1)

{

[**glBegin**](glbegin.md)(GL- \_ Zeilen \_ Streifen);

for (j = J1; j <= J1; j + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

glEnd ();

}

Wenn der *Modus* "GL Point" lautet \_ , entspricht ein **glEvalMesh2** -Rückruf dem folgenden:

[**glBegin**](glbegin.md)(GL- \_ Punkte);

for (j = J1; j <= J2; j + = 1)

{

for (i = I1; i <= I2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

}

[**glEnd**](glend.md)();

In allen drei Fällen sind die einzigen absoluten numerischen Anforderungen, dass der Wert, der von i u + U1 ist genau U2, und wenn j = m ist, dann wird der von j berechnete Wert angezeigt. v + v1 ist genau v2. Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glevalmesh** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Domäne

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Domäne

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Segmente

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Segmente

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

 





