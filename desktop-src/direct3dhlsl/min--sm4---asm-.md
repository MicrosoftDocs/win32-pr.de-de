---
title: min (sm4 - asm)
description: Komponentenweiser gleitkommamindest.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddabe79f70255cddc0f94302eb8147037e378c3197f3656a6d3369bb68e3e36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672580"
---
# <a name="min-sm4---asm"></a>min (sm4 - asm)

Komponentenweiser gleitkommamindest.



| min \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Ergebnis des Vorgangs.<br/> *dest*  =  *src0*  <  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten, die mit *src1* verglichen werden sollen.<br/>                                                  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Komponenten, die mit *src0* verglichen werden sollen.<br/>                                                  |



 

## <a name="remarks"></a>Hinweise

>= wird anstelle von > verwendet, sodass, wenn min(x,y) = x, max(x,y) = y.

NaN verfügt über eine spezielle Behandlung. Wenn ein Quelloperand NaN ist, wird der andere Quelloperand zurückgegeben, und die Auswahl erfolgt pro Komponente. Wenn beide NaN sind, wird eine beliebige NaN-Darstellung zurückgegeben. Dies entspricht den neuen IEEE 754R-Regeln.

Denormen werden geleert, wobei das Vorzeichen vor dem Vergleich beibehalten wird. Das in *dest* geschriebene Ergebnis kann jedoch denormiert werden.

Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen erzielt werden, vorausgesetzt, dass weder Überlauf noch Unterlauf auftreten. F bedeutet endliche reelle Zahl.



| **src0 src1->** | **-inf** | **F**        | **+inf** | **NaN** |
|--------------------|----------|--------------|----------|---------|
| **-inf**           | -inf     | -inf         | -inf     | -inf    |
| **F**              | -inf     | src0 oder src1 | src0     | src0    |
| **-inf**           | -inf     | src1         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





