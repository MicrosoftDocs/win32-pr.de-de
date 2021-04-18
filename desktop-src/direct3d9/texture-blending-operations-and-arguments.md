---
description: Anwendungen ordnen jeder Textur im Satz der aktuellen Texturen eine Mischungs Stufe zu. Direct3D wertet jede Mischungs Phase in der Reihenfolge aus, beginnend mit der ersten Textur in der Menge und endet mit der achten.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Textur Mischungs Vorgänge und Argumente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344178"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a>Textur Mischungs Vorgänge und Argumente (Direct3D 9)

Anwendungen ordnen jeder Textur im Satz der aktuellen Texturen eine Mischungs Stufe zu. Direct3D wertet jede Mischungs Phase in der Reihenfolge aus, beginnend mit der ersten Textur in der Menge und endet mit der achten.

Direct3D wendet die Informationen aus jeder Textur im Satz aktueller Texturen auf die zugeordnete Mischungs Phase an. Anwendungen steuern, welche Informationen aus einer Textur Phase durch Aufrufen von [**IDirect3DDevice9:: settexturestagestate**](/windows/desktop/api)verwendet werden. Sie können separate Vorgänge für die Farb-und Alphakanäle festlegen, und jeder Vorgang verwendet zwei Argumente. Angeben von farbchannelvorgängen mithilfe des D3DTSS \_ colorop-Phasen Zustands; angeben von Alpha-Vorgängen mithilfe von D3DTSS \_ alphaop. Beide Stufen Zustände verwenden Werte aus dem [**D3DTEXTUREOP**](./d3dtextureop.md) -Enumerationstyp.

Textur Mischungs Argumente verwenden die Member D3DTSS \_ COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 und D3DTSS ALPHARG2 \_ des [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerierten Typs. Die entsprechenden Argument Werte werden mithilfe von [D3DTA](d3dta.md)identifiziert.

> [!Note]  
> Sie können eine Textur Phase und alle nachfolgenden Textur Mischungs Stufen in der Cascade-Einstellung deaktivieren, indem Sie den Farb Vorgang für diese Phase auf D3DTOP \_ deaktivieren festlegen. Wenn Sie den Farb Vorgang deaktivieren, wird auch der Alpha-Vorgang deaktiviert. Alpha Vorgänge können nicht deaktiviert werden, wenn Farb Vorgänge aktiviert sind. Das Festlegen des Alpha-Vorgangs auf D3DTOP \_ deaktivieren, wenn die Farbmischung aktiviert ist, verursacht ein nicht definiertes Verhalten

 

Um die unterstützten Textur Mischungs Vorgänge eines Geräts zu bestimmen, Fragen Sie den TextureCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Mischung](texture-blending.md)
</dt> </dl>

 

 
