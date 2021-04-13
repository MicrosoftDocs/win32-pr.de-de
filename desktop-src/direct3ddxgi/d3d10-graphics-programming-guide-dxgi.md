---
description: 'Dieses Thema enthält folgende Abschnitte:'
ms.assetid: 0522ccbf-e754-470a-8199-004fcbaa927d
title: Übersicht über DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 324a5be26aade17385a6ab0b7d347015497a2a3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481086"
---
# <a name="dxgi-overview"></a>Übersicht über DXGI

Die Microsoft DirectX Graphics Infrastructure (DXGI) erkennt, dass sich einige Teile der Grafiken langsamer entwickeln als andere. Das primäre Ziel von DXGI ist das Verwalten von Aufgaben auf niedriger Ebene, die unabhängig von der DirectX-Grafik Laufzeit sein können. DXGI bietet ein gemeinsames Framework für zukünftige Grafik Komponenten. die erste Komponente, die DXGI nutzt, ist Microsoft Direct3D 10.

In früheren Versionen von Direct3D waren auf Low-Level-Aufgaben wie die Enumeration von Hardware Geräten, das darstellen von gerenderten Frames in einer Ausgabe, das Steuern von Gamma und das Verwalten eines voll Bild Übergangs in der Direct3D-Laufzeit enthalten. Diese Aufgaben sind nun in DXGI implementiert.

Der Zweck von DXGI besteht darin, mit dem Kernel Modus-Treiber und der System Hardware zu kommunizieren, wie im folgenden Diagramm dargestellt.

![Diagramm der Kommunikation zwischen Anwendungen, DXGI und Treibern und Hardware](images/dxgi-dll.png)

Eine Anwendung kann direkt auf DXGI zugreifen oder die Direct3D-APIs in D3D11 \_ 1. h, D3D11. h, d3d10 \_ 1. h oder d3d10. h aufrufen, die die Kommunikation mit DXGI für Sie verarbeiten. Möglicherweise möchten Sie DXGI direkt arbeiten, wenn Ihre Anwendung Geräte aufzählen oder Steuern soll, wie Daten in einer Ausgabe dargestellt werden.

Dieses Thema enthält folgende Abschnitte:

-   [Auflisten von Adaptern](#enumerating-adapters)
    -   [Neue Informationen zum Auflisten von Adaptern für Windows 8](#new-info-about-enumerating-adapters-for-windows-8)
-   [Präsentation](#presentation)
    -   [Austausch Kette erstellen](#create-a-swap-chain)
    -   [Pflege und Fütterung der SwapChain](#care-and-feeding-of-the-swap-chain)
    -   [Bearbeiten der Fenstergröße](#handling-window-resizing)
    -   [Auswählen der DXGI-Ausgabe und-Größe](#choosing-the-dxgi-output-and-size)
    -   [Debuggen im Full-Screen Modus](#debugging-in-full-screen-mode)
    -   [Zerstören einer austauschkette](#destroying-a-swap-chain)
    -   [Verwenden eines gedrehten Monitors](#using-a-rotated-monitor)
    -   [Wechsel Modi](#switching-modes)
    -   [Vollbild-Leistungs Tipp](#full-screen-performance-tip)
    -   [Überlegungen zum Multithread](#multithread-considerations)
-   [DXGI-Antworten von DllMain](#dxgi-responses-from-dllmain)
-   [DXGI 1,1-Änderungen](#dxgi-11-changes)
-   [DXGI 1,2-Änderungen](#dxgi-12-changes)
-   [Zugehörige Themen](#related-topics)

So sehen Sie, welche Formate von Direct3D 11-Hardware unterstützt werden:

-   [DXGI-Format Unterstützung für Direct3D Featureebene 12,1 Hardware](hardware-support-for-direct3d-12-1-formats.md)
-   [DXGI-Format Unterstützung für Direct3D Featureebene 12,0 Hardware](hardware-support-for-direct3d-12-0-formats.md)
-   [DXGI-Format Unterstützung für Direct3D Featureebene 11,1 Hardware](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [DXGI-Format Unterstützung für Direct3D Featureebene 11,0 Hardware](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Hardware Unterstützung für Direct3D 10level9-Formate](/previous-versions//ff471324(v=vs.85))
-   [Hardware Unterstützung für Direct3D 10,1-Formate](/previous-versions//cc627091(v=vs.85))
-   [Hardware Unterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))

## <a name="enumerating-adapters"></a>Auflisten von Adaptern

Bei einem Adapter handelt es sich um eine Abstraktion der Hardware und der Software Funktion Ihres Computers. Es gibt im Allgemeinen viele Adapter auf Ihrem Computer. Einige Geräte werden in Hardware (z. b. auf Ihrer Grafikkarte) implementiert, und einige sind in Software implementiert (z. b. Direct3D Reference Rasterizer). Adapter implementieren Funktionen, die von einer Grafikanwendung verwendet werden. Das folgende Diagramm zeigt ein System mit einem einzelnen Computer, zwei Adaptern (Grafikkarten) und drei Ausgabe Monitoren.

![Diagramm eines Computers mit zwei Grafikkarten und drei Monitoren](images/dxgi-terms.png)

Wenn diese Hardwareteile aufgelistet werden, erstellt DXGI eine [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) -Schnittstelle für jede Ausgabe (bzw. jeden Monitor) und eine [**IDXGIAdapter2**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2) -Schnittstelle für jede Grafikkarte (auch wenn es sich um eine Grafikkarte handelt, die in einem Motherboard integriert ist). Die Enumeration erfolgt mithilfe eines [**idxgifactory**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) -Schnittstellen Aufrufes [**idxgifactory:: enumadapters**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-enumadapters), um einen Satz von [**idxgi-Adapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) -Schnittstellen zurückzugeben, die die Video Hardware darstellen.

DXGI 1,1 hat die [**IDXGIFactory1**](/windows/win32/api/DXGI/nn-dxgi-idxgifactory1) -Schnittstelle hinzugefügt. [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) gibt eine Reihe von [**IDXGIAdapter1**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter1) -Schnittstellen zurück, die die Video Hardware darstellen.

Wenn Sie bei der Verwendung von Direct3D-APIs bestimmte Video Hardwarefunktionen auswählen möchten, empfiehlt es sich, die [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) -Funktion oder die [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) -Funktion iterativ mit jedem Adapter Handle und einer möglichen Hardware [Funktionsebene](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)aufzurufen. Diese Funktion ist erfolgreich, wenn die Featureebene vom angegebenen Adapter unterstützt wird.

### <a name="new-info-about-enumerating-adapters-for-windows-8"></a>Neue Informationen zum Auflisten von Adaptern für Windows 8

Ab Windows 8 ist immer ein Adapter mit dem Namen "Microsoft Basic-Rendering-Treiber" vorhanden. Dieser Adapter weist die VendorID **0x1414** und die DeviceID **0x8c** auf. Dieser Adapter weist auch den [**\_ \_ \_ Software Wert des DXGI-Adapters**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) auf, der im **Flags** -Member seiner [**DXGI- \_ Adapter \_ DESC2**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_adapter_desc2) -Struktur festgelegt ist. Bei diesem Adapter handelt es sich um ein nur für das Rendering geschütztes Gerät ohne Anzeige Ausgaben. DXGI gibt nie das [**DXGI- \_ Fehler \_ Gerät \_**](dxgi-error.md) zurück, das für diesen Adapter entfernt wurde.

Wenn der Anzeigetreiber eines Computers nicht funktionsfähig ist oder deaktiviert ist, kann der primäre (**null**) Adapter des Computers auch "Microsoft Basic-Rendering-Treiber" genannt werden. Dieser Adapter weist jedoch Ausgaben auf, und der [**\_ \_ \_ Software Wert des DXGI-Adapters**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) wird nicht festgelegt. Das Betriebssystem und die apps verwenden diesen Adapter standardmäßig. Wenn ein Anzeigetreiber installiert oder aktiviert ist, kann für apps das [**DXGI- \_ Fehler \_ Gerät \_**](dxgi-error.md) für diesen Adapter entfernt werden, und die Adapter müssen erneut erneut aufgelistet werden.

Wenn der primäre Anzeige Adapter eines Computers der "Microsoft Basic Display Adapter" ([Warp](../direct3d11/overviews-direct3d-11-devices-create-warp.md) -Adapter) ist, verfügt dieser Computer auch über einen zweiten Adapter. Bei diesem zweiten Adapter handelt es sich um das reine Rendering-Gerät, das keine Anzeige Ausgaben aufweist und für die DXGI nie das [**DXGI- \_ Fehler \_ Gerät \_**](dxgi-error.md)zurückgibt.

Wenn Sie Warp für Rendering-, COMPUTE-oder andere Tasks mit langer Ausführungszeit verwenden möchten, empfiehlt es sich, das reine rendergerät zu verwenden. Sie können einen Zeiger auf das reine Rendering-Gerät abrufen, indem Sie die [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) -Methode aufrufen. Außerdem erstellen Sie das nur-Rendering-Gerät, wenn Sie [**D3D \_ Driver \_ Type \_ Warp**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type) im *DriverType* -Parameter von [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) angeben, da das Warp-Gerät auch den reinen Rendering-Adapter verwendet.

## <a name="presentation"></a>Präsentation

Die Aufgabe Ihrer Anwendung besteht darin, Frames zu renderken und DXGI aufzufordern, diese Frames der Ausgabe anzuzeigen. Wenn für die Anwendung zwei Puffer verfügbar sind, kann Sie einen Puffer darstellen, während eine andere bereitgestellt wird. Abhängig von der Zeit, die zum Renderingvorgang oder der gewünschten Framerate für die Darstellung benötigt wird, sind für die Anwendung möglicherweise mehr als zwei Puffer erforderlich. Die Gruppe der erstellten Puffer wird als SwapChain bezeichnet, wie hier gezeigt.

![Abbildung einer Swapkette](images/dxgi-swap-chain.png)

-   [Austausch Kette erstellen](#create-a-swap-chain)
-   [Pflege und Fütterung der SwapChain](#care-and-feeding-of-the-swap-chain)
-   [Bearbeiten der Fenstergröße](#handling-window-resizing)
-   [Auswählen der DXGI-Ausgabe und-Größe](#choosing-the-dxgi-output-and-size)
-   [Debuggen im Full-Screen Modus](#debugging-in-full-screen-mode)
-   [Zerstören einer austauschkette](#destroying-a-swap-chain)
-   [Verwenden eines gedrehten Monitors](#using-a-rotated-monitor)
-   [Wechsel Modi](#switching-modes)
-   [Vollbild-Leistungs Tipp](#full-screen-performance-tip)
-   [Überlegungen zum Multithread](#multithread-considerations)

Eine austauschkette verfügt über einen Vorder-und einen oder mehrere Back-Puffer. Jede Anwendung erstellt eine eigene Austausch Kette. Um die Geschwindigkeit der Darstellung der Daten in einer Ausgabe zu maximieren, wird eine Swapkette fast immer im Arbeitsspeicher eines Anzeige Subsystems erstellt, was in der folgenden Abbildung dargestellt ist.

![Abbildung eines Anzeige Subsystems](images/dxgi-adapter.png)

Das Anzeige Subsystem (bei dem es sich häufig um eine Grafikkarte handelt, die jedoch auf einem Motherboard implementiert werden kann) enthält eine GPU, einen Digital-to-Analog-Konverter (DAC) und Arbeitsspeicher. Die Swapkette wird in diesem Arbeitsspeicher zugeordnet, damit die Präsentation sehr schnell ist. Das Anzeige-unter System zeigt die Daten im Vorder Puffer der Ausgabe an.

Eine SwapChain ist so eingerichtet, dass Sie im Vollbildmodus oder im Fenstermodus gezeichnet wird. dadurch ist es nicht erforderlich, dass Sie wissen, ob es sich um eine Ausgabe oder einen Vollbildmodus handelt. Eine Auslagerungs Kette im Vollbild Modus kann die Leistung optimieren, indem die Bildschirmauflösung gewechselt wird.

### <a name="create-a-swap-chain"></a>Erstellen einer Swapchain

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10: Direct3D 10 sind die erste Grafik Komponente für die Verwendung von dxgi. DXGI weist verschiedene Austausch Ketten Verhalten auf.<br/>
<ul>
<li>In DXGI ist eine austauschkette an ein Fenster gebunden, wenn die SwapChain erstellt wird. Diese Änderung verbessert die Leistung und spart Arbeitsspeicher. In früheren Versionen von Direct3D konnte die Swapkette das Fenster ändern, an das die SwapChain gebunden ist.</li>
<li>In DXGI ist eine SwapChain bei der Erstellung an ein renderinggerät gebunden. Das von den Direct3D Create Device Functions zurückgegebene Geräte Objekt implementiert die <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> -Schnittstelle. Sie können <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> zum Abfragen der entsprechenden <a href="/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgidevice2"><strong>IDXGIDevice2</strong></a> -Schnittstelle des Geräts abrufen. Eine Änderung am renderinggerät erfordert, dass die Swapkette neu erstellt wird.</li>
<li><p>In DXGI sind die Auslagerungs Effekte DXGI_SWAP_EFFECT_DISCARD und DXGI_SWAP_EFFECT_SEQUENTIAL verfügbar. Ab Windows 8 ist auch der DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL Swap-Effekt verfügbar. Die folgende Tabelle zeigt eine Zuordnung von Direct3D 9 zu DXGI-Swap-Effekt definiert. </p>
<table>
<thead>
<tr class="header">
<th>D3d9 Swap-Effekt</th>
<th>DXGI-Swap-Effekt</th>
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
<td>DXGI_SWAP_EFFECT_SEQUENTIAL mit mindestens zwei Puffern</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_FLIPEX</td>
<td>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL mit mindestens zwei Puffern</td>
</tr>
</tbody>
</table>
<p></p>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



 

Die Puffer der Swapkette werden in einer bestimmten Größe und in einem bestimmten Format erstellt. Die Anwendung gibt diese Werte an (oder Sie können die Größe vom Zielfenster erben) beim Start und kann Sie dann optional ändern, wenn sich die Fenstergröße in Reaktion auf Benutzereingaben oder Programm Ereignisse ändert.

Nachdem Sie die SwapChain erstellt haben, möchten Sie in der Regel Bilder in Sie darstellen. Hier ist ein Code Fragment, das einen Direct3D-Kontext zum Rendering in eine Swapkette einrichtet. Mit diesem Code wird ein Puffer aus der Swapkette extrahiert, eine renderzielansicht aus diesem Puffer erstellt und dann auf dem Gerät festgelegt:


```
ID3D11Resource * pBB;
ThrowFailure( pSwapChain->GetBuffer(0, __uuidof(pBB),    
  reinterpret_cast<void**>(&pBB)), "Couldn't get back buffer");
ID3D11RenderTargetView * pView;
ThrowFailure( pD3D11Device->CreateRenderTargetView(pBB, NULL, &pView), 
  "Couldn't create view" );
pD3D11DeviceContext->OMSetRenderTargets(1, &pView, 0);
        
```



Nachdem die Anwendung einen Frame in einen Austausch Ketten Puffer gerendert hat, nennen Sie [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). Die Anwendung kann dann zum Rendering des nächsten Bilds wechseln.

### <a name="care-and-feeding-of-the-swap-chain"></a>Pflege und Fütterung der SwapChain

Nachdem Sie das Bild dargestellt haben, rufen Sie [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) auf, und gehen Sie zum Rendering des nächsten Bilds. Das ist das Ausmaß ihrer Verantwortung.

Wenn Sie zuvor [**idxgifactory:: makewindowassociation**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation)aufgerufen haben, kann der Benutzer die Kombination aus Alt-Enter Tasten drücken, und DXGI wechselt zwischen dem Fenstermodus und dem Vollbildmodus. **Idxgifactory:: makewindowassociation** wird empfohlen, da ein Standard Steuerungsmechanismus für den Benutzer dringend erwünscht ist.

Obwohl Sie nicht mehr Code schreiben müssen, als bereits beschrieben wurde, können einige einfache Schritte die reaktionsfähigere Anwendung optimieren. Der wichtigste Aspekt ist die Größe der Puffer der Swapkette als Reaktion auf die Größe des Ausgabe Fensters. Natürlich besteht die beste Route der Anwendung darin, auf die WM-Größe zu reagieren \_ und [**idxgiswapchain:: resizebuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers)aufzurufen und die in den Parametern der Nachricht enthaltene Größe zu übergeben. Durch dieses Verhalten wird Ihre Anwendung offensichtlich für den Benutzer gut reagieren, wenn Sie die Rahmen des Fensters zieht, aber auch genau, was einen reibungslosen voll Bild Übergang ermöglicht. \_Wenn ein solcher Übergang stattfindet, erhält Ihr Fenster eine WM-Größen Meldung, und der Aufruf von **idxgiswapchain:: resizebuffers** ist die Möglichkeit, den Pufferspeicher für eine optimale Darstellung neu zuzuordnen. Aus diesem Grund ist es erforderlich, dass die Anwendung alle Verweise auf den vorhandenen Puffern freigibt, bevor Sie **idxgiswapchain:: resizebuffers** aufruft.

Wenn Sie [**idxgiswapchain:: resizebuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) nicht als Reaktion auf den Vollbildmodus aufrufen, \_ kann die Optimierung des flippens durch DXGI, das in der Antwort auf die WM-Größe am meisten angezeigt wird, die Optimierung des flippens ausschließen, wobei DXGI einfach austauschen kann, welcher Puffer angezeigt wird.

[**IDXGISwapChain1: in:P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) werden Sie informiert, wenn Ihr Ausgabefenster vollständig über den **DXGI- \_ Status " \_ okded**" verdeckt wird. Wenn dies auftritt, wird empfohlen, dass Ihre Anwendung in den Standbymodus wechselt (durch Aufrufen von **IDXGISwapChain1::P resent1** mit **DXGI \_ Present \_ Test**), da die zum Renderingvorgang verwendeten Ressourcen verschwendet werden. Die Verwendung von **DXGI \_ Present- \_ Test** verhindert, dass Daten angezeigt werden, während die Okklusions Prüfung weiterhin durchgeführt wird. **IDXGISwapChain1::P resent1** gibt S \_ OK zurück, Sie sollten den Standbymodus beenden. verwenden Sie den Rückgabecode nicht zum Wechseln in den Standbymodus, da dies dazu führen kann, dass die Swapkette den Vollbildmodus nicht verlassen kann.

Die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist, stellt eine **Swapkette** für das Flip-Modell bereit (d. h. eine Swapkette mit dem [**DXGI- \_ Swap- \_ \_ \_ Effekt**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) ), die im SwapEffect-Member der [**DXGI-Swap- \_ \_ Kette \_ DESC**](/windows/win32/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) oder [**DXGI- \_ SwapChain \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)festgelegt ist. Wenn Sie Frames für eine Ausgabe mit einer Swapkette mit einem Flip-Modell darstellen, hebt DXGI die Bindung des Back Puffers an allen Pipeline Zustands Positionen auf, wie z. b. ein Renderziel für die Ausgabe Zusammenführung, das in den Hintergrund Puffer 0 schreibt. Daher empfiehlt es sich, [**Verknüpfung id3d11devicecontext aus:: omstrendertargets**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets) direkt vor dem renderingzeichen in den Hintergrund Puffer aufzurufen. Nennen Sie z. b. nicht **omstrendertargets** , und führen Sie dann Compute-shaderaufgaben aus, die das Rendering der Ressource nicht beenden. Weitere Informationen zu Austausch Ketten von Flip-Modellen und deren Vorteilen finden Sie unter [DXGI Flip Model](dxgi-flip-model.md).

> [!NOTE]  
> In Direct3D 10 und Direct3D 11 müssen Sie [**idxgiswapchain:: GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) nicht aufrufen, um den Puffer 0 abzurufen, nachdem Sie [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) aufgerufen haben, da sich die Identitäten von backpuffern aus Gründen der Gewohnheit ändern. Dies geschieht in Direct3D 12 nicht, und Ihre Anwendung muss stattdessen die Puffer Indizes manuell nachverfolgen.

### <a name="handling-window-resizing"></a>Bearbeiten der Fenstergröße

Zum Verarbeiten der Fenstergröße können Sie die [**idxgiswapchain:: resizebuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) -Methode verwenden. Vor dem Aufrufen von **resizebuffers** müssen Sie alle ausstehenden Verweise auf die Puffer der Austausch Kette freigeben. Das Objekt, das in der Regel einen Verweis auf den Puffer einer Swapkette enthält, ist eine renderzielansicht.

Der folgende Beispielcode zeigt, wie [**resizebuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) innerhalb des WindowProc-Handlers für WM- \_ Größen Meldungen aufgerufen werden:


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



### <a name="choosing-the-dxgi-output-and-size"></a>Auswählen der DXGI-Ausgabe und-Größe

Standardmäßig wählt DXGI die Ausgabe aus, die den größten Teil des Client Bereichs des Fensters enthält. Dies ist die einzige Option, die für DXGI verfügbar ist, wenn Sie als Reaktion auf Alt + Eingabe den Vollbildmodus selbst durchläuft. Wenn die Anwendung den Vollbildmodus alleine wechselt, kann Sie [**idxgiswapchain:: setfullscreenstate**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) aufrufen und einen expliziten [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) (oder **null**) übergeben, wenn die Anwendung die DXGI-Entscheidung überlassen möchte.

Um die Größe der Ausgabe während des voll Bildschirms oder des Fensters zu ändern, wird empfohlen, [**idxgiswapchain:: resizetarget**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget)aufzurufen, da diese Methode auch die Größe des Zielfensters ändert. Da die Größe des Zielfensters geändert wird, sendet das Betriebssystem die **WM- \_ Größe**, und Ihr Code ruft in der Antwort auf natürliche Weise [**idxgiswapchain:: resizebuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) auf. Es ist daher eine Verschwendung von Aufwand, die Größe der Puffer zu ändern und anschließend die Größe des Ziels zu ändern.

### <a name="debugging-in-full-screen-mode"></a>Debuggen im Vollbildmodus

Eine DXGI-SwapChain gibt den Vollbildmodus nur dann zurück, wenn dies unbedingt erforderlich ist. Dies bedeutet, dass Sie eine Vollbildanwendung mithilfe mehrerer Monitore Debuggen können, solange sich das Debuggingfenster nicht mit dem Zielfenster der Austausch Kette überschneidet. Alternativ können Sie den Modus für den Modus vermeiden, indem Sie das switchflag für das **DXGI- \_ \_ SwapChain- \_ Flag \_ zulassen \_ \_** nicht festlegen.

Wenn der Moduswechsel zulässig ist, gibt eine Austausch Kette den Vollbildmodus aus, sobald das Ausgabefenster von einem anderen Fenster ausgeblendet wird. Die Okklusions Überprüfung wird bei [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)oder einem separaten Thread ausgeführt, dessen Zweck darin besteht, festzustellen, ob die Anwendung nicht mehr reagiert (und **IDXGISwapChain1::P resent1**) nicht mehr aufruft. Legen Sie den folgenden Registrierungsschlüssel auf einen Wert ungleich 0 (null) fest, um die Fähigkeit des separaten Threads zu deaktivieren, einen Switch auszulösen.

**HKCU \\ Software \\ Microsoft \\ DXGI \\ disablefullscreenwatchdog**

### <a name="destroying-a-swap-chain"></a>Zerstören einer austauschkette

Eine SwapChain kann nicht im Vollbildmodus freigegeben werden, da dadurch Thread Konflikte entstehen können (was dazu führt, dass DXGI eine nicht fort Setz Bare Ausnahme auslöst). Wechseln Sie vor dem Freigeben einer austauschkette zuerst in den Fenstermodus (mit [**idxgiswapchain:: setfullscreenstate**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)( **false**, **null** )), und nennen Sie dann [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

### <a name="using-a-rotated-monitor"></a>Verwenden eines gedrehten Monitors

Eine Anwendung muss sich nicht um die Monitor Ausrichtung kümmern, da DXGI bei Bedarf während der Präsentation einen Austausch Ketten Puffer rotiert. Natürlich kann sich diese zusätzliche Rotation auf die Leistung auswirken. Um eine optimale Leistung zu erzielen, führen Sie die Rotation in der Anwendung aus, indem Sie die folgenden Schritte ausführen:

-   Verwenden Sie das **DXGI- \_ \_ SwapChain- \_ Flag \_ nicht vorab**. Dadurch wird DXGI benachrichtigt, dass die Anwendung ein gedrehtes Bild erzeugt (z. b. durch Ändern der Projektions Matrix). Beachten Sie, dass dieses Flag nur im Vollbildmodus gültig ist.
-   Weisen Sie jeden SwapChain-Puffer in seine gedrehte Größe zu. Verwenden Sie [**idxgioutput:: getdesc**](/windows/win32/api/DXGI/nf-dxgi-idxgioutput-getdesc) , um diese Werte ggf. zu erhalten.

Durch Ausführen der Drehung in der Anwendung führt DXGI einfach eine Kopie anstelle einer Kopie und einer Drehung aus.

Die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist, stellt eine Swapkette für das Flip-Modell bereit (d. h. eine Swapkette mit dem [**DXGI- \_ Swap- \_ Effekt \_ \_**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) , die im **SwapEffect** -Member der [**DXGI- \_ \_ SwapChain \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)festgelegt ist). Um die Präsentations Optimierungen zu maximieren, die mit einer Swapkette für das Kippen von Modellen verfügbar sind, empfiehlt es sich, dass Sie die Inhalte Ihrer Anwendungen entsprechend der jeweiligen Ausgabe ausrichten, auf der sich der Inhalt befindet, wenn der Inhalt die Ausgabe vollständig einnimmt. Weitere Informationen zu Austausch Ketten von Flip-Modellen und deren Vorteilen finden Sie unter [DXGI Flip Model](dxgi-flip-model.md).

### <a name="switching-modes"></a>Wechsel Modi

Die DXGI-Swapkette kann den Anzeigemodus einer Ausgabe beim Durchführen eines voll Bild Wechsels ändern. Um die Änderung des automatischen Anzeigemodus zu aktivieren, müssen Sie in der Beschreibung der Austausch Kette **DXGI-Schalter für den Zulassungs \_ \_ \_ \_ \_ \_ Modus zulassen** angeben. Wenn sich der Anzeigemodus automatisch ändert, wählt DXGI den grundlegendsten Modus aus (Größe und Auflösung werden nicht geändert, aber die Farbtiefe kann). Das Ändern der Größe von Swap-Ketten Puffern führt nicht zu einem Modusschalter. Die SwapChain gibt eine implizite Zusage aus, dass bei Auswahl eines Back Puffers, der genau mit einem von der Ziel Ausgabe unterstützten Anzeigemodus übereinstimmt, zu diesem Anzeigemodus gewechselt wird, wenn in den Vollbildmodus für die Ausgabe gewechselt wird. Folglich wählen Sie einen Anzeigemodus aus, indem Sie die Größe und das Format des Hintergrund Puffers auswählen.

### <a name="full-screen-performance-tip"></a>Vollbild-Leistungs Tipp

Wenn Sie [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) auf einer Vollbildanwendung aufzurufen, schaltet die Swapkette den Inhalt des Hintergrund Puffers in den Vordergrund Puffer um (im Gegensatz zu Blits). Hierfür ist es erforderlich, dass die Swapkette mithilfe eines aufgelisteten Anzeigemodus (angegeben in der [**DXGI- \_ \_ SwapChain \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)) erstellt wurde. Wenn Sie die Anzeigemodi nicht aufzählen oder den Anzeigemodus fälschlicherweise in der Beschreibung angeben, kann die Swapkette stattdessen eine Bitblock Übertragung (Bitblock Transfer, BitBLT) durchführen. Das BitBLT bewirkt eine zusätzliche streckungs Kopie sowie eine bessere Auslastung des Video Speichers und ist schwer zu erkennen. Um dieses Problem zu vermeiden, müssen Sie die Anzeigemodi aufzählen und die Beschreibung der Austausch Kette ordnungsgemäß initialisieren, bevor Sie die SwapChain erstellen. Dies gewährleistet eine maximale Leistung beim Kippen im Vollbildmodus und vermeidet zusätzlichen Speicher Mehraufwand.

### <a name="multithread-considerations"></a>Überlegungen zum Multithread

Wenn Sie DXGI in einer Anwendung mit mehreren Threads verwenden, müssen Sie darauf achten, das Erstellen eines Deadlocks zu vermeiden, bei dem zwei verschiedene Threads aufeinander warten. Es gibt zwei Situationen, in denen dies vorkommen kann.

-   Der Renderingthread ist nicht der Nachrichten Pump Thread.
-   Der Thread, der eine DXGI-API ausführt, ist nicht derselbe Thread, der das Fenster erstellt hat.

Achten Sie darauf, dass der Message-Pump-Thread nie auf den Renderthread wartet, wenn Sie voll Bildaustausch Ketten verwenden. Beispielsweise kann das Aufrufen von [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (vom Renderthread) bewirken, dass der Renderthread auf den nachrichtenpump Thread wartet. Wenn eine Modusänderung auftritt, ist dieses Szenario möglich, wenn **Present1** Folgendes aufruft:: SetWindowPos () oder:: setwindowstyle () und eine der folgenden Methoden aufrufen:: SendMessage (). Wenn in diesem Szenario der Nachrichten Pump Thread über einen kritischen Abschnitt verfügt, in dem er sich befindet, oder wenn der Renderthread blockiert wird, werden die beiden Threads Deadlock.

Weitere Informationen zur Verwendung von DXGI mit mehreren Threads finden Sie unter [Multithreading und DXGI](../direct3d11/overviews-direct3d-11-render-multi-thread-intro.md).

## <a name="dxgi-responses-from-dllmain"></a>DXGI-Antworten von DllMain

Da eine [**DllMain**](../dlls/dllmain.md) -Funktion nicht die Reihenfolge garantieren kann, in der DLLs geladen und entladen werden, wird empfohlen, dass die **DllMain** -Funktion der APP keine Direct3D-oder DXGI-Funktionen oder-Methoden aufruft, einschließlich Funktionen oder Methoden, die Objekte erstellen oder freigeben. Wenn die **DllMain** -Funktion Ihrer APP eine bestimmte Komponente aufruft, kann diese Komponente eine andere DLL aufrufen, die nicht auf dem Betriebssystem vorhanden ist, was dazu führt, dass das Betriebssystem abstürzt. Direct3D und DXGI laden möglicherweise einen Satz von DLLs, in der Regel einen Satz von Treibern, der sich von Computer zu Computer unterscheidet. Dies gilt auch dann, wenn Ihre APP auf ihren Entwicklungs-und Testcomputern nicht stürzt, wenn die **DllMain** -Funktion Direct3D-oder DXGI-Funktionen oder-Methoden aufruft. Sie stürzt möglicherweise ab, wenn Sie auf einem anderen Computer ausgeführt wird.

Um zu verhindern, dass Sie eine APP erstellen, die möglicherweise zu einem Absturz des Betriebssystems führt, stellt DXGI die folgenden Antworten in den angegebenen Situationen bereit:

-   Wenn die [**DllMain**](../dlls/dllmain.md) -Funktion Ihrer APP den letzten Verweis auf eine DXGI-Factory freigibt, löst DXGI eine Ausnahme aus.
-   Wenn die [**DllMain**](../dlls/dllmain.md) -Funktion Ihrer APP eine DXGI-Factory erstellt, gibt DXGI einen Fehlercode zurück.

## <a name="dxgi-11-changes"></a>DXGI 1,1-Änderungen

In DXGI 1,1 wurden die folgenden Funktionen hinzugefügt.

-   Unterstützung für synchronisierte Shared-

    Synchronisierte freigegebene Oberflächen für Direct3D 10,1 und Direct3D 11 ermöglichen effiziente Lese-und Schreib Oberflächen Freigabe zwischen mehreren Direct3D-Geräten (die gemeinsame Nutzung von Direct3D 10-und Direct3D 11-Geräten ist möglich). Weitere Informationen finden Sie unter [**idxgikeyedmutex:: acquiresync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-acquiresync) und [**idxgikeyedmutex:: releasesync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-releasesync).

-   Unterstützung für hohe Farben

    Unterstützt das unorm-Format DXGI- \_ Format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ .

-   [**IDXGIDevice1:: setmaximumframelatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) und [ **IDXGIDevice1:: getmaximumframelatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-getmaximumframelatency)
-   [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) Listet lokale Adapter (e) ohne angehängte Monitore oder Ausgaben sowie Adapter (s) mit verbundenen Ausgaben auf. Der erste zurückgegebene Adapter ist der lokale Adapter, auf dem die primäre Desktop Datenbank angezeigt wird.
-   BGRA-Formatunterstützung

    DXGI \_ \_ -Format B8G8R8A8 \_ unorm und DXGI \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB, siehe [**IDXGISurface1:: GetDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-getdc) und [**IDXGISurface1:: ReleaseDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-releasedc).

## <a name="dxgi-12-changes"></a>DXGI 1,2-Änderungen

In DXGI 1,2 wurden die folgenden Funktionen hinzugefügt.

-   Stereo Austausch Kette
-   [Swapkette des Flip-Modells](dxgi-flip-model.md)
-   Optimierte Darstellung (Scrollen, geänderte Rechtecke und Drehung)
-   Verbesserte freigegebene Ressourcen und Synchronisierung
-   [Desktop Duplizierung](desktop-dup-api.md)
-   Optimierte Verwendung von Videospeicher
-   Unterstützung für 16 Bits pro Pixel (BPP)-Formate (DXGI- \_ Format \_ B5G6R5 \_ unorm, DXGI- \_ Format \_ B5G5R5A1 \_ unorm, DXGI- \_ Format \_ B4G4R4A4 \_ unorm)
-   Debugging-APIs

Weitere Informationen zu DXGI 1,2 finden Sie unter [DXGI 1,2-Verbesserungen](dxgi-1-2-improvements.md).

## <a name="related-topics"></a>Zugehörige Themen

[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)
