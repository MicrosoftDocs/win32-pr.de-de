---
title: dcl_function_table (SM5-ASM)
description: Deklarieren Sie eine Funktions Tabelle.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993254"
---
# <a name="dcl_function_table-sm5---asm"></a>DCL \_ \_ -Funktions Tabelle (SM5-ASM)

Deklarieren Sie eine Funktions Tabelle.



| DCL- \_ Funktions \_ Tabelle ft \# = {FB \# , FB \# ,...} |
|-----------------------------------------------|



 



| Element                                                      | BESCHREIBUNG                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span id="ft"></span><span id="FT"></span>*GRA*<br/> | \[in \] den Funktionstabellen Einträgen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion deklariert eine Funktions Tabelle als Satz von Funktions Texten, die zuvor deklariert wurden.

Dies entspricht einer C++ Vtable, es sei denn, es gibt einen Eintrag pro CallSite für eine Schnittstelle anstelle von pro Methode.

Es gibt keine Beschränkung für die Anzahl der Funktions Texte, die in einer Funktions Tabelle aufgeführt werden können.

Es ist zulässig, dass ein angegebener Funktions Text-FB \# mehrmals in einer oder mehreren Funktionstabellen referenziert wird, um gemeinsamen Code freizugeben.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





