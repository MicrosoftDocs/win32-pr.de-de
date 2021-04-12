---
title: glEvalMesh1-Funktion (GL. h)
description: Berechnet ein eindimensionales Raster von Punkten oder Zeilen.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- glEvalMesh1-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518095"
---
# <a name="glevalmesh1-function"></a>glEvalMesh1-Funktion

Berechnet ein eindimensionales Raster von Punkten oder Zeilen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Ein-Wert, der angibt, ob ein eindimensionales Mesh von Punkten oder Linien berechnet werden soll. Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ Point und GL \_ Line.

</dd> <dt>

*I1* 
</dt> <dd>

Der erste ganzzahlige Wert für die Raster Domänen Variable i.

</dd> <dt>

*I2* 
</dt> <dd>

Der letzte ganzzahlige Wert für die Raster Domänen Variable i.

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

Verwenden Sie " [**glmapgrid**](glmapgrid-functions.md) " und " [**glevalmesh**](glevalmesh-functions.md) ", um eine Reihe von gleichmäßig getrennten Zuordnungs Domänen Werten effizient zu generieren und auszuwerten. Die **glevalmesh** -Funktion durchläuft die ganzzahlige Domäne eines ein-oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungs Zuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden. Der Mode-Parameter bestimmt, ob die resultierenden Scheitel Punkte als Punkte, Linien oder gefüllte Polygone miteinander verbunden sind.

Im eindimensionalen Fall **glEvalMesh1** wird das Mesh generiert, als ob das folgende Code Fragment ausgeführt würde:

[**glBegin**](glbegin.md)(*Typ*);

for (i = I1; i <= I2; i + = 1)

{

[**glEvalCoord1**](glevalcoord1d.md)(i? u + U1)

}

[**glEnd**](glend.md)();

where

? u = (U2 U1)/n

und n, U1 und U2 sind die Argumente der neuesten [**glMapGrid1**](glmapgrid1d.md) -Funktion. Der *Typparameter* ist GL- \_ Punkte, wenn der Modus "GL Point" ist \_ , oder GL \_ Lines, wenn der Modus "GL \_ Line" ist Eine absolute numerische Anforderung besteht darin, dass der Wert, der von "i", "i" und "U1" berechnet wird, genau U2 ist.

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
</dt> </dl>

 

 





