---
title: dcl_tgsm_raw (sm5 – asm)
description: Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Threadgruppe des Compute-Shaders verfügbar ist.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0945cde7719129ca43368e50258c02727103209b8d467932e79acd1e1150c89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024690"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>dcl \_ tgsm \_ raw (sm5 – asm)

Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Threadgruppe des Compute-Shaders verfügbar ist.



| dcl \_ tgsm \_ raw g , \# byteCount |
|-------------------------------|



 



| Element                                                                                                       | BESCHREIBUNG                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                 | \[in \] Ein Verweis auf einen Block der Größe *byteCount* des nicht typierten freigegebenen Arbeitsspeichers. <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*Bytecount*<br/> | \[in \] muss ein Vielfaches von 4 sein. <br/>                                             |



 

## <a name="remarks"></a>Hinweise

Der Gesamtspeicher für alle g \# muss <= die Menge des pro Threadgruppe verfügbaren freigegebenen Arbeitsspeichers (32 KB) betragen.

Im Extremfall können Sie 8192 g gesamt deklarieren, \# jeweils mit einem *byteCount-Wert* von 4.

Im entgegengesetzten Extremfall können Sie ein einzelnes g \# mit einem *byteCount* von 32768 deklarieren.

> [!Note]  
> cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützt [dcl \_ tgsm \_ structured](dcl-tgsm-structured--sm5---asm-.md), aber nicht **dcl \_ tgsm \_ raw**.

 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

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

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





