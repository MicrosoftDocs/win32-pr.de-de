---
description: Wenn die Konstanten, Texturen und der Shader-Zustand deklariert und initialisiert sind, besteht die einzige Aufgabe darin, den Effekt Zustand im Gerät festzulegen.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Anwenden einer Technik (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7cc48c9115dfb81c1688a3a499e24d46cc563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483014"
---
# <a name="apply-a-technique-direct3d-10"></a>Anwenden einer Technik (Direct3D 10)

Wenn die Konstanten, Texturen und der Shader-Zustand deklariert und initialisiert sind, besteht die einzige Aufgabe darin, den Effekt Zustand im Gerät festzulegen.

## <a name="set-non-shader-state-in-the-device"></a>Festlegen des Zustands eines nicht-Shader im Gerät

Der Pipeline Zustand wird nicht durch einen Effekt festgelegt. Beispielsweise bereitet das Löschen eines Renderziels das Renderziel für Daten vor. Im folgenden finden Sie ein Beispiel für das Löschen von Ausgabe Puffern, bevor Sie den Effekt Zustand im Gerät festlegen.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Festlegen des Wirkungs Zustands im Gerät

Der Effekt Zustand wird durch Anwenden des Effekt Zustands innerhalb der Renderschleife festgelegt. Dies erfolgt von außerhalb von in. Das heißt, wählen Sie eine Technik aus, und legen Sie dann den Status für jeden der Durchläufen fest (je nach gewünschtem Ergebnis).


```
    D3D10_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



Ein Effekt führt nichts aus, sondern legt einfach den Effekt auf das Gerät fest. Der Renderingcode wird aufgerufen, nachdem der Status des Effekts den Gerätezustand aktualisiert hat. In diesem Beispiel führt der drawinentxed-Befehl das Rendering aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



