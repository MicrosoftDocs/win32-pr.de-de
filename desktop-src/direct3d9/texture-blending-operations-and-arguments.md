---
description: Anwendungen ordnen jeder Textur in der Gruppe der aktuellen Texturen eine Mischungsphase zu. Direct3D wertet jede Mischungsphase in der Reihenfolge aus, beginnend mit der ersten Textur in der Menge und endet mit der achten.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Texturmischungsvorgänge und -argumente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d242092de5919267d30a9b8ff4e7bd2324f0bc3120649d3bb1a423b3462be77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797772"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a>Texturmischungsvorgänge und -argumente (Direct3D 9)

Anwendungen ordnen jeder Textur in der Gruppe der aktuellen Texturen eine Mischungsphase zu. Direct3D wertet jede Mischungsphase in der Reihenfolge aus, beginnend mit der ersten Textur in der Menge und endet mit der achten.

Direct3D wendet die Informationen aus jeder Textur in der Gruppe der aktuellen Texturen auf die zugehörige Mischungsphase an. Anwendungen steuern, welche Informationen aus einer Texturphase verwendet werden, indem [**sie IDirect3DDevice9::SetTextureStageState aufrufen.**](/windows/desktop/api) Sie können separate Vorgänge für die Farb- und Alphakanäle festlegen, und jeder Vorgang verwendet zwei Argumente. Geben Sie Farbkanalvorgänge mithilfe des D3DTSS COLOROP-Phasenstatus an, und geben Sie \_ Alphavorgänge mithilfe von D3DTSS \_ ALPHAOP an. In beiden Phasenzuständen werden Werte des [**aufzählten D3DTEXTUREOP-Typs**](./d3dtextureop.md) verwendet.

Texturmischungsargumente verwenden die D3DTSS-Member \_ COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 und D3DTSS \_ ALPHARG2 des aufzählten [**D3DTEXTURESTAGESTATETYPE-Typs.**](./d3dtexturestagestatetype.md) Die entsprechenden Argumentwerte werden mithilfe von [D3DTA identifiziert.](d3dta.md)

> [!Note]  
> Sie können eine Texturphase und alle nachfolgenden Texturmischungsphasen in der Kaskadierung deaktivieren, indem Sie den Farbvorgang für diese Phase auf D3DTOP \_ DISABLE festlegen. Wenn Sie den Farbvorgang deaktivieren, wird auch der Alphavorgang deaktiviert. Alphavorgänge können nicht deaktiviert werden, wenn Farbvorgänge aktiviert sind. Das Festlegen des Alpha-Vorgangs auf D3DTOP DISABLE, wenn Farbblending aktiviert ist, führt zu \_ nicht definiertem Verhalten.

 

Um die unterstützten Texturmischungsvorgänge eines Geräts zu bestimmen, fragen Sie den TextureCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturmischung](texture-blending.md)
</dt> </dl>

 

 
