---
title: tex – ps
description: Lädt das Zielregister mit Farbdaten (RGBA), die aus einer Textur entnommen wurden. Die Textur muss mithilfe von SetTexture an eine bestimmte Texturstufe (n) gebunden werden. Textursampler wird durch SetSamplerState gesteuert.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0646a057fdc2fb96e5f72e7451b9b273191ced22f5092a14fab11a9042c5de25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788109"
---
# <a name="tex---ps"></a>tex – ps

Lädt das Zielregister mit Farbdaten (RGBA), die aus einer Textur entnommen wurden. Die Textur muss mithilfe von [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)an eine bestimmte Texturstufe (n) gebunden werden. Textursampler wird von [**SetSamplerState gesteuert.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)

## <a name="syntax"></a>Syntax



| tex dst |
|---------|



 

where

-   dst ist das Zielregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Tex                   | x    | x    | x    |      |      |      |       |      |       |



 

Die Zielregisternummer gibt die Texturphasennummer an.

Bei der Texturstichprobe werden Texturkoordinaten verwendet, um einen Farbwert an den angegebenen Koordinaten (u,v,w,q) zu suchen oder zu beproben, während die Zustandsattribute der Texturphase berücksichtigt werden.

Die Texturkoordinatendaten werden aus den Koordinatendaten der Scheitelpunkttextur interpoliert und einer bestimmten Texturstufe zugeordnet. Die Standardzuordnung ist eine 1:1-Zuordnung zwischen der Texturstufennummer und der Reihenfolge der Texturkoordinatendeklaration. Dies bedeutet, dass der erste Satz von Texturkoordinaten, die im Scheitelpunktformat definiert sind, standardmäßig Texturstufe 0 zugeordnet ist.

Texturkoordinaten können jeder Phase mithilfe von zwei Techniken zugeordnet werden. Bei Verwendung eines Vertex-Shaders einer festen Funktion oder der Festen Funktionspipeline kann das Texturphasenzustandsflag TSS \_ TEXCOORDINDEX in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) verwendet werden, um einer Phase Koordinaten zu zuordnen. Andernfalls werden die Texturkoordinaten von den Vertex-Shader-oTn-Registern ausgegeben, wenn ein programmierbarer Vertex-Shader verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 