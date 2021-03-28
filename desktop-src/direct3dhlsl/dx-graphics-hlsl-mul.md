---
title: mul
description: Multipliziert x und y mithilfe von Matrix Mathematik. Die inneren Dimensionen x-Columns und y-Rows müssen gleich sein.
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- Mul HLSL
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2e9fe545cb16f8ac1fef1935b9d7e97075521b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037770"
---
# <a name="mul"></a>mul

Multipliziert x und y mithilfe von Matrix Mathematik. Die inneren Dimensionen x-Columns und y-Rows müssen gleich sein.



| Ret Mul (x, y) |
|---------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] x-Eingabe Wert. Wenn x ein Vektor ist, wird es als Zeilen Vektor behandelt.<br/>    |
| <span id="y"></span><span id="Y"></span>*Teenie*<br/> | \[im \] y-Eingabe Wert. Wenn y ein Vektor ist, wird er als Spalten Vektor behandelt.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Das Ergebnis von x mal y. Das Ergebnis verfügt über die Dimension x-Rows x y-Columns.

## <a name="type-description"></a>Typbeschreibung

Es gibt 9 überladene Versionen dieser Funktion: in den überladenen Versionen werden die unterschiedlichen Fälle für die Typen und Größen der Eingabeargumente behandelt.



| Version | Name | Zweck | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md) | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | Skalar                                                        | identisch mit Eingabe x                                                | 1                                                                        |
|         | TZI  | out     | Skalar                                                        | identisch mit Eingabe x                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | Vektor                                                        | float, int                                                     | any                                                                      |
|         | TZI  | out     | Vektor                                                        | float, int                                                     | gleiche Dimension (n) wie Eingabe y                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | Matrix                                                        | float, int                                                     | any                                                                      |
|         | TZI  | out     | Matrix                                                        | identisch mit der Eingabe y                                                | gleiche Dimension (n) wie Eingabe y                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Vektor                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | TZI  | out     | Vektor                                                        | float, int                                                     | gleiche Dimension (n) wie Eingabe x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Vektor                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Vektor                                                        | float, int                                                     | gleiche Dimension (n) wie Eingabe x                                             |
|         | TZI  | out     | Skalar                                                        | float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Vektor                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Matrix                                                        | float, int                                                     | Rows = gleiche Dimension (n) wie Eingabe x, Spalten = beliebig                       |
|         | TZI  | out     | Vektor                                                        | float, int                                                     | gleiche Dimension (n) als Eingabe-y-Spalten                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Skalar                                                        | float, int                                                     | 1                                                                        |
|         | TZI  | out     | Matrix                                                        | float, int                                                     | gleiche Dimension (n) wie Eingabe x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Vektor                                                        | float, int                                                     | Anzahl von Spalten in der Eingabe x                                             |
|         | TZI  | out     | Vektor                                                        | float, int                                                     | Anzahl der Zeilen in der Eingabe x                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | Matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | Matrix                                                        | float, int                                                     | Rows = Anzahl der Spalten in der Eingabe x                                      |
|         | TZI  | out     | Matrix                                                        | float, int                                                     | Rows = Anzahl der Zeilen in der Eingabe x, Spalten = Anzahl der Spalten in der Eingabe y |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shader-Modelle | ja       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





