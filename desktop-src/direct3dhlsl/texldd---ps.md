---
title: texldd – ps
description: Probieren Sie eine Textur mit zusätzlichen Farbverlaufseingaben aus.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45bd755cdc0d183a6b06e42cbd9fb3934a5dc26a729e9982bc54fb9d2a2b01fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561970"
---
# <a name="texldd---ps"></a>texldd – ps

Probieren Sie eine Textur mit zusätzlichen Farbverlaufseingaben aus.

## <a name="syntax"></a>Syntax



| texldd, dst, src0, src1, src2, src3 |
|-------------------------------------|



 

Hierbei gilt:

-   dst ist ein Zielregister.
-   src0 ist ein Quellregister, das die Texturkoordinaten für das Texturbeispiel bereitstellt. Siehe [Texturkoordinatenregister.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifiziert das Quell-Samplerregister \# (s), wobei \# angibt, welche Textur-Samplernummer entnommen werden soll. Der Sampler hat ihm eine Textur und einen Durch die [**D3DSAMPLERSTATETYPE-Enumeration**](/windows/desktop/direct3d9/d3dsamplerstatetype) definierten Steuerelementzustand zugeordnet (z. B. D3DSAMP \_ MINFILTER).
-   src2 ist ein Eingabequellregister, das den x Farbverlauf angibt.
-   src3 ist ein Eingabequellregister, das den y-Farbverlauf angibt.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldd                |      |      |      |      |      | X \* | x     | x    | x     |



 

\* Diese Anweisung wird nur von ps \_ 2 \_ a unterstützt. Sie wird von ps 2 b nicht \_ \_ unterstützt. Weitere Informationen zu Profilen finden Sie unter [**D3DXGetPixelShaderProfile.**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)

Diese Anweisung erfasst eine Textur mithilfe der Texturkoordinaten bei src0, des von src1 angegebenen Samplers und der Farbverläufe DSX und DSY, die von src2 und src3 stammen. Die Farbverlaufswerte x und y werden verwendet, um die entsprechende Mipmapebene der Textur für die Stichprobenentnahme auszuwählen.

Alle Quellen unterstützen beliebige Swizzles.

Alle Schreibmasken sind auf dem Ziel gültig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 