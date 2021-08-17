---
title: Matrixtyp
description: Eine Matrix ist ein spezieller Datentyp, der zwischen einer und 16 Komponenten enthält. Jede Komponente einer Matrix muss denselben Typ aufweisen.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Matrixtyp HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e6b98309c760a3da4d1e9c488e4aed049aa34f0b449042e8f00a02426cc513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726170"
---
# <a name="matrix-type"></a>Matrixtyp

Eine Matrix ist ein spezieller Datentyp, der zwischen einer und 16 Komponenten enthält. Jede Komponente einer Matrix muss denselben Typ aufweisen.



|                         |
|-------------------------|
| **TypeComponents-Name** |



 

## <a name="components"></a>Komponenten



| Element                                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Ein einzelner Name, der drei Teile enthält. Der erste Teil ist einer der [skalaren](dx-graphics-hlsl-data-types.md) Typen. Der zweite Teil ist die Anzahl der Zeilen. Der dritte Teil ist die Anzahl der Spalten. Die Anzahl der Zeilen und Spalten ist eine positive ganze Zahl zwischen 1 und 4 einschließlich.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**<br/>                                         | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a>Beispiele

Hier sind einige Beispiele:


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Eine Matrix kann auch mit dieser Syntax deklariert werden:


```
matrix <Type, Number> VariableName
```



Der Matrixtyp verwendet die spitzen Klammern, um den Typ, die Anzahl der Zeilen und die Anzahl der Spalten anzugeben. In diesem Beispiel wird eine Gleitkommamatrix mit zwei Zeilen und zwei Spalten erstellt. Jeder der skalaren Datentypen kann verwendet werden.

Beispiel:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





