---
description: Dieses Thema enthält Entwicklerleitfäden zum Maximieren von Leistung und Effizienz im Präsentationsstapel für moderne Versionen von Windows.
ms.assetid: B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1
title: Verwenden Sie das DXGI-Flip-Modell, um eine optimale Leistung zu erzielen.
ms.topic: article
ms.date: 05/31/2018
ms.custom: RS5
ms.openlocfilehash: ce999bc735042132902158cfd6bd6d41296d29a3afc98ab27d9480dc6bd8b3b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951220"
---
# <a name="for-best-performance-use-dxgi-flip-model"></a>Verwenden Sie das DXGI-Flip-Modell, um eine optimale Leistung zu erzielen.

Dieses Thema enthält Entwicklerleitfäden zum Maximieren von Leistung und Effizienz im Präsentationsstapel für moderne Versionen von Windows. Dabei werden dxgi flip model , DirectX 12: Presentation Modes In Windows 10 (video) und Presentation Enhancements in Windows 10: An Early Look (video) left off [(DXGI Flip-Modell,](dxgi-flip-model.md) [DirectX 12: Präsentationsmodi in Windows 10 (Video)](https://www.youtube.com/watch?v=E3wTajGZOsA)und [Presentation Enhancements in Windows 10: An Early Look (video) left off(Präsentationserweiterungen in Windows 10: Ein frühes Aussehen (Video))](https://www.youtube.com/watch?v=nUZVV_mssWQ) aufgehört.

## <a name="call-to-action"></a>Handlungsaufforderung

Wenn Sie weiterhin **DXGI \_ SWAP EFFECT \_ \_ DISCARD** oder DXGI SWAP EFFECT SEQUENTIAL (auch als "DXGI **SWAP EFFECT \_ \_ \_ SEQUENTIAL"** bezeichnet) verwenden. das "blt"-Modell), ist es an der Zeit, anzuhalten!

Wechseln zu **DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL** oder DXGI SWAP EFFECT FLIP DISCARD (auch als "DXGI **SWAP EFFECT FLIP \_ \_ \_ \_ DISCARD"** bezeichnet). das Flip-Modell) bietet eine bessere Leistung, einen geringeren Energieverbrauch und eine umfangreichere Reihe von Features. (Weitere Informationen zu diesen Werten finden Sie unter [DXGI \_ SWAP \_ EFFECT-Enumeration.)](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)

Die Darstellung des Flip-Modells geht so weit, dass der Fenstermodus im Vergleich zum klassischen exklusiven Vollbildmodus effektiv gleichwertig oder besser ist. Tatsächlich möchten Sie vielleicht überlegen, ob Ihre Anwendung tatsächlich einen exklusiven Vollbildmodus benötigt, da die Vorteile eines rahmenlosen Flipmodellfensters schnellere Alt-Tab Wechseln und eine bessere Integration mit modernen Anzeigefunktionen umfassen.

Warum jetzt? Vor dem Update vom April 2018 konnte das vorgestellte Blt-Modell bei Verwendung in Hybrid-GPU-Konfigurationen, die häufig in High-End-Laptops verwendet werden, zu sichtbaren Löschungen führen (siehe [KB 3158621](https://support.microsoft.com/help/3158621/hybrid-graphics-and-vsync-results-in-graphic-tearing-in-some-games-and)). Im April 2018-Update wurde diese Löschung auf Kosten einiger zusätzlicher Arbeit behoben. Wenn Sie blt-Darstellungen mit hohen Frameraten über Hybrid-GPUs hinweg durchführen, insbesondere bei hohen Auflösungen wie 4K, kann sich diese zusätzliche Arbeit auf die Gesamtleistung auswirken. Um die beste Leistung auf diesen Systemen zu gewährleisten, wechseln Sie von blt zum Flip-Present-Modell. Erwägen Sie außerdem, die Auflösung Ihrer Swapkette zu reduzieren, insbesondere, wenn sie nicht der primäre Punkt der Benutzerinteraktion ist (wie dies häufig bei VR-Vorschaufenstern der Fall ist).

## <a name="a-brief-history"></a>Ein kurzer Verlauf

Was ist das Flip-Modell? Was ist die Alternative?

Vor Windows 7 war die einzige Möglichkeit, Inhalte aus D3D darzustellen, "blt" oder in eine Oberfläche zu kopieren, die sich im Besitz des Fensters oder Bildschirms befand. Beginnend mit dem FLIPEX-Swapeffekt von D3D9 und dem Einstieg in DXGI über den FLIP \_ SEQUENTIAL-Swap-Effekt in Windows 8 haben wir eine effizientere Möglichkeit entwickelt, Inhalte auf den Bildschirm zu stellen, indem wir sie direkt mit dem Desktop-Compositor freigeben, mit minimalen Kopien. Eine allgemeine Übersicht über die Technologie finden Sie unter [DXGI-Flip-Modell.](dxgi-flip-model.md)

Diese Optimierung ist dank des DWM (Desktopfenster-Manager) möglich, bei dem es sich um den Compositor handelt, der den Windows Desktop steuert.

## <a name="when-should-i-use-the-blt-model"></a>Wann sollte ich das blt-Modell verwenden?

Es gibt eine Funktion, die das Flip-Modell nicht bereitstellt: die Fähigkeit, mehrere verschiedene APIs zu erstellen, die Inhalte erzeugen, die alle zusammen in demselben **HWND** zusammengefasst sind, auf einer vorhandenen Basis. Ein Beispiel hierfür wäre die Verwendung von D3D zum Zeichnen eines Fensterhintergrunds und dann [Windows GDI,](/windows/desktop/gdi/windows-gdi) um etwas darüber zu zeichnen, oder die Verwendung von zwei verschiedenen Grafik-APIs oder zwei Swapchains aus derselben API, um abwechselnde Frames zu erzeugen. Wenn Sie keine Interop auf **HWND-Ebene** zwischen Grafikkomponenten benötigen, benötigen Sie kein blt-Modell.

Es gibt eine zweite Funktion, die nicht im ursprünglichen Flip-Modellentwurf bereitgestellt wurde, aber jetzt verfügbar ist. Dies ist die Möglichkeit, in einer ungedrosselten Framerate darzustellen. Für eine Anwendung, die das Synchronisierungsintervall 0 verwendet, empfiehlt es sich nicht, zum Flip-Modell zu wechseln, es sei denn, die [IDXGIFactory5::CheckFeatureSupport-API](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) ist verfügbar und meldet Unterstützung für **DXGI \_ FEATURE PRESENT \_ ALLOW \_ \_ TEARING.** Dieses Feature ist nahezu überall in aktuellen Versionen von Windows 10 und auf moderner Hardware verfügbar.

## <a name="directflip"></a>DirectFlip

Wenn Sie [DirectX 12: Präsentationsmodi in Windows 10](https://www.youtube.com/watch?v=E3wTajGZOsA)gesehen haben, sehen Sie, wie Sie über "Direct Flip" und "Independent Flip" sprechen. Dies sind Optimierungen, die für Anwendungen mit Flip-Modell-Swapchains aktiviert sind. Abhängig von der Fenster- und Pufferkonfiguration ist es möglich, die Desktopkomposition vollständig zu umgehen und Anwendungsframes auf die gleiche Weise direkt an den Bildschirm zu senden wie der exklusive Vollbildmodus.

Heutzutage können diese Optimierungen in einem von drei Szenarien verwendet werden, um die Funktionalität zu erhöhen:

1.  **DirectFlip:** Ihre Swapchainpuffer entsprechen den Bildschirmdimensionen, und der Fensterclientbereich deckt den Bildschirm ab. Anstatt die DWM-Swapkette für die Anzeige auf dem Bildschirm zu verwenden, wird die Anwendungstauschkette verwendet.
2.  **DirectFlip mit Panelpasser:** Ihre Fensterclientregion deckt den Bildschirm ab, und Ihre Swapchainpuffer befinden sich innerhalb eines hardwareabhängigen Skalierungsfaktors (z.B. 0,25x bis 4x) des Bildschirms. Die GPU-Scanouthardware wird verwendet, um Ihren Puffer beim Senden an die Anzeige zu skalieren.
3.  **DirectFlip mit MPO (Multi-Plane Overlay):** Ihre Swapchainpuffer befinden sich innerhalb eines hardwareabhängigen Skalierungsfaktors Ihrer Fensterdimensionen. Der DWM kann eine dedizierte Hardwareüberprüfungsebene für Ihre Anwendung reservieren, die dann gescannt und möglicherweise auf einen alphageblendeten Unterbereich des Bildschirms gestreckt wird.

Mit dem Flip-Modell mit Fenstern kann die Anwendung die Hardwareunterstützung für verschiedene DirectFlip-Szenarien abfragen und verschiedene Arten der dynamischen Skalierung implementieren, wobei [IDXGIOutput6::CheckHardwareCompositionSupport verwendet wird.](/windows/desktop/api/DXGI1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport) Ein Zu beachtender Nachteil ist, dass es möglich ist, dass der Cursor bei Verwendung von Panelpassern Stretching-Nebeneffekte erleidet, was über **DXGI \_ HARDWARE COMPOSITION SUPPORT FLAG CURSOR \_ \_ \_ \_ \_ STRETCHED** angegeben wird.

Sobald Ihre Swapkette "DirectF msid" ist, kann der DWM in den Standbymodus versetzt werden und nur aktiviert werden, wenn sich außerhalb Ihrer Anwendung etwas ändert. Ihre Anwendungsframes werden unabhängig voneinander direkt an den Bildschirm gesendet, mit der gleichen Effizienz wie die exklusive Vollbildanzeige. Dies ist "Independent Flip" und kann in allen oben genannten Szenarien verwendet werden. Wenn andere Desktopinhalte an oberster Stelle stehen, kann der DWM entweder nahtlos zurück in den zusammengesetzten Modus wechseln, den Inhalt vor dem Flippen effizient "in umgekehrter Reihenfolge" zusammenstellen oder MPO nutzen, um den unabhängigen Flip-Modus beizubehalten.

Sehen Sie sich das [PresentMon-Tool](https://github.com/GameTechDev/PresentMon) an, um einen Einblick in die oben genannten Verwendungen zu erhalten.

## <a name="what-else-is-new-in-the-flip-model"></a>Welche weiteren Neuerungen gibt es im Flip-Modell?

Zusätzlich zu den oben genannten Verbesserungen, die für Standard-Swapchains ohne besonderen Zweck gelten, stehen mehrere Features zur Verfügung, die von Flip-Modellanwendungen verwendet werden können:

-   Verringern der Latenz mit **DXGI \_ SWAP CHAIN FLAG FRAME \_ \_ \_ \_ LATENCY \_ WAITABLE \_ OBJECT**. Wenn Sie sich im unabhängigen Flip-Modus befinden, können Sie bei aktuellen Versionen von Windows auf einen Latenzrahmen herunterkommen, mit einem ordnungsgemäßen Fallback auf das mögliche Minimum, wenn sie zusammengesetzt werden.
    -   Einschränkung: Es gab ein Problem, das mindestens zwei Latenzframes im Windows 10 Anniversary Update und früher ergeben hat. Weitere Informationen finden Sie in [diesem Forumthema.](https://www.gamedev.net/forums/topic/686507-windows-10-dx12-low-latency-tearing-free-rendering/) Dies wird im Fall Creator es Update behoben.
-   **DXGI \_ SWAP \_ EFFECT \_ FLIP \_ DISCARD** ermöglicht einen Modus für die "umgekehrte Komposition" des direkten Flip, was zu weniger Gesamtarbeit führt, um den Desktop anzuzeigen. Der DWM kann die Anwendungspuffer abschneiden und diese an den Bildschirm senden, anstatt eine vollständige Kopie in ihre eigenen Swapketten auszuführen.
-   **DXGI \_ SWAP \_ CHAIN FLAG ALLOW \_ \_ \_ TEARING** kann sogar in einem Fenster auf Systemen mit Überlagerungsunterstützung mit mehreren Ebenen eine noch geringere Latenz als das wartebare Objekt ermöglichen.
-   Anwendungen haben die Kontrolle über die Inhaltsskalierung, die während der Größenänderung des Fensters erfolgt. Dabei wird die [DXGI \_ SCALING-Eigenschaft](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling) verwendet, die während der Erstellung der Swapchain festgelegt wurde.
-   Inhalte in HDR-Formaten (R10G10B10A2 \_ UNORM oder R16G16B16A16 \_ FLOAT) werden nur mit einem SDR-Desktop zusammengestellt.
-   Aktuelle Statistiken sind im Fenstermodus verfügbar.
-   Es besteht eine höhere Kompatibilität mit dem UWP-Anwendungsmodell (Universal Windows Platform) und DX12, da diese nur mit dem Flip-Modell kompatibel sind.

## <a name="what-do-i-have-to-do-to-use-the-flip-model"></a>Was muss ich tun, um das Flip-Modell zu verwenden?

Flip-Modellaustauschketten haben zusätzlich zu blt-Swapchains einige zusätzliche Anforderungen:

1.  Die Pufferanzahl muss mindestens 2 sein.
2.  Nach [Present-Aufrufen](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) muss der Backpuffer explizit an den unmittelbaren D3D11-Kontext gebunden werden, bevor er erneut verwendet werden kann.
3.  Nach dem Aufruf von [SetFullscreenState](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)muss die Anwendung [ResizeBuffers](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) vor **Present** aufrufen.
4.  MSAA-Swapketten (Multisample-Antialiasing) werden im Flip-Modell nicht direkt unterstützt, sodass die Anwendung eine MSAA-Auflösung durchführen muss, bevor die **Present** ausgegeben wird.

## <a name="how-to-choose-the-right-rendering-and-presentation-resolutions"></a>Auswählen der richtigen Rendering- und Präsentationsauflösungen

Das herkömmliche Muster für Anwendungen in der Vergangenheit war es, dem Benutzer eine Liste von Lösungen zur Auswahl zu geben, wenn der Benutzer den exklusiven Vollbildmodus auswählt. Mit der Möglichkeit moderner Anzeigen, inhalte nahtlos zu skalieren, sollten Sie erwägen, Benutzern die Möglichkeit zu geben, eine Renderingauflösung für die Leistungsskalierung auszuwählen, unabhängig von einer Ausgabeauflösung und sogar im Fenstermodus. Darüber hinaus sollten Anwendungen **IDXGIOutput6::CheckHardwareCompositionSupport** nutzen, um zu bestimmen, ob der Inhalt vor der Präsentation skaliert werden muss oder ob die Hardware die Skalierung für sie durchführen soll.

Ihre Inhalte müssen möglicherweise im Rahmen des aktuellen Oder Kompositionsvorgangs von einer GPU zu einer anderen migriert werden. Dies gilt häufig für Laptops mit mehreren GPU oder Systeme mit externen GPUs, die angeschlossen sind. Wenn diese Konfigurationen häufiger verwendet werden und die Anzeige mit hoher Auflösung immer häufiger wird, steigen die Kosten für die Darstellung einer vollständigen Auflösungstauschkette. Wenn das Ziel Ihrer Swapkette nicht der primäre Punkt der Benutzerinteraktion ist, wie es häufig bei VR-Titeln der Fall ist, die eine 2D-Vorschau der VR-Szene in einem sekundären Fenster darstellen, erwägen Sie die Verwendung einer Swapkette mit niedrigerer Auflösung, um die Bandbreite zu minimieren, die über verschiedene GPUs übertragen werden muss.

## <a name="other-considerations"></a>Weitere Überlegungen

Das erste Mal, wenn Sie die GPU zum Schreiben in den Swapchainbackpuffer auffordern, ist die Zeit, in der die GPU angehalten wird und darauf wartet, dass der Puffer verfügbar wird. Verzögern Sie diesen Punkt nach Möglichkeit so weit wie möglich in den Rahmen.

 

 
