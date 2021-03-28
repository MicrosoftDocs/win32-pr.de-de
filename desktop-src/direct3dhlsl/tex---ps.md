---
title: tex-PS
description: Lädt das Ziel Register mit Farbdaten (RGBA), das aus einer Textur entnommen wurde. Die Textur muss mithilfe von SetTexture an eine bestimmte Textur Phase (n) gebunden werden. Die Textur Stichprobe wird von setsamplerstate gesteuert.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948896"
---
# <a name="tex---ps"></a>tex-PS

Lädt das Ziel Register mit Farbdaten (RGBA), das aus einer Textur entnommen wurde. Die Textur muss mithilfe von [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)an eine bestimmte Textur Phase (n) gebunden werden. Die Textur Stichprobe wird von [**setsamplerstate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)gesteuert.

## <a name="syntax"></a>Syntax



| tex-DST |
|---------|



 

where

-   DST ist das Ziel Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| tels                   | x    | x    | x    |      |      |      |       |      |       |



 

Die Ziel Registernummer gibt die Textur Phasen Nummer an.

Bei der Textur Stichprobe werden Texturkoordinaten verwendet, um einen Farbwert bei den angegebenen (u, v, w, q)-Koordinaten zu suchen, während die Attribute des Textur Stufen Zustands berücksichtigt werden.

Die Texturkoordinaten Daten werden aus den vertextextur-Koordinatendaten interpoliert und einer bestimmten Textur Phase zugeordnet. Die Standard Zuordnung ist eine eins-zu-Eins-Zuordnung zwischen der Reihenfolge der Textur Stufen und der Reihenfolge der Texturkoordinaten Deklaration. Dies bedeutet, dass der erste Satz von Texturkoordinaten, der im Scheitelpunkt Format definiert ist, standardmäßig mit Textur Phase 0 verknüpft ist.

Texturkoordinaten können jeder Phase mithilfe von zwei Techniken zugeordnet werden. Wenn Sie einen Scheitelpunkt-Shader oder eine Fixed-Funktions Pipeline verwenden, kann das Textur Stufen-Statusflag TSS \_ texcoordindex in [**settexturestagestate**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) verwendet werden, um Koordinaten zu einer Stufe zuzuordnen. Andernfalls werden die Texturkoordinaten von den Vertex-Shader-OTN-Registern ausgegeben, wenn ein programmierbarer Vertex-Shader verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 