---
title: glEvalMesh1-Funktion (Gl.h)
description: Berechnet ein eindimensionales Raster von Punkten oder Linien.
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
ms.openlocfilehash: c325134a8a8fd60afdc764eebc8a4de9bd507b5b667ebb8e1b2ab967edcd7e77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625470"
---
# <a name="glevalmesh1-function"></a>glEvalMesh1-Funktion

Berechnet ein eindimensionales Raster von Punkten oder Linien.

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

Ein -Wert, der angibt, ob ein eindimensionales Gitternetz von Punkten oder Linien berechnet werden soll. Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ POINT und GL \_ LINE.

</dd> <dt>

*i1* 
</dt> <dd>

Der erste ganzzahlige Wert für die Rasterdomänenvariable i.

</dd> <dt>

*i2* 
</dt> <dd>

Der letzte ganzzahlige Wert für die Rasterdomänenvariable i.

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

Verwenden Sie [**glMapGrid**](glmapgrid-functions.md) und [**glEvalMesh**](glevalmesh-functions.md) zusammen, um eine Reihe von gleichmäßigen Zuordnungsdomänenwerten effizient zu generieren und auszuwerten. Die **glEvalMesh-Funktion** durchgehen die ganzzahlige Domäne eines ein- oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungszuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden. Der Mode-Parameter bestimmt, ob die resultierenden Scheitelpunkte als Punkte, Linien oder gefüllte Polygone verbunden sind.

Im eindimensionalen Fall **glEvalMesh1** wird das Gitternetz so generiert, als ob das folgende Codefragment ausgeführt würde:

[**glBegin**](glbegin.md)(*typ*);

für (i = i1; i <= i2; i += 1)

{

[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)

}

[**glEnd**](glend.md)( );

where

?u = (u2 u1) / n

und n, u1 und u2 sind die Argumente für die neueste [**glMapGrid1-Funktion.**](glmapgrid1d.md) Der *Typparameter* ist "GL \_ POINTS", wenn der Modus "GL \_ POINT" ist, oder "GL \_ LINES", wenn der Modus "GL \_ LINE" ist. Die einzige absolute numerische Anforderung ist, dass bei i = n der aus i?u + u1 berechnete Wert genau u2 ist.

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
</dt> </dl>

 

 





