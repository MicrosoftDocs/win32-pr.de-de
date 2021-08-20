---
title: frc (sm4 - asm)
description: Komponentenweises Extrahieren von Bruchteilen einer Komponente.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7726837a8c88e21b1756c08963a08f3714a9cdb4d93159ed80848166d84e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907613"
---
# <a name="frc-sm4---asm"></a>frc (sm4 - asm)

Komponentenweises Extrahieren von Bruchteilen einer Komponente.



| frc \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|-------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> *dest*  =  *src0*  -  [round \_ ni](round-ni--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponente im Vorgang.<br/>                                                                                        |



 

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen erzielt werden.



| **src**  | **-inf** | **-F**     | **-denorm** | **-0** | **+0** | **+denorm** | **+F**     | **+inf** | **NaN** |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **Dest** | NaN      | \[+0 bis 1) | +0          | +0     | +0     | +0          | \[+0 bis 1) | NaN      | NaN     |



 

F bedeutet endliche reelle Zahl.

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

 

 





