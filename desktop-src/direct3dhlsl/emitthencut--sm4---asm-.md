---
title: emitthencut (SM4-ASM)
description: Entspricht einem Ausgabe Befehl gefolgt von einem Befehl zum Ausschneiden. | emitthencut (SM4-ASM)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5b413ca11e22c7cfc17691fc0a39fe96bf7c0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353859"
---
# <a name="emitthencut-sm4---asm"></a>emitthencut (SM4-ASM)

Entspricht einem Ausgabe [Befehl gefolgt von einem Befehl zum](emit--sm4---asm-.md) [Ausschneiden](cut--sm4---asm-.md) .



| emitthencut |
|-------------|



 

## <a name="remarks"></a>Bemerkungen

Dieser Befehl ist nützlich, wenn der letzte Scheitelpunkt in einer Topologie wissentlich ausgegeben wird.

Wenn Streams deklariert wurden, müssen Sie [emitthenausschneide Daten \_ Strom](emitthencut-stream--sm5---asm-.md)verwenden.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

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

 

 




