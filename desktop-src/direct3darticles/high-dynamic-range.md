---
title: Verwenden von DirectX mit High Dynamic Range-Displays und erweiterter Farbe
description: Dieses Thema bietet eine technische Übersicht über das Rendern von Inhalten mit hoher dynamischer Breite Direct3D 11 und Direct3D 12 in eine HDR10-Anzeige mithilfe von Unterstützung für erweiterte Farben in Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104553357"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a>Verwenden von DirectX mit dynamischen Bereichs anzeigen und erweiterter Farbe

Dieses Thema bietet eine technische Übersicht über die Ausgabe von Direct3D 11-und Direct3D 12-Inhalten in eine HDR10-Anzeige mithilfe von Unterstützung für erweiterte Farben in Windows 10. Es fasst einige wichtige konzeptionelle Unterschiede zwischen der Ausgabe von HDR10 im Vergleich zu herkömmlichen standardmäßigen Dynamic Range-anzeigen (SZR) zusammen. Außerdem werden die wichtigsten technischen Anforderungen für Ihre APP behandelt, um die erweiterte Windows-Farbe sowie Empfehlungen und bewährte Methoden zu unterstützen.

## <a name="introduction"></a>Einführung

Windows 10 unterstützt HDR und andere erweiterte Farbanzeige, die eine deutlich höhere Farbgenauigkeit als herkömmliche SZR-anzeigen bieten. Sie können "Direct3D", "Direct2D" und andere Grafik-APIs verwenden, um HDR-Inhalte in einer fähigen Anzeige darzustellen.

Die erweiterte Farbe von Windows bezieht sich auf verschiedene verwandte Technologien, die erstmals mit Windows 10 Version 1703 eingeführt wurden und Unterstützung für Anzeigefunktionen bieten, die die Farbfunktionen herkömmlicher standardmäßiger dynamischer Bereiche (SDR) anzeigen. Die drei wichtigsten erweiterten Funktionen werden unten beschrieben. Der häufigste Typ der erweiterten Farbanzeige, HDR10, unterstützt alle drei erweiterten Funktionen.

### <a name="high-dynamic-range"></a>Hoher dynamischer Bereich

Der dynamische Bereich bezieht sich auf den Unterschied zwischen der maximalen und der minimalen Leuchtkraft in einer Szene. Dies wird häufig in Nits gemessen (Kerzen-pro Quadratzentimeter). In realen Szenen, wie z. b. bei diesem Sonnenuntergang, gibt es häufig dynamische Bereiche mit einer Größe von mehr als einer Leuchtkraft. das menschliche Auge kann nach der Anpassung einen noch größeren Bereich erkennen.

![Bild des Sonnen namens mit Helligkeit und dunkelsten Punkten in der Szene mit der Bezeichnung](images/HDR-HDR.jpg)

Seit Direct3D 9 können Grafik-Engines Ihre Szenen intern mit dieser Ebene physisch präziser Treue Renderen. Allerdings kann eine typische standardmäßige dynamische Bereichs Anzeige nur ein wenig mehr als drei Reihenfolge der Leuchtkraft reproduzieren. Daher muss jeder mit HDR gerenderte Inhalt in den begrenzten Bereich der Anzeige tonezugeordnet (komprimiert) werden. Neue HDR-anzeigen, einschließlich derjenigen, die dem HDR10 (BT. 2100)-Standard entsprechen, unterbrechen diese Einschränkung.

### <a name="wide-color-gamut-with-automatic-system-color-management"></a>Breite Farbpalette mit automatischer System Farbverwaltung

Farb-Farbskala bezieht sich auf den Bereich und die Sättigung der Schattierungen, die eine Anzeige reproduzieren kann. Die gebräuchlichste natürliche Farbe, die das menschliche Auge erkennen kann, ist rein, Monochromatisch, wie z. b. das, was von einem Laser erzeugt wird. Allerdings können gängige Consumer-anzeigen häufig Farben nur innerhalb des sRGB-Gamut reproduzieren, der nur ungefähr 35% aller von Menschen wahrnehmbaren Farben darstellt. Das folgende Diagramm ist eine Darstellung des menschlichen "spektralen Lokus" oder aller wahrnehmbaren Farben (auf einer bestimmten Beleuchtungs Ebene), wobei das kleinere Dreieck der sRGB-Gamut ist.

![Diagramm des menschlichen spektralen Lokus und sRGB-Farbskala](images/HDR-WCG.jpg)

High-End, die Professional PC-Anzeige hat lange unterstützte Farbspiele, die deutlich breiter als sRGB sind, z. b. Adobe RGB und D65-P3. Diese großen Fenster anzeigen werden immer häufiger. Vor der erweiterten Farbe hat Windows jedoch keine Farbverwaltung auf Systemebene für Anwendungen durchgeführt. Dies bedeutete, dass Windows beim Rendern einer DirectX-APP, z. b. eines reinen roten oder RGB (1.0, 0,0, 0,0) in seine Swapkette, einfach das am stärksten satte rote Abbild Scannen konnte, das die Darstellung reproduzieren konnte, unabhängig davon, was der tatsächliche Farbverlauf der Anzeige war.

Apps, die eine hohe Farbgenauigkeit benötigten, konnten die Farbfunktionen der Anzeige Abfragen (z. b. mithilfe von "ICC-Profilen") und eine eigene Prozess interne Farbverwaltung durchführen, um den Farbverlauf der Anzeige ordnungsgemäß zu verwenden. Bei den meisten apps und visuellen Inhalten wird jedoch davon ausgegangen, dass die Anzeige sRGB ist, und Sie verlassen sich auf das Betriebssystem, um diese Annahme zu erfüllen.

Die erweiterte Windows-Farbe fügt eine automatische Farbverwaltung auf Systemebene hinzu. Der Desktopfenster-Manager (DWM) ist Windows-Compositor. Wenn erweiterte Farbe aktiviert ist, führt die DWM eine explizite Farbkonvertierung aus dem colorspace-Element der visuellen app in einen kanonischen Kompositions Farbraum durch, bei dem es sich um ScRGB handelt. Windows konvertiert dann den zusammengesetzten Frame Puffer-Inhalt in den nativen Farbraum der Anzeige. Auf diese Weise erhält herkömmliche sRGB-Inhalte automatisch ein Farb genaues Verhalten, während erweiterte Farb abhängige Apps die vollständigen Farbfunktionen der Anzeige nutzen können.

### <a name="deep-precisionbit-depth"></a>Tiefe Genauigkeit/Bittiefe

Die numerische Genauigkeit oder die Bittiefe bezieht sich auf das darstellen oder unterscheiden zwischen ähnlichen, aber unterschiedlichen Farben ohne Bandbreite und Artefakte. Der Mainstream-PC zeigt Unterstützung für 8 Bits pro Farbkanal an, während für das menschliche Auge mindestens 10-12 Bits an Genauigkeit erforderlich sind, um wahrnehmbare Verzerrungen zu vermeiden, ohne auf Techniken wie Dithering oder die Anzeige Bedingungen zurückgreifen zu müssen.

![Bild von Windmühlen mit simulierten 2 Bits pro Farbkanal und 8 Bits pro Kanal](images/HDR-bitdepth.jpg)

Vor der erweiterten Farbe haben die DWM-Anwendungen eingeschränkt, um Inhalt nur in 8 Bits pro Farbkanal auszugeben, auch wenn die Anzeige eine höhere Bitrate unterstützte. Wenn erweiterte Farbe aktiviert ist, führt die DWM die Komposition mithilfe des IEEE-Werts mit halber Genauigkeit (FP16) aus, um Engpässe zu beseitigen und die Verwendung der vollständigen Genauigkeit der Anzeige zuzulassen.

## <a name="system-requirements"></a>Systemanforderungen

### <a name="operating-system-os"></a>Betriebssystem

Die erweiterte Farbunterstützung ist zuerst mit Windows 10, Version 1703, ausgeliefert und wurde bei jedem Update erheblich verbessert. In diesem Thema wird davon ausgegangen, dass Ihre APP auf Windows 10, Version 1903 oder höher, abzielt.

### <a name="display"></a>Anzeige

Um einen hohen dynamischen Bereich zu nutzen, müssen Sie über eine Anzeige verfügen, die den HDR10-Standard unterstützt. Windows funktioniert am besten mit anzeigen, die [VESA displayhdr-zertifiziert](https://displayhdr.org/)sind.

### <a name="graphics-processor-gpu"></a>Grafikprozessor (GPU)

Eine aktuelle GPU ist erforderlich. Zur Unterstützung von HDR10-anzeigen erfordert Windows 10 einen der folgenden Punkte.

* NVIDIA GeForce 1000-Serie (Pascal) oder neuer
* AMD Radeon RX 400 Series (Polaris) oder neuer
* Ausgewählte Intel Core 7-Serie (kaby Lake) oder höher

Beachten Sie, dass abhängig von den Szenarien, einschließlich Hardware-Codec-Beschleunigung (10 Bit hevc, 10 Bit VP9 usw.) und PlayReady-Unterstützung (SL3000), zusätzliche Hardwareanforderungen gelten. Weitere Informationen erhalten Sie von Ihrem GPU-Anbieter.

### <a name="graphics-driver-wddm"></a>Grafiktreiber (WDDM)

Der neueste verfügbare Grafiktreiber wird dringend empfohlen, entweder von Windows Update oder vom GPU-Hersteller oder von der Website des PC-Herstellers. Für Windows 10, Version 1903 und höher, empfehlen wir Treiber, die mindestens Windows Display Driver Model (WDDM), Version 2,6, unterstützen.

## <a name="supported-rendering-apis"></a>Unterstützte Rendering-APIs

Windows 10 unterstützt eine Vielzahl von renderingapis und Frameworks. Die erweiterte Farbunterstützung basiert im Grunde darauf, dass Ihre APP eine moderne Präsentation mit DXGI oder den APIs der visuellen Ebene durchführen kann.

* [DirectX-Grafik Infrastruktur (DXGI)](../direct3ddxgi/dx-graphics-dxgi.md)
* [Visuelle Ebene (Windows. UI. Composition)](/windows/uwp/composition/visual-layer)

Daher kann jede Rendering-API, die eine dieser Präsentationsmethoden ausgeben kann, die erweiterte Farbe unterstützen. Dies umfasst u. a. die folgenden.

* [Direct3D 11](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [Direct3D 12](../direct3d12/direct3d-12-graphics.md)
* [Direct2D](../direct2d/direct2d-portal.md)
* [Win2D](https://github.com/Microsoft/Win2D)
  * Erfordert die Verwendung der **kanvasswapchain** -oder **canvasswapchainpanel** -APIs auf niedrigerer Ebene.
* [**Windows.UI.Input.Inking**](/uwp/api/Windows.UI.Input.Inking)
  * Unterstützt das benutzerdefinierte Dry Ink-Rendering mit DirectX.
* [XAML](/windows/uwp/xaml-platform/)
  * Unterstützt die Wiedergabe von HDR-Videos mithilfe von **mediaplayerelement**.
  * Unterstützt die Decodierung von JPEG XR-Bildern mithilfe des **Image** -Elements.
  * Unterstützt DirectX-Interop mithilfe von " **Swap-chainpanel**".

## <a name="handling-dynamic-display-capabilities"></a>Behandeln dynamischer Anzeigefunktionen

Windows 10 unterstützt eine große Bandbreite von erweiterten Farb fähigen anzeigen, von energieeffizienten integrierten Panels bis hin zu High-End-Gaming-Monitoren und-fern. Windows-Benutzer erwarten, dass Ihre APP alle diese Variationen nahtlos verarbeitet, einschließlich der universellen vorhandenen SZR-Anzeige.

Windows 10 bietet dem Benutzer die Kontrolle über die Funktionen von HDR und erweiterten Farben. Ihre APP muss die Konfiguration der aktuellen Anzeige erkennen und dynamisch auf alle Änderungen reagieren. Dies kann verschiedene Ursachen haben, z. b. weil der Benutzer eine Funktion aktiviert oder deaktiviert oder die APP zwischen verschiedenen anzeigen verschoben hat oder sich der Energiezustand des Systems geändert hat.

### <a name="universal-windows-platform-uwp-apps"></a>Universelle Windows-Plattform-Apps (UWP)

Wenn Sie eine UWP-app schreiben, verwenden Sie, unabhängig von der verwendeten Grafik Rendering-API, [**advancedcolorinfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) , um Anzeigefunktionen zu erhalten. Rufen Sie eine Instanz von **advancedcolorinfo** aus [**Displayinformation:: getadvancedcolorinfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo)ab.

Verwenden Sie die [**currentadvancedcolorkind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) -Eigenschaft, um zu überprüfen, welche erweiterte Farbart derzeit aktiv ist. In Windows 10, Version 1903 und höher, wird ein von drei möglichen Werten zurückgegeben: " **SZR**", " **WCG**" oder " **HDR**". Dies ist die wichtigste zu Überprüfung, und Sie sollten die Renderingpipeline und die Präsentations Pipeline als Reaktion auf die aktive Art konfigurieren.

Um zu überprüfen, welche erweiterten Farb Arten unterstützt werden, aber nicht unbedingt aktiv sind, wenden Sie [**isadvancedcolorkindavailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable)an. Sie können diese Informationen z. b. verwenden, um den Benutzer zur Eingabe der Windows-Einstellungs-APP aufzufordern, damit Sie HDR oder WCG aktivieren können.

Die anderen Mitglieder von **advancedcolorinfo** stellen quantitative Informationen über das physische Farbvolumen des Panels ("Leuchtkraft" und "Chrominance") bereit, die den statischen HDR-Metadaten von SMPTE St. 2086 entsprechen. Sie sollten diese Informationen verwenden, um die HDR Tonemapping-und Farbskala-Zuordnung Ihrer APP zu konfigurieren.

Registrieren Sie sich für das [**advancedcolorinfochanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) -Ereignis, um Änderungen in erweiterten Farbfunktionen zu verarbeiten. Dieses Ereignis wird ausgelöst, wenn sich ein Parameter der erweiterten Farbfunktionen der Anzeige aus irgendeinem Grund ändert.

Behandeln Sie dieses Ereignis, indem Sie eine neue Instanz von **advancedcolorinfo** abrufen und überprüfen, welche Werte geändert wurden.

### <a name="desktop-win32-directx-apps"></a>Desktop-DirectX-Apps (Win32)

Wenn Sie eine Win32-app schreiben und DirectX zum Renderingvorgang verwenden, verwenden Sie [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) , um Anzeigefunktionen zu erhalten. Rufen Sie eine Instanz dieser Struktur über [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1)ab.

Um zu überprüfen, welche erweiterte Farbart derzeit aktiv ist, verwenden Sie die **colorspace** -Eigenschaft, die vom Typ [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)ist, und enthält einen der folgenden Werte:

* **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR
* **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR

> [!Note]
> Andere erweiterte Farb Arten, wie z. b. WCG, werden von DXGI als SZR behandelt. DXGI kann nicht verwendet werden, um eine WCG-Anzeige zu identifizieren.

> [!Note]
> Mit DXGI können Sie nicht überprüfen, welche erweiterten Farb Arten unterstützt werden, aber derzeit nicht aktiv sind.

Die meisten anderen Member von **DXGI_OUTPUT_DESC1** stellen quantitative Informationen über das physische Farbvolumen des Panels ("Leuchtkraft" und "Chrominance") bereit, die den statischen HDR-Metadaten von SMPTE St. 2086 entsprechen. Sie sollten diese Informationen verwenden, um die HDR Tonemapping-und Farbskala-Zuordnung Ihrer APP zu konfigurieren.

Win32-apps verfügen über keinen systemeigenen Mechanismus zum reagieren auf Erweiterte Farb Funktionsänderungen. Wenn Ihre APP eine Renderschleife verwendet, sollten Sie stattdessen [**IDXGIFactory1:: IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) mit jedem Frame Abfragen. Wenn **false** angezeigt wird, sollten Sie eine neue **DXGI_OUTPUT_DESC1** abrufen und überprüfen, welche Werte geändert wurden.

Außerdem sollte die Win32-Nachrichten Pumpe die [**WM_SIZE**](../winmsg/wm-size.md) Nachricht verarbeiten, die darauf hinweist, dass Ihre APP möglicherweise zwischen verschiedenen anzeigen verschoben wurde.

> [!Note]
> Zum Abrufen eines neuen **DXGI_OUTPUT_DESC1** müssen Sie die aktuelle Anzeige abrufen. Allerdings sollten Sie **idxgiswapchain:: getcontainingoutput** nicht aufrufen. Dies liegt daran, dass Swapketten eine veraltete DXGI-Ausgabe zurückgeben, sobald **dxgifactory:: IsCurrent** false ist, und wenn die SwapChain neu erstellt wird, um eine aktuelle Ausgabe zu erhalten, wird ein temporärer schwarzer Bildschirm angezeigt. Stattdessen wird empfohlen, die Grenzen aller DXGI-Ausgaben aufzulisten und zu bestimmen, welche Schnittmenge mit den Begrenzungen Ihres App-Fensters am größten ist.

Das folgende Codebeispiel stammt aus dem [Repository DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a>Einrichten der DirectX-Swap-Kette

Nachdem Sie festgestellt haben, dass die Anzeige derzeit erweiterte Farbfunktionen unterstützt, konfigurieren Sie die Swapkette wie folgt.

### <a name="use-a-flip-presentation-model-effect"></a>Verwenden eines Flip Presentation Model-Effekts

Beim Erstellen der **SwapChain mithilfe von "fiateswapchainfor" [HWND | Komposition | Corewindow]** -Methoden. Sie müssen das DXGI-Flip-Modell verwenden, indem Sie entweder die Option " **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** " oder " **DXGI_SWAP_EFFECT_FLIP_DISCARD** " auswählen, wodurch die SwapChain für die erweiterte Farbverarbeitung von DWM und verschiedene voll Bild Optimierungen geeignet ist. Weitere Informationen finden Sie im Thema [zur optimalen Leistung und zum Verwenden des DXGI-Flip-Modells](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a>Option 1. FP16-Pixel Format und ScRGB-Farbraum verwenden

Windows 10 unterstützt zwei Haupt Kombinationen von Pixel Format und Farbraum für erweiterte Farben. Wählen Sie einen basierend auf den spezifischen Anforderungen Ihrer APP aus.

Für allgemeine apps empfiehlt es sich beim Erstellen der SwapChain, [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)anzugeben. Dies wird auch als *FP16* in Ihrer [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)bezeichnet. Standardmäßig wird eine Austausch Kette, die mit einem Gleit Komma-Pixel Format erstellt wurde, so behandelt, als ob Sie den [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) Farbraum verwendet, der auch als *ScRGB* bezeichnet wird.

Diese Kombination ermöglicht Ihnen den numerischen Bereich und die Genauigkeit, um nahezu jede physisch mögliche Farbe anzugeben und eine beliebige Verarbeitung einschließlich der Mischung auszuführen. Wenn Sie Direct2D, Win2D oder Windows. UI. Composition verwenden, ist dies die einzige unterstützte Kombination für alle Austausch Ketten oder Zwischenziele, die erweiterte Farb Inhalte enthalten. 

Der wichtigste Nachteil dieser Option besteht darin, dass Sie 64 Bits pro Pixel verbraucht, wodurch die GPU-Bandbreite und der Arbeitsspeicher Verbrauch im Vergleich zu den herkömmlichen Uint8 SZR-Pixel Formaten verdoppelt werden. Außerdem verwendet ScRGB numerische Werte außerhalb des normalisierten [0, 1]-Bereichs zur Darstellung von Farben außerhalb der sRGB-Farbskala und/oder mehr als 80 Nits der Leuchtkraft. ScRGB (1,0, 1,0, 1,0) codiert z. b. den standardmäßigen D65 White bei 80 Nits. ScRGB (12,5, 12,5, 12,5) codiert jedoch dasselbe D65 weiß bei einem wesentlich helleren 1000-Nits. Für einige Grafik Vorgänge ist ein normalisierter numerischer Bereich erforderlich, und Sie müssen den Vorgang entweder ändern oder die Farbwerte erneut normalisieren.

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a>Option 2: Verwenden des UINT10/RGB10-Pixel Formats und des HDR10/BT. 2100-Farbraum

Für apps, die HDR10-codierten Inhalt verwenden, z. b. Medien Player, oder apps, die voraussichtlich in voll Bild Szenarien wie Spielen verwendet werden sollen, sollten Sie beim Erstellen der SwapChain die Angabe von [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)in Erwägung gezogen. Standardmäßig wird dies als Verwendung des sRGB-Farbraum behandelt. Daher müssen Sie [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)explizit aufzurufen und als Farbraum [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)(auch als HDR10/BT. 2100 bezeichnet) festgelegt werden.

Diese Kombination hat strengere Einschränkungen als FP16. Dies kann nur mit Direct3D 11 oder Direct3D 12 verwendet werden. Außerdem weist UINT10/HDR10 Einschränkungen als zwischen Format auf, da die St. 2084 EotF ("Gamma"-Funktion) verwendet wird, die sehr nicht linear ist und als Wire-Format optimiert ist, und da Sie nur 2 Bits von Alpha bietet.

Diese Kombination kann jedoch leistungsstarke Leistungsoptimierungen bieten, wenn Sie in der endgültigen Ausgabe Ihrer APP verwendet werden. Dabei werden die gleichen 32 Bits pro Pixel wie herkömmliche Uint8-SZR-Pixel Formate verwendet. Außerdem kann das Betriebssystem in bestimmten Vollbild-Szenarios die Leistung optimieren, indem es die HDR10-Oberfläche direkt scannt.

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a>Verwenden einer erweiterten Farb Austausch Kette, wenn sich die Anzeige im SDR-Modus befindet

Sie können eine erweiterte Farb Austausch Kette auch dann verwenden, wenn die Anzeige einige oder alle der erweiterten Farbfunktionen, die ihr Inhalt erfordert, nicht unterstützt. In diesen Fällen konvertiert der Desktopfenster-Manager (DWM) ihre Inhalte so, dass Sie den Funktionen der Anzeige angepasst werden. In Windows 10, Version 1903 und höher, wird ein numerisches Abschneiden durchgeführt. Wenn Sie z. b. eine FP16 ScRGB-Swap-Kette renderingkette, wird alles außerhalb des numerischen Bereichs [0, 1] abgeschnitten.

Dieses downkonvertierungsverhalten tritt auch auf, wenn das App-Fenster zwei oder mehr anzeigen mit unterschiedlichen erweiterten Farbfunktionen überspannt. **Advancedcolorinfo** und **IDXGIOutput6** werden abstrahiert, um nur die Merkmale der Haupt Anzeige zu melden (definiert als die Anzeige, die den Mittelpunkt des Fensters enthält).

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a>Ordnungsgemäße Rendering von "SDR Content" mit der SZR-Referenz

In vielen Szenarios möchte Ihre APP sowohl den SZR-als auch den HDR-Inhalt darstellen. beispielsweise das Rendern von Untertiteln oder Transport Steuerelementen über das HDR-Video oder die Benutzeroberfläche in eine Spielszene. Es ist wichtig, das Konzept der *SZR-Referenz-weißen Ebene* zu verstehen, um sicherzustellen, dass Ihr SZR-Inhalt in einer HDR-Anzeige korrekt aussieht.

Der HDR-Inhalt wird von Windows als _Szenen bezogen_ behandelt, was bedeutet, dass ein bestimmter Farbwert auf einer bestimmten Leuchtkraft Ebene angezeigt werden soll. beispielsweise codieren sowohl ScRGB (1,0, 1,0, 1,0) als auch HDR10 (497, 497, 497) genau D65 White bei 80 Nits-Beleuchtung. In der Zwischenzeit wurde in der Regel der _compilerinhalt ausgegeben_ (oder auf den Display verwiesen), was bedeutet, dass seine Leuchtkraft dem Benutzer oder dem Gerät überlassen wird. beispielsweise codiert sRGB (1,0, 1,0, 1,0) D65 White wie in den HDR-Beispielen, aber mit der maximalen Helligkeit, für die die Anzeige konfiguriert ist. Mithilfe von Windows kann der Benutzer die Whitelist für den _SZR-Verweis_ auf seine bevorzugte Einstellung festlegen. Dies ist die Leuchtkraft, mit der Windows sRGB (1,0, 1,0, 1,0) in Rendering wird. Auf Desktop-HDR-Monitoren werden SZR-Referenz-White Levels in der Regel auf etwa 200 nits festgelegt.

> [!Note]
> In einer Anzeige, die ein Helligkeits Steuerelement unterstützt, wie z. b. auf einem Laptop, passt Windows auch die Leuchtkraft von HDR (Szenen bezogen) an, die der gewünschten Helligkeits Ebene des Benutzers entsprechen, aber dies ist für die APP nicht sichtbar. Wenn Sie nicht versuchen, eine bitgenaue Reproduktion des HDR-Signals zu gewährleisten, können Sie dies im allgemeinen ignorieren.

Wenn Ihre APP immer SZR und HDR zum Trennen der Oberflächen rendert und auf der Betriebssystem Komposition basiert, führt Windows automatisch die richtige Anpassung durch, um die e/a-Inhalte auf die gewünschte weiße Ebene zu erhöhen. Wenn Ihre APP z. b. XAML verwendet und den HDR-Inhalt in einem eigenen " **Swap-chainpanel**" rendert.

Wenn Ihre APP jedoch eine eigene Komposition von SDR-und HDR-Inhalten in einer einzigen Oberfläche ausführt, sind Sie dafür verantwortlich, die positiv Anpassung der SZR-Referenz auf der whitelinbene auszuführen. Andernfalls erscheint der Inhalt der SDR-Inhalte möglicherweise zu schlecht, wenn Sie typische Desktop Anzeige Bedingungen annehmen Zuerst müssen Sie die aktuelle SZR-Referenz-White-Ebene abrufen und dann die Farbwerte aller von Ihnen renderenden SZR-Inhalte anpassen.

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a>Schritt 1: Abrufen der aktuellen SZR-Referenz-weißen Ebene

Derzeit können nur UWP-Apps die aktuelle SZR-Referenz-weißen Ebene über [**advancedcolorinfo. sdrwhitelevelinnits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits)abrufen. Diese API erfordert ein [**corewindow**](/uwp/api/Windows.UI.Core.CoreWindow).

### <a name="step-2-adjust-color-values-of-sdr-content"></a>Schritt 2: Anpassen von Farbwerten von "SDR Content"

Windows definiert den nominalen bzw. den Standard Verweis auf die weiße Ebene bei 80 Nits. Wenn Sie also eine standardmäßige sRGB-(1,0, 1,0, 1,0) weiß in einer FP16-SwapChain gerenden, wird Sie bei der "80 Nits"-Beleuchtung reproduziert. Um die tatsächliche benutzerdefinierte Verweis-weißen Ebene abzugleichen, müssen Sie den compilerinhalt von 80 Nits an die Ebene anpassen, die über **advancedcolorinfo. sdrwhitelevelinnits** angegeben wird.

Wenn Sie mithilfe von FP16 und ScRGB oder mit einem beliebigen Farbraum, der lineare (1,0) Gamma verwendet, gerendert werden, können Sie einfach den Wert von "SDR" durch _advancedcolorinfo. sdrwhitelevelinnits_  /  _80_ multiplizieren. Wenn Sie Direct2D verwenden, gibt es eine vordefinierte Konstante [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f)mit einem Wert von 80.

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

Wenn Sie mit einem nichtlinearen Gamma-Farbraum wie HDR10 rendern, ist die Durchführung der Farb verarbeistung der SZR-Ebene komplexer. Wenn Sie einen eigenen Pixelshader schreiben, sollten Sie in Erwägung gezogen werden, die Anpassung in lineare Gamma vorzunehmen.

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a>Anpassen von HDR-Inhalten an die Anzeigefunktionen mithilfe von Tonemapping

Die Farbe "HDR" und "Advanced" unterscheiden sich in Bezug auf ihre Funktionen stark. Beispielsweise die minimale und die maximale Leuchtkraft und die Farbpalette, die Sie reproduzieren können. In vielen Fällen enthalten die HDR-Inhalte Farben, die die Anzeigefunktionen überschreiten. Um die beste Bildqualität zu erzielen, ist es wichtig, dass Sie HDR Tonemapping durchführen, wobei der Bereich der Farben im Grunde an die Anzeige angepasst wird, während die visuelle Absicht der Inhalte am besten gewahrt bleibt.

Der wichtigste einzige Parameter für die Anpassung ist die maximale Helligkeit, auch bekannt als maxcll (Content Light Level). komplexere Tonmapper passen auch min. Leuchtkraft (mincll) und/oder Farb Replikate an.

### <a name="step-1-get-the-displays-color-volume-capabilities"></a>Schritt 1: Hiermit werden die Farbvolumen Funktionen der Anzeige angezeigt.

#### <a name="universal-windows-platform-uwp-apps"></a>Universelle Windows-Plattform-Apps (UWP)

Verwenden Sie [**advancedcolorinfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) , um das farbvolume der Anzeige zu erhalten.

#### <a name="win32-desktop-directx-apps"></a>Win32-Apps (Desktop)

Verwenden Sie [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) , um das farbvolume der Anzeige zu erhalten.

### <a name="step-2-get-the-contents-color-volume-information"></a>Schritt 2: Die farbvolumeinformationen des Inhalts erhalten.

Abhängig davon, woher der HDR-Inhalt stammt, gibt es mehrere Möglichkeiten, seine Beleuchtungs-und Farb Spielinformationen zu bestimmen. Bestimmte HDR-Video-und Bilddateien enthalten SMPTE St. 2086-Metadaten. Wenn Ihr Inhalt dynamisch gerendert wurde, können Sie möglicherweise szeneninformationen aus den internen renderingstufen extrahieren, z. b. die hellste helle Quelle in einer Szene.

Eine allgemeinere, aber Rechen aufwändige Lösung besteht darin, ein Histogramm oder einen anderen Analyse Durchlauf für den gerenderten Frame auszuführen. Das [Direct2D Advanced Color Images SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) veranschaulicht, wie dies mithilfe von Direct2D durchzuführen ist. die relevantesten Code Ausschnitte sind unten aufgeführt:

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a>Schritt 3: Ausführen des Vorgangs "HDR Tonemapping"

Tonemapping ist naturgemäß ein verlustfreier Prozess und kann für eine Reihe von perzeptive oder zielmetriken optimiert werden, sodass es keinen Standard Algorithmus gibt. Windows bietet einen integrierten [HDR Tonemapper-Effekt](../direct2d/hdr-tone-map-effect.md) als Teil von Direct2D und in der Media Foundation HDR-Videowiedergabe Pipeline. Einige andere häufig verwendete Algorithmen sind ACEs filmic, Reinhard und ITU-R BT. 2390-3 EETF (Electric-Electrical Transfer Function).

Unten ist ein vereinfachter Reinhard Tonemapper-Operator angegeben.

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a>Erfassen von HDR-und WCG-Inhalten

APIs, die die Angabe von Pixel Formaten unterstützen, wie z. b. die im [**Windows. Graphics. Capture**](/uwp/api/windows.graphics.capture) -Namespace und die [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) -Methode, bieten die Möglichkeit, HDR-und WCG-Inhalte zu erfassen, ohne Pixel Informationen zu verlieren. Beachten Sie, dass nach dem Erwerb von Inhalts Frames zusätzliche Verarbeitungsschritte erforderlich sind. Beispielsweise die HDR-zu-SZR-Zuordnungs Zuordnung (z. b. "htmscreencopy" für die Internet Freigabe) und die Speicherung von Inhalten mit dem richtigen Format (z. b. JPEG XR).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

* *Verwenden des HDR-Rendering mit dem DirectX-Toolkit* für [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering). Exemplarische Vorgehensweise zum Hinzufügen von HDR-Unterstützung zu einer DirectX-App mithilfe des DirectX-Toolkits (directxtk).
* [Direct2D Advanced Color Images SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages). UWP SDK-Beispiel, das einen erweiterten Farb abhängigen HDR-und WCG-Bild-Viewer mit Direct2D implementiert. Veranschaulicht die vollständige Palette der bewährten Methoden für UWP-apps, einschließlich der Reaktion auf Änderungen der Anzeigefunktionen und der Anpassung für die e/a-weißen Ebene.
* [Direct3D 12 HDR Desktop-Beispiel](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR). Desktop SDK-Beispiel, das eine grundlegende Direct3D 12 HDR-Szene implementiert.
* [Direct3D 12 HDR UWP-Beispiel](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR). UWP-Entsprechung des obigen Beispiels.
* [Xbox ATG simplehdr-PC-Beispiel](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC). Desktop SDK-Beispiel, das eine grundlegende Direct3D 11 HDR-Szene implementiert.
