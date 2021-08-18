---
description: Wenn die Konstanten, Texturen und der Shaderzustand deklariert und initialisiert sind, müssen Sie nur noch den Effektzustand auf dem Gerät festlegen.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Anwenden einer Technik (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4c920cbc7323ba42f3b099688a962674e3f5c2305746df7a56d1e158330919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128412"
---
# <a name="apply-a-technique-direct3d-10"></a>Anwenden einer Technik (Direct3D 10)

Wenn die Konstanten, Texturen und der Shaderzustand deklariert und initialisiert sind, müssen Sie nur noch den Effektzustand auf dem Gerät festlegen.

## <a name="set-non-shader-state-in-the-device"></a>Festlegen des Zustands ohne Shader auf dem Gerät

Ein Pipelinezustand wird nicht durch einen Effekt festgelegt. Wenn Sie beispielsweise ein Renderziel löschen, wird das Renderziel auf Daten vorbereitet. Vor dem Festlegen des Effektzustands auf dem Gerät finden Sie hier ein Beispiel für das Löschen von Ausgabepuffern.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Festlegen des Effektzustands auf dem Gerät

Das Festlegen des Effektzustands erfolgt durch Anwenden des Effektzustands innerhalb der Renderschleife. Dies erfolgt von außen in . Das heißt, wählen Sie eine Technik aus, und legen Sie dann den Zustand für jeden der Durchläufe fest (je nach gewünschtem Ergebnis).


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



Ein Effekt rendert nichts, sondern legt einfach den Effektzustand auf das Gerät fest. Der Renderingcode wird aufgerufen, nachdem der Auswirkungsstatus den Gerätezustand aktualisiert hat. In diesem Beispiel führt der DrawIndexed-Aufruf das Rendering aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



