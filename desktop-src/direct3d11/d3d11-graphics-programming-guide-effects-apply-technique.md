---
title: Anwenden einer Technik (Direct3D 11)
description: Wenn die Konstanten, Texturen und der Shader-Zustand deklariert und initialisiert sind, besteht die einzige Aufgabe darin, den Effekt Zustand im Gerät festzulegen.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e67668b27c1f0271974f20edc62619a7b1ae8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037051"
---
# <a name="apply-a-technique-direct3d-11"></a>Anwenden einer Technik (Direct3D 11)

Wenn die Konstanten, Texturen und der Shader-Zustand deklariert und initialisiert sind, besteht die einzige Aufgabe darin, den Effekt Zustand im Gerät festzulegen.

## <a name="set-non-shader-state-in-the-device"></a>Festlegen des Zustands eines nicht-Shader im Gerät

Der Pipeline Zustand wird nicht durch einen Effekt festgelegt. Beispielsweise bereitet das Löschen eines Renderziels das Renderziel für Daten vor. Im folgenden finden Sie ein Beispiel für das Löschen von Ausgabe Puffern, bevor Sie den Effekt Zustand im Gerät festlegen.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Festlegen des Wirkungs Zustands im Gerät

Der Effekt Zustand wird durch Anwenden des Effekt Zustands innerhalb der Renderschleife festgelegt. Dies erfolgt von außerhalb von in. Das heißt, wählen Sie eine Technik aus, und legen Sie dann den Status für jeden der Durchläufen fest (je nach gewünschtem Ergebnis).


```
    D3D11_TECHNIQUE_DESC techDesc;
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

[Rendern eines Effekts (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




