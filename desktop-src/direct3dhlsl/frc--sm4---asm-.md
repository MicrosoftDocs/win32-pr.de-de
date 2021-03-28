---
title: FRC (SM4-ASM)
description: Komponenten Weise extrahieren Sie eine Bruchteile Komponente.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4abcfd56e7d6051e9c476097b3e5eef4d97563e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976432"
---
# <a name="frc-sm4---asm"></a>FRC (SM4-ASM)

Komponenten Weise extrahieren Sie eine Bruchteile Komponente.



| FRC \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|-------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> *dest*  =  *src0*  -  [Round \_ NI](round-ni--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der-Komponente im-Vorgang.<br/>                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen abgerufen wurden.



|          |          |            |             |        |        |             |            |          |         |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **src**  | **-INF** | **-F**     | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F**     | **+ INF** | **NaN** |
| **dest** | NaN      | \[+ 0 bis 1) | +0          | +0     | +0     | +0          | \[+ 0 bis 1) | NaN      | NaN     |



 

F bedeutet eine endliche reelle Zahl.

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

 

 





