---
title: mul
description: Multipliziert x und y mithilfe der Matrixmathematik. Die x-spalten- und y-Zeilen der inneren Dimension müssen gleich sein.
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- mul HLSL
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6362c734cbbf30defa8fed75f28c6f39397d75977488d9efc170d2647a9b3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950360"
---
# <a name="mul"></a>mul

Multipliziert x und y mithilfe der Matrixmathematik. Die x-spalten- und y-Zeilen der inneren Dimension müssen gleich sein.



| ret mul(x, y) |
|---------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der x-Eingabewert. Wenn x ein Vektor ist, wird es als Zeilenvektor behandelt.<br/>    |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Der y-Eingabewert. Wenn y ein Vektor ist, wird er als Spaltenvektor behandelt.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Das Ergebnis von x mal y. Das Ergebnis weist die Dimension x-rows x y-columns auf.

## <a name="type-description"></a>Typbeschreibung

Es gibt 9 überladene Versionen dieser Funktion. die überladenen Versionen verarbeiten die verschiedenen Fälle für die Typen und Größen der Eingabeargumente.



| Version | Name | Zweck | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md) | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | Skalar                                                        | identisch mit eingabe x                                                | 1                                                                        |
|         | Ret  | out     | Skalar                                                        | identisch mit eingabe x                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | Vektor                                                        | float, int                                                     | any                                                                      |
|         | Ret  | out     | Vektor                                                        | float, int                                                     | gleiche Dimension(en) wie eingabe y                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | Matrix                                                        | float, int                                                     | any                                                                      |
|         | Ret  | out     | Matrix                                                        | entspricht der Eingabe y                                                | gleiche Dimension(en) wie eingabe y                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Vektor                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | Ret  | out     | Vektor                                                        | float, int                                                     | Gleiche Dimension(en) wie eingabe x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Vektor                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Vektor                                                        | float, int                                                     | Gleiche Dimension(n) wie Eingabe x                                             |
|         | Ret  | out     | Skalar                                                        | float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Vektor                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Matrix                                                        | float, int                                                     | rows = gleiche Dimension(n) wie Eingabe x, Spalten = any                       |
|         | Ret  | out     | Vektor                                                        | float, int                                                     | Gleiche Dimension(n) wie Eingabe-y-Spalten                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | Ret  | out     | Matrix                                                        | float, int                                                     | Gleiche Dimension(n) wie Eingabe x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Vektor                                                        | float, int                                                     | Anzahl der Spalten in Eingabe x                                             |
|         | Ret  | out     | Vektor                                                        | float, int                                                     | Anzahl der Zeilen in Eingabe x                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Matrix                                                        | float, int                                                     | rows = Anzahl der Spalten in Eingabe x                                      |
|         | Ret  | out     | Matrix                                                        | float, int                                                     | rows = Anzahl der Zeilen in Eingabe x, Spalten = Anzahl der Spalten in der Eingabe y |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shadermodelle | Ja       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





