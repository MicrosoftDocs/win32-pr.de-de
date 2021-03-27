---
title: ishl (SM4-ASM)
description: Nach links verschieben. | ishl (SM4-ASM)
ms.assetid: FA0213B8-8A76-4916-8B2F-0983C404A838
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e14225f8c8b0e46cf0ba6eda61f96e4563a904e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995582"
---
# <a name="ishl-sm4---asm"></a>ishl (SM4-ASM)

Nach links verschieben.



| dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1. Select- \_ Komponente |
|---------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] enthält die Werte, die verschoben werden sollen.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] enthält die UMSCHALT Menge.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine Komponenten Weise Verschiebung jedes 32-Bit-Werts in *src0* nach links durch eine ganzzahlige Bitzahl ohne Vorzeichen aus, die von der LSB 5 Bits (0-31 Range) in Quelle1 bereitgestellt wird *. Wählen Sie \_ Komponente* aus, und fügen Sie 0 ein. Die 32-Bit-pro-Komponenten Ergebnisse werden in *dest* platziert. Die Anzahl ist ein Skalarwert, der auf alle Komponenten angewendet wird.

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

 

 





