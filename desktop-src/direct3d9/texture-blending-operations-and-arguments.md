---
description: Anwendungen ordnen jeder Textur im Satz der aktuellen Texturen eine Mischungsphase zu. Direct3D wertet jede Mischungsphase in der reihenfolge aus, beginnend mit der ersten Textur im Satz und endend mit der achten.
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

Anwendungen ordnen jeder Textur im Satz der aktuellen Texturen eine Mischungsphase zu. Direct3D wertet jede Mischungsphase in der reihenfolge aus, beginnend mit der ersten Textur im Satz und endend mit der achten.

Direct3D wendet die Informationen aus jeder Textur im Satz der aktuellen Texturen auf die Füllphase an, die ihr zugeordnet ist. Anwendungen steuern, welche Informationen aus einer Texturphase durch Aufrufen von [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api)verwendet werden. Sie können separate Vorgänge für die Farb- und Alphakanäle festlegen, und jeder Vorgang verwendet zwei Argumente. Angeben von Farbkanalvorgängen mithilfe des D3DTSS \_ COLOROP-Phasenzustands; Angeben von Alphavorgängen mithilfe von D3DTSS \_ ALPHAOP. Beide Phasenzustände verwenden Werte aus dem [**D3DTEXTUREOP-Enumerationstyp.**](./d3dtextureop.md)

Texturmischungsargumente verwenden die Member D3DTSS \_ COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 und D3DTSS \_ ALPHARG2 des [**D3DTEXTURESTAGESTATETYPE-Enumerationstyps.**](./d3dtexturestagestatetype.md) Die entsprechenden Argumentwerte werden mithilfe von [D3DTA](d3dta.md)identifiziert.

> [!Note]  
> Sie können eine Texturphase und alle nachfolgenden Texturmischungsstufen in der Kaskadierung deaktivieren, indem Sie den Farbvorgang für diese Phase auf D3DTOP \_ DISABLE festlegen. Wenn Sie den Farbvorgang deaktivieren, wird auch der Alphavorgang deaktiviert. Alphavorgänge können nicht deaktiviert werden, wenn Farbvorgänge aktiviert sind. Das Festlegen des Alphavorgangs auf D3DTOP \_ DISABLE bei aktivierter Farbmischung führt zu nicht definiertem Verhalten.

 

Um die unterstützten Texturmischungsvorgänge eines Geräts zu bestimmen, fragen Sie den TextureCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturmischung](texture-blending.md)
</dt> </dl>

 

 
