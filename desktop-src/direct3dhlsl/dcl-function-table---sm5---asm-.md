---
title: dcl_function_table (sm5 - asm)
description: Deklarieren Sie eine Funktionstabelle.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549653ee7316a664b628d5cdc692c091bdf042ad24e89b983c0fd3aac8a67ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490890"
---
# <a name="dcl_function_table-sm5---asm"></a>\_ \_ dcl-Funktionstabelle (sm5 - asm)

Deklarieren Sie eine Funktionstabelle.



| dcl \_ function table ft = \_ \# {fb , fb , \# \# ...} |
|-----------------------------------------------|



 



| Element                                                      | Beschreibung                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span id="ft"></span><span id="FT"></span>*Ft*<br/> | \[in \] Die Funktionstabelleneinträge.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Funktion deklariert eine Funktionstabelle als einen Satz von Funktionskörpern, die zuvor deklariert wurden.

Dies ist wie eine C++-VTable, mit der Ausnahme, dass es einen Eintrag pro Aufrufsite für eine Schnittstelle statt pro Methode gibt.

Es gibt keine Beschränkung, wie viele Funktionskörper in einer Funktionstabelle aufgelistet werden können.

Es ist gültig, dass auf einen bestimmten Funktionskörper fb mehrmals in einer oder mehreren Funktionstabellen verwiesen wird, um gemeinsamen \# Code zu teilen.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
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

 

 





