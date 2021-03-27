---
title: texldd-PS
description: Modelliert eine Textur mit zusätzlichen Farbverlaufs Eingaben.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390343"
---
# <a name="texldd---ps"></a>texldd-PS

Modelliert eine Textur mit zusätzlichen Farbverlaufs Eingaben.

## <a name="syntax"></a>Syntax



| texldd, DST, src0, Quelle1, Quelle2, src3 |
|-------------------------------------|



 

Hierbei gilt:

-   DST ist ein Ziel Register.
-   src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt. Siehe [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   Quelle1 identifiziert die Quell-Samplerregister \# , bei der \# angibt, welche Textur samplingnummer Stichproben geben soll. Der Sampler hat ihm eine Textur und einen von der [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) -Enumeration definierten Steuerelement Zustand zugeordnet (z. D3DSAMP \_ MinFilter).
-   Quelle2 ist ein Eingabe Quellen Register, das den x-Farbverlauf angibt.
-   src3 ist ein Eingabe Quellen Register, das den y-Farbverlauf angibt.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldd                |      |      |      |      |      | Stuben \* | x     | x    | x     |



 

\* Diese Anweisung wird nur von PS \_ 2 a unterstützt \_ . Sie wird von PS 2 b nicht unterstützt \_ \_ . Weitere Informationen zu Profilen finden Sie unter [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).

Diese Anweisung unterscheidet eine Textur mithilfe der Texturkoordinaten bei src0, dem durch Quelle1 angegebenen Sampler und den Gradienten DSX und DSY aus Quelle2 und src3. Die Werte für x und y-Farbverlauf werden verwendet, um die entsprechende MipMap-Ebene der Textur für die Stichprobenentnahme auszuwählen.

Alle Quellen unterstützen willkürliche Streifen.

Alle Schreib Masken sind auf dem Ziel gültig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 