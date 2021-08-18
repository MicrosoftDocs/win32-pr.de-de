---
description: Eine Direct3D-Anwendung zeigt in der Regel eine animierte Sequenz an, indem die Frames der Animation in Hintergrundpuffern generiert und nacheinander dargestellt werden.
ms.assetid: 4ca9a845-f433-4d4a-939e-4b9ab2983927
title: Flipping Surfaces (Direct3D 9) (Spiegeln von Oberflächen (Direct3D 9))
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c14aa7df63c3956d4974282033b44a7129853940d475b23115f9bca344ca4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988035"
---
# <a name="flipping-surfaces-direct3d-9"></a>Flipping Surfaces (Direct3D 9) (Spiegeln von Oberflächen (Direct3D 9))

Eine Direct3D-Anwendung zeigt in der Regel eine animierte Sequenz an, indem die Frames der Animation in Hintergrundpuffern generiert und nacheinander dargestellt werden. Hintergrundpuffer sind in Swapketten organisiert. Eine Swapkette ist eine Reihe von Puffern, die nacheinander auf den Bildschirm "blättern". Dies kann verwendet werden, um eine Szene im Arbeitsspeicher zu rendern und die Szene dann auf den Bildschirm zu drehen, wenn das Rendering abgeschlossen ist. Dadurch wird das als "Löschen" bezeichnete Problem vermieden und eine reibungslose Animation ermöglicht.

Jedes in Direct3D erstellte Gerät verfügt über mindestens eine Swapkette. Wenn Sie das erste Direct3D-Gerät initialisieren, legen Sie das BackBufferCount-Element von [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md)fest, das Direct3D die Anzahl der Backpuffer angibt, die sich in der Swapkette befindet. Der Aufruf von [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) erstellt dann das Direct3D-Gerät und die entsprechende Swapkette.

Wenn Sie [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) verwenden, um einen Surface Flip-Vorgang anzufordern, werden die Zeiger auf den Oberflächenspeicher für den Front- und Denkpuffer getauscht. Das Umschalten erfolgt durch Umschalten von Zeigern, die das Anzeigegerät zum Verweisen auf den Arbeitsspeicher verwendet, und nicht durch Kopieren des Oberflächenspeichers. Wenn eine Flippingkette einen Frontpuffer und mehr als einen Hintergrundpuffer enthält, werden die Zeiger in einem kreisförmigen Muster umgeschaltet, wie im folgenden Diagramm dargestellt.

![Diagramm einer Flippingkette mit einem Frontpuffer und zwei Hintergrundpuffern](images/trplflip.png)

Sie können zusätzliche Austauschketten für ein Gerät erstellen, indem Sie [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/desktop/api)aufrufen. Eine Anwendung kann eine Swapkette pro Ansicht erstellen und jede Swapkette einem bestimmten Fenster zuordnen. Die Anwendung rendert Bilder in den Hintergrundpuffern jeder Swapkette und stellt sie dann einzeln dar. Die beiden Parameter, die **IDirect3DDevice9::CreateAdditionalSwapChain** verwendet, sind ein Zeiger auf eine [**D3DPRESENT \_ PARAMETERS-Struktur**](d3dpresent-parameters.md) und die Adresse eines Zeigers auf eine [**IDirect3DSwapChain9-Schnittstelle.**](/windows/desktop/api) Anschließend können Sie [**IDirect3DSwapChain9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) verwenden, um den Inhalt des nächsten Backpuffers im Frontpuffer anzuzeigen. Beachten Sie, dass ein Gerät nur über eine Vollbild-Auslagerungskette verfügen kann.

Sie können Zugriff auf einen bestimmten Backpuffer erhalten, indem Sie die [**Methoden IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) oder [**IDirect3DSwapChain9::GetBackBuffer**](/windows/desktop/api) aufrufen, die einen Zeiger auf eine [**IDirect3DSurface9-Schnittstelle**](/windows/desktop/api) zurückgeben, die die zurückgegebene Pufferoberfläche darstellt. Beachten Sie, dass durch das Aufrufen dieser Methode der interne Verweiszähler für die [**IDirect3DDevice9-Schnittstelle**](/windows/desktop/api) erhöht wird. Rufen Sie daher [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) auf, wenn Sie mit dieser Oberfläche fertig sind oder ein Speicherverlust vorkommt.

Denken Sie daran, dass Direct3D Oberflächen durch Austauschen von Oberflächenspeicherzeigern innerhalb der Austauschkette und nicht durch Austauschen der Oberflächen selbst umtauscht. Dies bedeutet, dass Sie immer im Hintergrundpuffer rendern, der als Nächstes angezeigt wird.

Beachten Sie unbedingt den Unterschied zwischen einem "Flippingvorgang", der von einem Adaptertreiber für die Anzeige ausgeführt wird, und einem "Present"-Vorgang, der auf eine swap chain angewendet wird, die mit D3DSWAPEFFECT FLIP erstellt \_ wurde.

Der Begriff "Flip" bezeichnet konventionell einen Vorgang, der den Bereich der Videospeicheradressen ändert, den ein Adapter zum Generieren des Ausgabesignals verwendet, wodurch der Inhalt eines zuvor ausgeblendeten Hintergrundpuffers angezeigt wird. In Direct3D 9 wird der Begriff häufig allgemeiner verwendet, um die Darstellung eines Hintergrundpuffers in jeder Swapkette zu beschreiben, die mit dem Flip-Swap-Effekt D3DSWAPEFFECT erstellt \_ wurde.

Während solche "present"-Vorgänge nahezu ausweichend durch Flip-Vorgänge implementiert werden, wenn es sich bei der Swapkette um eine Vollbildkette handelt, werden sie notwendigerweise durch Kopiervorgänge implementiert, wenn die Swapkette eingeblendet wird. Darüber hinaus kann ein Anzeigeadaptertreiber Flipping verwenden, um Present-Vorgänge für Vollbild-Swapketten basierend auf D3DSWAPEFFECT \_ DISCARD und D3DSWAPEFFECT COPY zu \_ implementieren.

Die obige Erläuterung gilt für den häufig verwendeten Fall einer Vollbild-Swapkette, die mit D3DSWAPEFFECT FLIP erstellt \_ wurde.

Eine allgemeinere Erläuterung der verschiedenen Auslagerungseffekte für Fenster- und Vollbild-Swapketten finden Sie unter [**D3DSWAPEFFECT**](./d3dswapeffect.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 
