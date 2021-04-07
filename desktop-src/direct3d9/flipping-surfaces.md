---
description: In einer Direct3D-Anwendung wird in der Regel eine animierte Sequenz angezeigt, indem die Rahmen der Animation in backpuffern erstellt und nacheinander dargestellt werden.
ms.assetid: 4ca9a845-f433-4d4a-939e-4b9ab2983927
title: Flipping-Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dafd263de0f907b33ff6f20ffcbb2cce69943da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746865"
---
# <a name="flipping-surfaces-direct3d-9"></a>Flipping-Oberflächen (Direct3D 9)

In einer Direct3D-Anwendung wird in der Regel eine animierte Sequenz angezeigt, indem die Rahmen der Animation in backpuffern erstellt und nacheinander dargestellt werden. Backpuffer werden in Austausch Ketten organisiert. Eine austauschkette ist eine Reihe von Puffern, die nacheinander auf den Bildschirm kippen. Dies kann verwendet werden, um eine Szene im Speicher zu rendern und die Szene nach Abschluss des Renderings auf den Bildschirm zu kippen. Dadurch wird das als "zerreißen" bezeichnete Phänomen vermieden und eine reibungslosere Animation ermöglicht.

Jedes in Direct3D erstellte Gerät weist mindestens eine SwapChain auf. Wenn Sie das erste Direct3D-Gerät initialisieren, legen Sie das BackBufferCount-Element der [**D3DPRESENT- \_ Parameter**](d3dpresent-parameters.md)fest, das Direct3D die Anzahl der Back Puffer angibt, die in der SwapChain sein werden. Durch den Aufrufen von [**IDirect3D9:: kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) werden dann das Direct3D-Gerät und die zugehörige austauschkette erstellt.

Bei Verwendung von [**IDirect3DDevice9::P erneut gesendet**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) , um einen Surface-Flip-Vorgang anzufordern, werden die Zeiger auf den Speicherplatz für den Vorder-und den Hintergrund Puffer vertauscht. Das Kippen erfolgt durch das Wechseln von Zeigern, die das Anzeigegerät für den Verweis auf den Speicher verwendet, nicht durch Kopieren von Oberflächen Arbeitsspeicher. Wenn eine flippingkette einen Vorder-und mehr als einen Hintergrund Puffer enthält, werden die Zeiger in einem Zirkel Muster umgeschaltet, wie im folgenden Diagramm dargestellt.

![Diagramm einer flippingkette mit einem Vorder-und zwei hinteren Puffern](images/trplflip.png)

Sie können durch Aufrufen von [**IDirect3DDevice9:: createadditionalswapchain**](/windows/desktop/api)Additions Austausch Ketten für ein Gerät erstellen. Eine Anwendung kann eine Austausch Kette pro Ansicht erstellen und jede Swapkette einem bestimmten Fenster zuordnen. Die Anwendung rendert Bilder in den backpuffern jeder SwapChain und zeigt Sie dann einzeln an. Die zwei Parameter, die **IDirect3DDevice9:: kreateadditionalswapchain** annimmt, sind ein Zeiger auf eine [**D3DPRESENT- \_ Parameter**](d3dpresent-parameters.md) Struktur und die Adresse eines Zeigers auf eine [**IDirect3DSwapChain9**](/windows/desktop/api) -Schnittstelle. Anschließend können Sie [**IDirect3DSwapChain9::P Resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) verwenden, um den Inhalt des nächsten hinterpuffers für den Frontpuffer anzuzeigen. Beachten Sie, dass ein Gerät nur über eine voll Bildaustausch Kette verfügen kann.

Sie erhalten Zugriff auf einen bestimmten Back Puffer, indem Sie die [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) -Methode oder die [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/desktop/api) -Methode aufrufen, die einen Zeiger auf eine [**IDirect3DSurface9**](/windows/desktop/api) -Schnittstelle zurückgibt, die die zurückgegebene Hintergrund Puffer Oberfläche darstellt. Beachten Sie, dass das Aufrufen dieser Methode den internen Verweis Zähler in der [**IDirect3DDevice9**](/windows/desktop/api) -Schnittstelle erhöht. Achten Sie daher darauf, [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) aufzurufen, wenn Sie die Verwendung dieser Oberfläche abgeschlossen haben oder wenn Sie einen Speicherplatz haben.

Beachten Sie, dass Direct3D kippt-Oberflächen durch Austauschen von Oberflächen Speicher Zeigern innerhalb der Austausch Kette, nicht durch Austauschen der Oberflächen selbst. Dies bedeutet, dass Sie immer in den Hintergrund Puffer Rendering werden, der als nächstes angezeigt wird.

Es ist wichtig, den Unterschied zwischen einem "flippingvorgang" zu beachten, wie er von einem Anzeige Adapter Treiber ausgeführt wird, und einem "Present"-Vorgang, der auf eine mit D3DSWAPEFFECT Flip erstellte Austausch Kette angewendet wird \_ .

Der Begriff "Kippen" bezeichnet einen Vorgang, durch den der Bereich der Videospeicher Adressen geändert wird, der von einem Anzeige Adapter verwendet wird, um sein Ausgabesignal zu generieren, wodurch der Inhalt eines zuvor ausgeblendeten Hintergrund Puffers angezeigt wird. In Direct3D 9 wird der Begriff häufig allgemeiner verwendet, um die Darstellung eines Hintergrund Puffers in jeder SwapChain zu beschreiben, die mit dem D3DSWAPEFFECT Flip-Swap-Effekt erstellt wurde \_ .

Obwohl solche "Present"-Vorgänge fast ausnahmslos von Flip-Vorgängen implementiert werden, wenn die SwapChain ein voll Bildschirm ist, werden Sie notwendigerweise von Kopier Vorgängen implementiert, wenn die SwapChain angezeigt wird. Darüber hinaus kann ein Anzeige Adapter Treiber das Kippen verwenden, um vorhandene Vorgänge für Vollbild-Swapketten basierend auf den D3DSWAPEFFECT \_ DISCARD-und D3DSWAPEFFECT-Kopien zu implementieren \_ .

Die obige Erörterung gilt für den häufig verwendeten Fall einer mit D3DSWAPEFFECT Flip erstellten Vollbild-SwapChain \_ .

Eine allgemeinere Erläuterung der unterschiedlichen Auslagerungs Effekte für Fenster-und voll Bildaustausch Ketten finden Sie unter [**D3DSWAPEFFECT**](./d3dswapeffect.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 
