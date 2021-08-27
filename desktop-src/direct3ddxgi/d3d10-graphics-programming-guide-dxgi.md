---
description: 'Dieses Thema enthält folgende Abschnitte:'
ms.assetid: 0522ccbf-e754-470a-8199-004fcbaa927d
title: DXGI – Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 604787a1b3f747b9d33cc04e249128aede7b7a3e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626136"
---
# <a name="dxgi-overview"></a>DXGI – Übersicht

Microsoft DirectX Graphic Infrastructure (DXGI) erkennt, dass einige Teile von Grafiken langsamer weiterentwickelt werden als andere. Das Hauptziel von DXGI ist die Verwaltung von Aufgaben auf niedriger Ebene, die unabhängig von der DirectX-Grafikruntime sein können. DXGI stellt ein allgemeines Framework für zukünftige Grafikkomponenten bereit. Die erste Komponente, die DXGI nutzt, ist Microsoft Direct3D 10.

In früheren Versionen von Direct3D wurden in der Direct3D-Runtime Low-Level-Aufgaben wie das Aufzählen von Hardwaregeräten, das Darstellen von gerenderten Frames in einer Ausgabe, das Steuern von Gamma und das Verwalten eines Vollbildübergangs einbezogen. Diese Aufgaben werden jetzt in DXGI implementiert.

DXGI dient der Kommunikation mit dem Kernelmodustreiber und der Systemhardware, wie im folgenden Diagramm dargestellt.

![Diagramm der Kommunikation zwischen Anwendungen, Dxgi und Treibern und Hardware](images/dxgi-dll.png)

Eine Anwendung kann direkt auf DXGI zugreifen oder die Direct3D-APIs in D3D11 \_ 1.h, D3D11.h, D3D10 \_ 1.h oder D3D10.h aufrufen, die die Kommunikation mit DXGI für Sie übernimmt. Sie können direkt mit DXGI arbeiten, wenn Ihre Anwendung Geräte aufzählen oder steuern muss, wie Daten in einer Ausgabe angezeigt werden.

Dieses Thema enthält folgende Abschnitte:

-   [Aufzählen von Adaptern](#enumerating-adapters)
    -   [Neue Informationen zum Aufzählen von Adaptern für Windows 8](#new-info-about-enumerating-adapters-for-windows-8)
-   [Präsentation](#presentation)
    -   [Erstellen einer Swapkette](#create-a-swap-chain)
    -   [Pflege und Einspeisung der Swapkette](#care-and-feeding-of-the-swap-chain)
    -   [Behandeln der Größenänderung von Fenstern](#handling-window-resizing)
    -   [Auswählen der DXGI-Ausgabe und -Größe](#choosing-the-dxgi-output-and-size)
    -   [Debuggen im Full-Screen Modus](#debugging-in-full-screen-mode)
    -   [Zerstören einer Swapkette](#destroying-a-swap-chain)
    -   [Verwenden eines gedrehten Monitors](#using-a-rotated-monitor)
    -   [Wechseln von Modi](#switching-modes)
    -   [Vollbild-Leistungstipp](#full-screen-performance-tip)
    -   [Überlegungen zu Multithreads](#multithread-considerations)
-   [DXGI Responses from DLLMain](#dxgi-responses-from-dllmain)
-   [DXGI 1.1 Changes](#dxgi-11-changes)
-   [DXGI 1.2 Changes](#dxgi-12-changes)
-   [Zugehörige Themen](#related-topics)

So sehen Sie, welche Formate von Direct3D 11-Hardware unterstützt werden:

-   [DXGI-Formatunterstützung für Direct3D Feature Level 12.1-Hardware](hardware-support-for-direct3d-12-1-formats.md)
-   [DXGI-Formatunterstützung für Direct3D Feature Level 12.0-Hardware](hardware-support-for-direct3d-12-0-formats.md)
-   [DXGI-Formatunterstützung für Direct3D Feature Level 11.1-Hardware](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [DXGI-Formatunterstützung für Direct3D Feature Level 11.0-Hardware](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Hardwareunterstützung für Direct3D 10Level9-Formate](/previous-versions//ff471324(v=vs.85))
-   [Hardwareunterstützung für Direct3D 10.1-Formate](/previous-versions//cc627091(v=vs.85))
-   [Hardwareunterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))

## <a name="enumerating-adapters"></a>Aufzählen von Adaptern

Ein Adapter ist eine Abstraktion der Hardware- und Softwarefunktion Ihres Computers. Es gibt im Allgemeinen viele Adapter auf Ihrem Computer. Einige Geräte werden in Hardware (z. B. Ihre Grafikkarte) und andere in Software implementiert (z. B. der Direct3D-Referenzrasterizer). Adapter implementieren funktionen, die von einer grafischen Anwendung verwendet werden. Das folgende Diagramm zeigt ein System mit einem einzelnen Computer, zwei Adaptern (Grafikkarten) und drei Ausgabemonitoren.

![Diagramm eines Computers mit zwei Grafikkarten und drei Monitoren](images/dxgi-terms.png)

Beim Aufzählen dieser Hardwarekomponenten erstellt DXGI eine [**IDXGIOutput1-Schnittstelle**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) für jede Ausgabe (oder jeden Monitor) und eine [**IDXGIAdapter2-Schnittstelle**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2) für jede Grafikkarte (auch wenn es sich um eine in eine Hauptplatine integrierte Grafikkarte handelt). Die Enumeration erfolgt mithilfe eines [**IDXGIFactory-Schnittstellenaufrufs,**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) [**IDXGIFactory::EnumAdapters,**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-enumadapters)um einen Satz von [**IDXGIAdapter-Schnittstellen**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) zurückzugeben, die die Videohardware darstellen.

DXGI 1.1 hat die [**IDXGIFactory1-Schnittstelle**](/windows/win32/api/DXGI/nn-dxgi-idxgifactory1) hinzugefügt. [**IDXGIFactory1::EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) gibt einen Satz von [**IDXGIAdapter1-Schnittstellen**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter1) zurück, die die Videohardware darstellen.

Wenn Sie bestimmte Videohardwarefunktionen auswählen möchten, wenn Sie Direct3D-APIs verwenden, wird empfohlen, die [**Funktion D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) mit jedem Adapterhandle und der möglichen [Hardwarefunktionsebene](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)iterativ aufzurufen. Diese Funktion ist erfolgreich, wenn die Funktionsebene vom angegebenen Adapter unterstützt wird.

### <a name="new-info-about-enumerating-adapters-for-windows-8"></a>Neue Informationen zum Aufzählen von Adaptern für Windows 8

Ab Windows 8 ist immer ein Adapter namens "Microsoft Basic Render Driver" vorhanden. Dieser Adapter verfügt über die VendorId **0x1414** und die DeviceID **0x8c**. Für diesen Adapter ist auch der [**DXGI \_ ADAPTER FLAG \_ \_ SOFTWARE-Wert**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) im **Flags-Member** der [**DXGI ADAPTER \_ \_ DESC2-Struktur**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_adapter_desc2) festgelegt. Dieser Adapter ist ein rein renderbasiertes Gerät ohne Anzeigeausgaben. DXGI gibt für diesen Adapter nie [**DXGI \_ ERROR DEVICE \_ REMOVED \_ zurück.**](dxgi-error.md)

Wenn der Anzeigetreiber eines Computers nicht funktioniert oder deaktiviert ist, wird der primäre Adapter **(NULL)** des Computers möglicherweise auch als "Microsoft Basic-Rendertreiber" bezeichnet. Dieser Adapter verfügt jedoch über Ausgaben, und der [**DXGI \_ ADAPTER FLAG \_ \_ SOFTWARE-Wert**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) ist nicht festgelegt. Das Betriebssystem und die Apps verwenden diesen Adapter standardmäßig. Wenn ein Anzeigetreiber installiert oder aktiviert ist, können Apps [**DXGI \_ ERROR DEVICE \_ \_ REMOVED**](dxgi-error.md) für diesen Adapter empfangen und müssen adapters dann erneut aufzählen.

Wenn der primäre Anzeigeadapter eines Computers der "Microsoft Basic Display Adapter"[(WARP-Adapter)](../direct3d11/overviews-direct3d-11-devices-create-warp.md) ist, verfügt dieser Computer auch über einen zweiten Adapter. Dieser zweite Adapter ist das rein renderbasierte Gerät, das keine Anzeigeausgaben aufweist und für das DXGI nie [**DXGI \_ ERROR DEVICE \_ \_ REMOVED**](dxgi-error.md)zurückgibt.

Wenn Sie WARP für Rendering-, Compute- oder andere Aufgaben mit langer Ausführungslaufzeit verwenden möchten, empfehlen wir die Verwendung des reinen Rendergeräts. Sie können einen Zeiger auf das Nur-Render-Gerät abrufen, indem Sie die [**IDXGIFactory1::EnumAdapters1-Methode**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) aufrufen. Sie erstellen auch das Nur-Render-Gerät, wenn Sie [**D3D \_ DRIVER \_ TYPE \_ WARP**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type) im *DriverType-Parameter* von [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) angeben, da das WARP-Gerät auch den warp-Adapter nur rendert.

## <a name="presentation"></a>Präsentation

Die Aufgabe Ihrer Anwendung besteht darin, Frames zu rendern und DXGI aufzufordern, diese Frames in der Ausgabe darzustellen. Wenn die Anwendung über zwei verfügbare Puffer verfügt, kann sie einen Puffer rendern und einen anderen darstellen. Abhängig von der Zeit, die zum Rendern eines Frames benötigt wird, oder der gewünschten Bildfrequenz für die Präsentation benötigt die Anwendung möglicherweise mehr als zwei Puffer. Der erstellte Puffersatz wird wie hier gezeigt als Swapkette bezeichnet.

![Abbildung einer Swapkette](images/dxgi-swap-chain.png)

-   [Erstellen einer Swapkette](#create-a-swap-chain)
-   [Pflege und Einspeisung der Swapkette](#care-and-feeding-of-the-swap-chain)
-   [Behandeln der Größenänderung von Fenstern](#handling-window-resizing)
-   [Auswählen der DXGI-Ausgabe und -Größe](#choosing-the-dxgi-output-and-size)
-   [Debuggen im Full-Screen Modus](#debugging-in-full-screen-mode)
-   [Zerstören einer Swapkette](#destroying-a-swap-chain)
-   [Verwenden eines gedrehten Monitors](#using-a-rotated-monitor)
-   [Wechseln von Modi](#switching-modes)
-   [Vollbild-Leistungstipp](#full-screen-performance-tip)
-   [Überlegungen zu Multithreads](#multithread-considerations)

Eine Swapkette verfügt über einen Frontpuffer und mindestens einen Backpuffer. Jede Anwendung erstellt eine eigene Swapkette. Um die Geschwindigkeit der Darstellung der Daten in einer Ausgabe zu maximieren, wird fast immer eine Swapkette im Speicher eines Anzeigeuntersystems erstellt, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Anzeigeuntersystems](images/dxgi-adapter.png)

Das Anzeigeuntersystem (das häufig eine Grafikkarte ist, aber auf einer Hauptplatine implementiert werden kann) enthält eine GPU, einen Digital-to-Analog-Konverter (Digital to Analog Converter, DAC) und Arbeitsspeicher. Die Swapkette wird innerhalb dieses Arbeitsspeichers zugeordnet, um die Präsentation sehr schnell zu gestalten. Das Anzeigeuntersystem stellt die Daten im Frontpuffer für die Ausgabe dar.

Eine Auslagerungskette ist so eingerichtet, dass sie im Vollbild- oder Fenstermodus gezeichnet wird. Dies macht es überflüssig, zu wissen, ob eine Ausgabe im Vollbildmodus oder im Vollbildmodus angezeigt wird. Eine Auslagerungskette im Vollbildmodus kann die Leistung optimieren, indem die Anzeigeauflösung gewechselt wird.

### <a name="create-a-swap-chain"></a>Erstellen einer Swapchain

<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10: Direct3D 10 ist die erste Grafikkomponente, die DXGI verwendet. DXGI weist einige unterschiedliche Swap chain-Verhaltensweisen auf.<br/>
<ul>
<li>In DXGI ist eine Swapkette an ein Fenster gebunden, wenn die Swapkette erstellt wird. Diese Änderung verbessert die Leistung und spart Arbeitsspeicher. In früheren Versionen von Direct3D konnte die Swapkette das Fenster ändern, an das die Austauschkette gebunden ist.</li>
<li>In DXGI ist eine Swapkette bei der Erstellung an ein Renderinggerät gebunden. Das Geräteobjekt, das die Direct3D-Gerätefunktionen zurückgeben, implementiert die <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown-Schnittstelle.</strong></a> Sie können <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> aufrufen, um die entsprechende <a href="/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgidevice2"><strong>IDXGIDevice2-Schnittstelle</strong></a> des Geräts abzufragen. Eine Änderung am Renderinggerät erfordert, dass die Austauschkette neu erstellt wird.</li>
<li><p>In DXGI sind die verfügbaren Swapeffekte DXGI_SWAP_EFFECT_DISCARD und DXGI_SWAP_EFFECT_SEQUENTIAL. Ab Windows 8 ist auch DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL Austauscheffekt verfügbar. Die folgende Tabelle zeigt eine Zuordnung von Direct3D 9 zu DXGI swap effect defines. </p>
<table>
<thead>
<tr class="header">
<th>D3D9 Swap Effect</th>
<th>DXGI Swap Effect</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DSWAPEFFECT_DISCARD</td>
<td>DXGI_SWAP_EFFECT_DISCARD</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_COPY</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL mit 1 Puffer</td>
</tr>
<tr class="odd">
<td>D3DSWAPEFFECT_FLIP</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL mit 2 oder mehr Puffern</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_FLIPEX</td>
<td>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL mit 2 oder mehr Puffern</td>
</tr>
</tbody>
</table>
<p></p>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



 

Die Puffer einer Austauschkette werden in einer bestimmten Größe und in einem bestimmten Format erstellt. Die Anwendung gibt diese Werte beim Start an (oder Sie können die Größe vom Zielfenster erben) und kann sie dann optional ändern, wenn sich die Fenstergröße als Reaktion auf Benutzereingabe- oder Programmereignisse ändert.

Nachdem Sie die Auslagerungskette erstellt haben, möchten Sie in der Regel Bilder in die Kette rendern. Hier sehen Sie ein Codefragment, das einen Direct3D-Kontext zum Rendern in einer Austauschkette ein richtet. Dieser Code extrahiert einen Puffer aus der Auslagerungskette, erstellt eine Renderzielansicht aus diesem Puffer und legt ihn dann auf dem Gerät fest:


```
ID3D11Resource * pBB;
ThrowFailure( pSwapChain->GetBuffer(0, __uuidof(pBB),    
  reinterpret_cast<void**>(&pBB)), "Couldn't get back buffer");
ID3D11RenderTargetView * pView;
ThrowFailure( pD3D11Device->CreateRenderTargetView(pBB, NULL, &pView), 
  "Couldn't create view" );
pD3D11DeviceContext->OMSetRenderTargets(1, &pView, 0);
        
```



Nachdem Ihre Anwendung einen Frame in einen Swap-Chain-Puffer gerendert hat, rufen Sie [**IDXGISwapChain1::P resent1 auf.**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) Die Anwendung kann dann das nächste Bild rendern.

### <a name="care-and-feeding-of-the-swap-chain"></a>Pflege und Einführung der Austauschkette

Rufen Sie nach dem Rendern Ihres [**Bilds IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) auf, und rendern Sie das nächste Bild. Dies ist der Umfang Ihrer Verantwortung.

Wenn Sie zuvor [**IDXGIFactory::MakeWindowAssociation**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation)aufgerufen haben, kann der Benutzer die Tastenkombination Alt-Enter drücken, und DXGI überwechselt Ihre Anwendung zwischen dem Fenstermodus und dem Vollbildmodus. **IDXGIFactory::MakeWindowAssociation** wird empfohlen, da ein Standardkontrollmechanismus für den Benutzer dringend gewünscht ist.

Sie müssen zwar nicht mehr Code schreiben, als beschrieben wurde, aber mit einigen einfachen Schritten kann Ihre Anwendung reaktionsfähiger werden. Der wichtigste Aspekt ist die Größenvergrößerung der Puffer der Austauschkette als Reaktion auf die Größenvergrößerung des Ausgabefensters. Die beste Route der Anwendung besteht natürlich darin, auf WM SIZE zu reagieren und \_ [**IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers)aufrufen und dabei die in den Parametern der Nachricht enthaltene Größe zu übergeben. Dieses Verhalten sorgt natürlich dafür, dass Ihre Anwendung gut auf den Benutzer reagiert, wenn er die Rahmen des Fensters zieht, aber es ist auch genau das, was einen reibungslosen Vollbildübergang ermöglicht. Ihr Fenster erhält immer dann eine WM SIZE-Nachricht, wenn ein solcher Übergang erfolgt, und der Aufruf von \_ **IDXGISwapChain::ResizeBuffers** ist die Chance der Swapkette, den Pufferspeicher für eine optimale Darstellung neu zu ordnen. Aus diesem Grund muss die Anwendung verweise auf die vorhandenen Puffer vor dem Aufruf von **IDXGISwapChain::ResizeBuffers frei geben.**

Wenn [**IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) nicht als Reaktion auf den Wechsel in den Vollbildmodus (am natürlichsten als Reaktion auf WM SIZE) aufgerufen werden kann, kann die Optimierung des Flippings verhindert werden, wobei DXGI einfach den angezeigten Puffer austauschen kann, anstatt die Daten eines Vollbildbilds zu \_ kopieren.

[**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) informiert Sie, wenn Ihr Ausgabefenster vollständig über **DXGI \_ STATUS \_ OCCLUDED verblendet ist.** In diesem Fall wird empfohlen, dass Ihre Anwendung in den Standbymodus versetzt wird (durch Aufrufen von **IDXGISwapChain1::P resent1** mit **DXGI \_ PRESENT \_ TEST),** da Ressourcen, die zum Rendern des Frames verwendet werden, verschwendet werden. Die **Verwendung von DXGI PRESENT \_ \_ TEST** verhindert, dass Daten angezeigt werden, während die Okklusionsprüfung noch durchgeführt wird. Sobald **IDXGISwapChain1::P resent1** S OK zurückgibt, sollten Sie den Standbymodus beenden. Verwenden Sie nicht den Rückgabecode, um in den Standbymodus zu wechseln, da dies dazu führen kann, dass die Swapkette den Vollbildmodus nicht verlassen \_ kann.

Die Direct3D 11.1-Runtime, die ab Windows 8 verfügbar ist, bietet eine Austauschkette für flip-model (d. h. eine Swapkette, bei der [**der DXGI \_ SWAP EFFECT \_ FLIP \_ \_ SEQUENTIAL-Wert**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) im **SwapEffect-Member** von [**DXGI SWAP CHAIN \_ \_ \_ DESC**](/windows/win32/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) oder [**DXGI SWAP CHAIN \_ \_ \_ DESC1 festgelegt ist).**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Wenn Sie Frames für eine Ausgabe mit einer Flip-Model-Swap-Kette präsentieren, entbinden DXGI den Hintergrundpuffer von allen Pipelinezustandsspeicherorten, z. B. einem Ausgabe-Merger-Renderziel, das in den Hintergrundpuffer 0 schreibt. Daher wird empfohlen, [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets) unmittelbar vor dem Rendern in den Hintergrundpuffer aufrufen. Rufen Sie beispielsweise nicht **OMSetRenderTargets** auf, und führen Sie dann Compute-Shader-Aufgaben aus, die nicht zum Rendern an die Ressource führen. Weitere Informationen zu Flip-Model-Austauschketten und ihren Vorteilen finden Sie unter [DXGI Flip Model](dxgi-flip-model.md).

> [!NOTE]  
> In Direct3D 10 und Direct3D 11 müssen Sie [**IDXGISwapChain::GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) nicht aufrufen, um den Puffer 0 abzurufen, nachdem Sie [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) aufgerufen haben, da sich die Identitäten der Hintergrundpuffer der Einfachheit halber ändern. Dies geschieht nicht in Direct3D 12, und Ihre Anwendung muss stattdessen Pufferindizes manuell nachverfolgen.

### <a name="handling-window-resizing"></a>Behandeln der Größenver ändern des Fensters

Sie können die [**IDXGISwapChain::ResizeBuffers-Methode**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) verwenden, um die Fenstergröße zu ändern. Bevor Sie **ResizeBuffers aufrufen,** müssen Sie alle ausstehenden Verweise auf die Puffer der Austauschkette frei geben. Das Objekt, das in der Regel einen Verweis auf den Puffer einer Austauschkette enthält, ist eine Renderzielansicht.

Der folgende Beispielcode zeigt, wie [**ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) innerhalb des WindowProc-Handlers für WM \_ SIZE-Meldungen aufgerufen wird:


```
    case WM_SIZE:
        if (g_pSwapChain)
        {
            g_pd3dDeviceContext->OMSetRenderTargets(0, 0, 0);

            // Release all outstanding references to the swap chain's buffers.
            g_pRenderTargetView->Release();

            HRESULT hr;
            // Preserve the existing buffer count and format.
            // Automatically choose the width and height to match the client rect for HWNDs.
            hr = g_pSwapChain->ResizeBuffers(0, 0, 0, DXGI_FORMAT_UNKNOWN, 0);
                                            
            // Perform error handling here!

            // Get buffer and create a render-target-view.
            ID3D11Texture2D* pBuffer;
            hr = g_pSwapChain->GetBuffer(0, __uuidof( ID3D11Texture2D),
                                         (void**) &pBuffer );
            // Perform error handling here!

            hr = g_pd3dDevice->CreateRenderTargetView(pBuffer, NULL,
                                                     &g_pRenderTargetView);
            // Perform error handling here!
            pBuffer->Release();

            g_pd3dDeviceContext->OMSetRenderTargets(1, &g_pRenderTargetView, NULL );

            // Set up the viewport.
            D3D11_VIEWPORT vp;
            vp.Width = width;
            vp.Height = height;
            vp.MinDepth = 0.0f;
            vp.MaxDepth = 1.0f;
            vp.TopLeftX = 0;
            vp.TopLeftY = 0;
            g_pd3dDeviceContext->RSSetViewports( 1, &vp );
        }
        return 1;
```



### <a name="choosing-the-dxgi-output-and-size"></a>Auswählen der DXGI-Ausgabe und -Größe

Standardmäßig wählt DXGI die Ausgabe aus, die den Großteil des Clientbereichs des Fensters enthält. Dies ist die einzige Option, die DXGI als Reaktion auf die EINGABETASTE im Vollbildmodus zur Verfügung steht. Wenn die Anwendung sich dafür entscheidet, selbst in den Vollbildmodus zu wechseln, kann sie [**IDXGISwapChain::SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) aufrufen und eine explizite [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) (oder **NULL)** übergeben, wenn die Anwendung DXGI gerne entscheiden lässt).

Um die Größe der Ausgabe entweder im Vollbildmodus oder im Fenster zu ändern, wird empfohlen, [**IDXGISwapChain::ResizeTarget**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget)auf aufruft, da diese Methode auch die Größe des Zielfensters geändert. Da die Größe des Zielfensters geändert wird, sendet das Betriebssystem **WM \_ SIZE,** und Ihr Code wird [**idXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) als Antwort natürlich aufrufen. Daher ist es eine Verschwendung von Aufwand, die Größe Ihrer Puffer zu ändern und anschließend die Größe des Ziels zu ändern.

### <a name="debugging-in-full-screen-mode"></a>Debuggen im Vollbildmodus

Eine DXGI-Swapkette gibt den Vollbildmodus nur dann auf, wenn dies unbedingt erforderlich ist. Dies bedeutet, dass Sie eine Vollbildanwendung mit mehreren Monitoren debuggen können, solange das Debugfenster das Zielfenster der Swapkette nicht überlappt. Alternativ können Sie den Moduswechsel ganz verhindern, indem Sie das **DXGI \_ SWAP CHAIN FLAG ALLOW MODE \_ \_ \_ \_ \_ SWITCH-Flag nicht** festlegen.

Wenn der Moduswechsel zulässig ist, gibt eine Swapkette den Vollbildmodus auf, wenn das Ausgabefenster von einem anderen Fenster umschließet wird. Die Okklusionsprüfung wird während [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)oder durch einen separaten Thread durchgeführt, dessen Zweck es ist, zu überprüfen, ob die Anwendung nicht mehr reagiert (und nicht mehr **IDXGISwapChain1::P resent1) aufruft.** Um die Fähigkeit des separaten Threads zu deaktivieren, einen Schalter zu verursachen, legen Sie den folgenden Registrierungsschlüssel auf einen beliebigen Wert fest, der nicht 0 (null) ist.

**HKCU \\ Software \\ Microsoft \\ DXGI \\ DisableFullscreenWatchdog**

### <a name="destroying-a-swap-chain"></a>Zerstören einer Austauschkette

Sie können eine Swapkette im Vollbildmodus nicht veröffentlichen, da dies zu Thread-Problemen führen kann (was dazu führen kann, dass DXGI eine nicht kontinuierbare Ausnahme auslöst). Bevor Sie eine Swapkette freigeben, wechseln Sie zunächst in den Fenstermodus (mit [**IDXGISwapChain::SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)( **FALSE,** **NULL** )), und rufen Sie [**dann IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)auf.

### <a name="using-a-rotated-monitor"></a>Verwenden eines gedrehten Monitors

Eine Anwendung muss sich keine Gedanken über die Monitorausrichtung machen. DXGI rotiert bei Bedarf während der Präsentation einen Auslagerungskettenpuffer. Diese zusätzliche Drehung kann sich natürlich auf die Leistung auswirken. Führen Sie die folgenden Schritte aus, um eine optimale Leistung zu erzielen:

-   Verwenden Sie **das DXGI \_ SWAP CHAIN \_ FLAG \_ \_ NONPREROTATED**. Dadurch wird DXGI benachrichtigt, dass die Anwendung ein gedrehtes Bild erzeugt (z. B. durch Ändern der Projektionsmatrix). Beachten Sie, dass dieses Flag nur im Vollbildmodus gültig ist.
-   Ordnen Sie jeden Auslagerungskettenpuffer in seiner gedrehten Größe zu. Verwenden [**Sie IDXGIOutput::GetDesc,**](/windows/win32/api/DXGI/nf-dxgi-idxgioutput-getdesc) um diese Werte bei Bedarf zu erhalten.

Durch Ausführen der Drehung in Ihrer Anwendung wird von DXGI einfach eine Kopie statt einer Kopie und eine Drehung verwendet.

Die Direct3D 11.1-Runtime, die ab Windows 8 verfügbar ist, bietet eine Austauschkette für flip-model (d. h. eine Swapkette, bei der der [**DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL-Wert**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) im **SwapEffect-Member** von [**DXGI SWAP CHAIN \_ \_ \_ DESC1 festgelegt ist).**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Um die präsentationsoptimierungen zu maximieren, die mit einer Flip-Model-Swap-Kette verfügbar sind, empfehlen wir, dass Sie Ihre Anwendungen so ausrichten, dass sie den Inhalt an die bestimmte Ausgabe ausrichten, in der sich der Inhalt befindet, wenn dieser Inhalt die Ausgabe vollständig einnimmt. Weitere Informationen zu Flip-Model-Austauschketten und ihren Vorteilen finden Sie unter [DXGI Flip Model](dxgi-flip-model.md).

### <a name="switching-modes"></a>Wechseln von Modi

Die DXGI-Swapkette kann den Anzeigemodus einer Ausgabe ändern, wenn ein Vollbildübergang ausgeführt wird. Um die automatische Anzeigemodusänderung zu aktivieren, müssen Sie **DXGI \_ SWAP CHAIN FLAG ALLOW MODE \_ \_ \_ \_ \_ SWITCH** in der Beschreibung der Auslagerungskette angeben. Wenn sich der Anzeigemodus automatisch ändert, wählt DXGI den mäßigsten Modus aus (Größe und Auflösung ändern sich nicht, aber die Farbtiefe kann sich ändern). Das Ändern der Größe von Auslagerungskettenpuffern verursacht keinen Moduswechsel. Die Swapkette verspricht implizit, dass bei Auswahl eines Hintergrundpuffers, der genau mit dem von der Zielausgabe unterstützten Anzeigemodus abspricht, in diesen Anzeigemodus wechselt, wenn der Vollbildmodus für diese Ausgabe aktiviert wird. Folglich wählen Sie einen Anzeigemodus aus, indem Sie die Größe und das Format des Hintergrundpuffers auswählen.

### <a name="full-screen-performance-tip"></a>Leistungstipps im Vollbildmodus

Wenn Sie [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) in einer Vollbildanwendung aufrufen, wird der Inhalt des Hintergrundpuffers von der Swapkette in den Frontpuffer gekippt (im Gegensatz zu Blits). Dies erfordert, dass die Swapkette mithilfe eines aufzählten Anzeigemodus erstellt wurde (angegeben in [**DXGI \_ SWAP CHAIN \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Wenn Sie die Anzeigemodi nicht aufzählen oder den Anzeigemodus in der Beschreibung falsch angeben, führt die Auslagerungskette möglicherweise stattdessen eine Bitblockübertragung (bitblt) aus. Das Bitblt verursacht eine zusätzliche Stretchingkopie sowie eine erhöhte Videospeicherauslastung und ist schwer zu erkennen. Um dieses Problem zu vermeiden, aufzählen Sie Anzeigemodi, und initialisieren Sie die Beschreibung der Auslagerungskette ordnungsgemäß, bevor Sie die Swapkette erstellen. Dadurch wird die maximale Leistung beim Kippen im Vollbildmodus sichergestellt, und der zusätzliche Arbeitsspeicheraufwand wird vermieden.

### <a name="multithread-considerations"></a>Überlegungen zu Multithreads

Wenn Sie DXGI in einer Anwendung mit mehreren Threads verwenden, müssen Sie darauf achten, dass kein Deadlock erstellt wird, bei dem zwei verschiedene Threads aufeinander warten, um den Abschluss zu vermeiden. Es gibt zwei Situationen, in denen dies auftreten kann.

-   Der Renderingthread ist nicht der Message Pump-Thread.
-   Der Thread, der eine DXGI-API ausgeführt, ist nicht derselbe Thread, der das Fenster erstellt hat.

Achten Sie darauf, dass der Message Pump-Thread nie auf den Renderthread wartet, wenn Sie Vollbild-Auslagerungsketten verwenden. Beispielsweise kann der Aufruf von [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (aus dem Renderthread) dazu führen, dass der Renderthread auf den Message-Pump-Thread wartet. Wenn eine Modusänderung auftritt, ist dieses Szenario möglich, wenn **Present1** ::SetWindowPos() oder ::SetWindowStyle() aufruft und eine dieser Methoden ::SendMessage() aufruft. Wenn der Message-Pump-Thread in diesem Szenario über einen kritischen Abschnitt verfügt, der ihn schützt, oder wenn der Renderthread blockiert ist, werden die beiden Threads blockiert.

Weitere Informationen zur Verwendung von DXGI mit mehreren Threads finden Sie unter [Multithreading und DXGI.](../direct3d11/overviews-direct3d-11-render-multi-thread-intro.md)

## <a name="dxgi-responses-from-dllmain"></a>DXGI-Antworten von DLLMain

Da eine [**DllMain-Funktion**](../dlls/dllmain.md) die Reihenfolge des Ladens und Entladens von DLLs nicht garantieren kann, wird empfohlen, dass die **DllMain-Funktion** Ihrer App keine Direct3D- oder DXGI-Funktionen oder -Methoden aufruft, einschließlich Funktionen oder Methoden, die Objekte erstellen oder freigeben. Wenn die **DllMain-Funktion** Ihrer App eine bestimmte Komponente aufruft, ruft diese Komponente möglicherweise eine andere DLL auf, die nicht auf dem Betriebssystem vorhanden ist, wodurch das Betriebssystem abstürzt. Direct3D und DXGI laden möglicherweise eine Reihe von DLLs, in der Regel eine Gruppe von Treibern, die sich von Computer zu Computer unterscheiden. Selbst wenn Ihre App auf Ihren Entwicklungs- und Testcomputern nicht abstürzt, wenn ihre **DllMain-Funktion** Direct3D- oder DXGI-Funktionen oder -Methoden aufruft, stürzt sie möglicherweise ab, wenn sie auf einem anderen Computer ausgeführt wird.

Um zu verhindern, dass Sie eine App erstellen, die zum Absturz des Betriebssystems führen kann, stellt DXGI in den angegebenen Situationen die folgenden Antworten bereit:

-   Wenn die [**DllMain-Funktion**](../dlls/dllmain.md) Ihrer App den letzten Verweis auf eine DXGI-Factory freigibt, löst DXGI eine Ausnahme aus.
-   Wenn die [**DllMain-Funktion**](../dlls/dllmain.md) Ihrer App eine DXGI-Factory erstellt, gibt DXGI einen Fehlercode zurück.

## <a name="dxgi-11-changes"></a>DXGI 1.1-Änderungen

Wir haben die folgende Funktionalität in DXGI 1.1 hinzugefügt.

-   Unterstützung synchronisierter freigegebener Oberflächen

    Synchronisierte freigegebene Oberflächen für Direct3D 10.1 und Direct3D 11 ermöglichen eine effiziente Freigabe von Lese- und Schreiboberflächen zwischen mehreren Direct3D-Geräten (die Gemeinsame Nutzung zwischen Direct3D 10- und Direct3D 11-Geräten ist möglich). Siehe [**IDXGIKeyedMutex::AcquireSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-acquiresync) und [**IDXGIKeyedMutex::ReleaseSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-releasesync).

-   Unterstützung hoher Farben

    Unterstützt das DXGI \_ FORMAT \_ R10G10B10 \_ XR \_ BIAS \_ A2 \_ UNORM-Format.

-   [**IDXGIDevice1::SetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) und [ **IDXGIDevice1::GetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-getmaximumframelatency)
-   [**IDXGIFactory1::EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) listet lokale Adapter auf, ohne dass Monitore oder Ausgaben angefügt sind, sowie Adapter mit angefügten Ausgaben. Der erste zurückgegebene Adapter ist der lokale Adapter, auf dem der primäre Desktopadapter angezeigt wird.
-   Unterstützung des BGRA-Formats

    DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM und DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB finden Sie unter [**IDXGISurface1::GetDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-getdc) und [**IDXGISurface1::ReleaseDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-releasedc).

## <a name="dxgi-12-changes"></a>DXGI 1.2-Änderungen

Wir haben die folgende Funktionalität in DXGI 1.2 hinzugefügt.

-   Stereo-Swapkette
-   [Swapkette für Flip-Model](dxgi-flip-model.md)
-   Optimierte Darstellung (Scrollen, geänderte Rechtecke und Drehung)
-   Verbesserte freigegebene Ressourcen und Synchronisierung
-   [Desktopduplizierung](desktop-dup-api.md)
-   Optimierte Verwendung des Videospeichers
-   Unterstützung für BPP-Formate (16 Bits pro Pixel) (DXGI \_ FORMAT \_ B5G6R5 \_ UNORM, DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM, DXGI \_ FORMAT \_ B4G4R4A4 \_ UNORM)
-   Debuggen von APIs

Weitere Informationen zu DXGI 1.2 finden Sie unter [DXGI 1.2 Improvements](dxgi-1-2-improvements.md).

## <a name="related-topics"></a>Zugehörige Themen

[Programmierhandbuch für DXGI](dx-graphics-dxgi-overviews.md)
