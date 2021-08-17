---
title: dcl_function_body (sm5 - asm)
description: Deklarieren Sie einen Funktionskörper.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339e7f5d7edb91f4f3405b328286a9ae32a8108efdaafaba1f212870be7ff8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727234"
---
# <a name="dcl_function_body-sm5---asm"></a>\_ \_ dcl-Funktionskörper (sm5 - asm)

Deklarieren Sie einen Funktionskörper.



| dcl \_ function \_ body fb\# |
|--------------------------|



 



| Element                                                          | Beschreibung                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*Fb\#*<br/> | \[in \] Die Bezeichnung des Orts, an dem die Funktion angezeigt wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung deklariert einen eindeutigen Funktionskörper, dessen Code später im Programm bei der Bezeichnung fb angezeigt \# wird.

Funktionskörper werden in Funktionstabellendeklarationen verwendet. Weitere Informationen finden Sie in der [ \_ dcl-Funktionstabelle. \_ ](dcl-function-table---sm5---asm-.md)

Im Hüllen-Shader und Domänen-Shader, in dem es mehrere Phasen gibt (Kontrollpunktphase, Forkphase und Joinphase), werden alle Funktionskörper (Bezeichnung fb ) nach allen Phasen angezeigt, anstatt nach Phase zu gruppiert \# zu werden.

Es gibt keine Beschränkung, wie viele Funktionskörper vorhanden sein können.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





