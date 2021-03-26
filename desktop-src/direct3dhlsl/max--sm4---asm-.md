---
title: Max (SM4-ASM)
description: Der Komponenten Weise Gleit Komma Wert.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389501"
---
# <a name="max-sm4---asm"></a>Max (SM4-ASM)

Der Komponenten Weise Gleit Komma Wert.



| Max \[ \_ \] . Sat dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[im \] Ergebnis des Vorgangs. <br/> *dest*  =  *src0*  >=  *Quelle1* ? *src0* : *Quelle1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.<br/>                                                    |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den Komponenten, die mit *src0* verglichen werden sollen.<br/>                                                    |



 

## <a name="remarks"></a>Bemerkungen

>= wird anstelle von > verwendet, sodass, wenn min (x, y) = x, dann Max (x, y) = y ist.

Nan hat eine besondere Behandlung. Wenn ein Quell Operand NaN ist, wird der andere Quell Operand zurückgegeben, und die Auswahl erfolgt pro Komponente. Wenn beide Nan sind, wird eine Nan-Darstellung zurückgegeben.

Denorms werden vor dem Vergleich mit einem Vorzeichen geleert. Das in *dest* geschriebene Ergebnis wird jedoch möglicherweise nicht denorm geleert.

In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt F bedeutet eine begrenzte reelle Zahl.



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| **src0 Quelle1->** | **-INF** | **F**        | **+ INF** | **NaN** |
| **-INF**           | -inf     | src1         | +inf     | -inf    |
| **F**              | src0     | src0 oder Quelle1 | +inf     | src0    |
| **+ INF**           | +inf     | +inf         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





