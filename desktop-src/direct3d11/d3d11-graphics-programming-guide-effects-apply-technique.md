---
title: Anwenden einer Technik (Direct3D 11)
description: Erfahren Sie, wie Sie den Effektzustand auf dem Gerät für Direct3D 11 festlegen, nachdem die Konstanten, Texturen und Shaderstatus deklariert und initialisiert wurden.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d03f92957eaf1b3d501c0acd54aafde7e16d8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118945"
---
# <a name="apply-a-technique-direct3d-11"></a>Anwenden einer Technik (Direct3D 11)

Wenn die Konstanten, Texturen und der Shaderzustand deklariert und initialisiert sind, müssen Sie nur noch den Effektzustand auf dem Gerät festlegen.

## <a name="set-non-shader-state-in-the-device"></a>Festlegen des Zustands ohne Shader auf dem Gerät

Ein Pipelinezustand wird nicht durch einen Effekt festgelegt. Wenn Sie beispielsweise ein Renderziel löschen, wird das Renderziel auf Daten vorbereitet. Vor dem Festlegen des Effektzustands auf dem Gerät finden Sie hier ein Beispiel für das Löschen von Ausgabepuffern.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Festlegen des Effektzustands auf dem Gerät

Das Festlegen des Effektzustands erfolgt durch Anwenden des Effektzustands innerhalb der Renderschleife. Dies erfolgt von außen in . Das heißt, wählen Sie eine Technik aus, und legen Sie dann den Zustand für jeden der Durchläufe fest (je nach gewünschtem Ergebnis).


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



Ein Effekt rendert nichts, sondern legt einfach den Effektzustand auf das Gerät fest. Der Renderingcode wird aufgerufen, nachdem der Auswirkungsstatus den Gerätezustand aktualisiert hat. In diesem Beispiel führt der DrawIndexed-Aufruf das Rendering aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Effekts (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




