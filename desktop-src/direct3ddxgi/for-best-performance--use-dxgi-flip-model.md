---
description: Dieses Thema enthält Anleitungen für Entwickler zur Maximierung der Leistung und Effizienz im Präsentations Stapel auf modernen Versionen von Windows.
ms.assetid: B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1
title: Verwenden Sie zum erzielen der optimalen Leistung DXGI-Flip-Modell.
ms.topic: article
ms.date: 05/31/2018
ms.custom: RS5
ms.openlocfilehash: 2a1e671c03f468fd62b0b5bad0f008f84e62ca3c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343130"
---
# <a name="for-best-performance-use-dxgi-flip-model"></a>Verwenden Sie zum erzielen der optimalen Leistung DXGI-Flip-Modell.

Dieses Thema enthält Anleitungen für Entwickler zur Maximierung der Leistung und Effizienz im Präsentations Stapel auf modernen Versionen von Windows. Dabei geht es um das [DXGI-Flip-Modell](dxgi-flip-model.md), [DirectX 12: präsentationsmodi in Windows 10 (Video)](https://www.youtube.com/watch?v=E3wTajGZOsA)und [Präsentations Erweiterungen in Windows 10: ein frühes aussehen (Video)](https://www.youtube.com/watch?v=nUZVV_mssWQ) .

## <a name="call-to-action"></a>Handlungsaufforderung

Wenn Sie weiterhin **DXGI- \_ Swap- \_ Effekt \_ verwerfen** oder **DXGI- \_ Swap- \_ Effekt \_ sequenziell** verwenden (auch als Das "BLT"-Modell), es ist Zeit, den Vorgang zu unterbinden.

Wechseln zum **DXGI- \_ Swap- \_ Effekt \_ kippen \_ sequenziell** oder **DXGI- \_ Swap- \_ Effekt \_ kippen kippen \_** (auch bekannt als Das Flip-Modell) bietet eine bessere Leistung, geringeren Energieverbrauch und einen umfassenderen Satz an Features. (Weitere Informationen zu diesen Werten finden Sie unter [DXGI \_ Swap \_ Effect-Enumeration](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) .)

Modell Darstellung kippen geht so weit, dass der Fenster-Modus im Vergleich zum klassischen Fullscreen-Modus effektiv Äquivalent oder besser ist. In der Tat sollten Sie überprüfen, ob Ihre Anwendung tatsächlich einen exklusiven Vollbildmodus benötigt, da die Vorteile eines randlose-Fensters für das Kippen des Modells schnellere Alt-Tab wechseln und eine bessere Integration in moderne Anzeigefunktionen umfassen.

Warum jetzt? Vor dem Update vom April 2018 konnten BLT-Modell Darstellung zu einem sichtbaren zerreißen führen, wenn Sie in Hybrid-GPU-Konfigurationen verwendet werden, die häufig in High-End-Laptops gefunden werden (siehe [KB 3158621](https://support.microsoft.com/help/3158621/hybrid-graphics-and-vsync-results-in-graphic-tearing-in-some-games-and)). Im Update vom April 2018 wurde dieses zerreißen behoben, was wiederum zu einer zusätzlichen Arbeit hat. Wenn Sie BLT-Vorschauen bei hohen Frameraten über Hybrid-GPUs machen, insbesondere bei hohen Auflösungen wie 4K, kann sich diese zusätzliche Arbeit auf die Gesamtleistung auswirken. Um die beste Leistung für diese Systeme zu gewährleisten, wechseln Sie vom BLT zum aktuellen Modell. Außerdem sollten Sie die Auflösung ihrer SwapChain reduzieren, insbesondere dann, wenn dies nicht der primäre Punkt der Benutzerinteraktion ist (was häufig bei den VR-Vorschau Fenstern der Fall ist).

## <a name="a-brief-history"></a>Ein kurzer Verlauf

Was ist das Flip-Modell? Was ist die Alternative?

Vor Windows 7 war die einzige Möglichkeit zum präsentieren von Inhalten aus D3D das "BLT" oder das Kopieren in eine Oberfläche, die sich im Besitz des Fensters oder des Bildschirms befand. Beginnend mit dem D3D9's flipex-swapffekt und dem Wechsel zu DXGI durch den \_ sequenziellen Swap-Effekt in Windows 8 haben wir eine effizientere Möglichkeit zum Platzieren von Inhalten auf dem Bildschirm entwickelt, indem wir Sie direkt mit dem Desktop-Compositor mit minimalen Kopien teilen. Eine allgemeine Übersicht über die Technologie finden Sie unter [DXGI Flip Model](dxgi-flip-model.md) .

Diese Optimierung ist dank der DWM (Desktopfenster-Manager) möglich, bei der es sich um den Compositor handelt, der den Windows-Desktop steuert.

## <a name="when-should-i-use-the-blt-model"></a>Wann sollte ich das BLT-Modell verwenden?

Es gibt eine Funktion, die das Flip-Modell nicht bereitstellt: die Möglichkeit, mehrere verschiedene APIs zu erzeugen, die Inhalte erzeugen, die sich auf der aktuellen Ebene im gleichen **HWND** befinden. Ein Beispiel hierfür wäre die Verwendung von D3D, um einen Fenster Hintergrund zu zeichnen, und dann [Windows GDI](/windows/desktop/gdi/windows-gdi) , um etwas auf der obersten Ebene zu zeichnen, oder zwei verschiedene Grafik-APIs oder zwei SwapChain-Objekte aus derselben API zu verwenden, um abwechselnde Frames zu erstellen. Wenn Sie keine Interop auf **HWND**-Ebene zwischen Grafik Komponenten benötigen, benötigen Sie kein BLT-Modell.

Es gibt ein zweites Element, das nicht im ursprünglichen Modell für das Kippen von Modellen bereitgestellt wurde, aber jetzt verfügbar ist. Dies ist die Möglichkeit, sich bei einem nicht gedrossten Framerate zu präsentieren. Für eine Anwendung, die das Synchronisierungs Intervall 0 verwendet, empfiehlt es sich nicht, zu einem kippen-Modell zu wechseln, es sei denn, die [IDXGIFactory5:: checkfeaturesupport](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) -API ist verfügbar, und die Unterstützung für die **DXGI- \_ Funktion \_ \_ \_** ist Diese Funktion ist in den neuesten Versionen von Windows 10 und auf moderner Hardware nahezu universell.

## <a name="directflip"></a>Directflip

Wenn Sie [DirectX 12: präsentationsmodi in Windows 10](https://www.youtube.com/watch?v=E3wTajGZOsA)gesehen haben, werden Sie über "Direktes kippen" und "unabhängige kippen" erfahren. Dies sind Optimierungen, die für Anwendungen aktiviert sind, die SwapChain-Modelle kippen. Abhängig von der Fenster-und Puffer Konfiguration ist es möglich, die Desktop Komposition vollständig zu umgehen und Anwendungs Frames direkt an den Bildschirm zu senden, und zwar auf dieselbe Weise wie bei exklusiven Vollbild.

Heutzutage können diese Optimierungen in einem von drei Szenarien in der Reihenfolge, in der die Funktionalität erhöht wird, eintreten:

1.  **Directflip**: Ihre vorhandenes SwapChain-Puffer entsprechen den Bildschirm Abmessungen, und Ihr Fenster Client Bereich deckt den Bildschirm ab. Anstatt die DWM-vorhandenes SwapChain für die Anzeige auf dem Bildschirm zu verwenden, wird die vorhandenes SwapChain-Anwendung verwendet.
2.  **Directflip mit Panel-fittern**: der Fenster Client Bereich deckt den Bildschirm ab, und ihre vorhandenes SwapChain-Puffer befinden sich innerhalb eines Hardware abhängigen Skalierungsfaktors (z. b. 0,25 x bis 4X) des Bildschirms. Die GPU-scanout-Hardware wird zum Skalieren Ihres Puffers beim Senden an die Anzeige verwendet.
3.  **Directflip mit multiebenenoverlay (MPO)**: Ihre vorhandenes SwapChain-Puffer befinden sich innerhalb eines Hardware abhängigen Skalierungsfaktors ihrer Fenster Dimensionen. Die DWM kann eine dedizierte Hardware-scanout-Ebene für Ihre Anwendung reservieren. diese wird dann ausgecheckt und potenziell auf eine Alpha gemischte Unterregion des Bildschirms gestreckten.

Mit dem Modell für das Fenster "Kippen" kann die Anwendung Hardwareunterstützung für verschiedene directflip-Szenarien Abfragen und mithilfe von [IDXGIOutput6:: checkhardwarecompositionsupport](/windows/desktop/api/DXGI1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport)verschiedene dynamische Skalierungs Typen implementieren. Beachten Sie, dass bei der Nutzung von Panel-fittern es möglich ist, dass der Cursor Auswirkungen auf die Streckung von Nebeneffekten hat, was über die **\_ \_ \_ Unterstützung der \_ \_ Cursor \_ Streckung der DXGI-Hardware Komposition** angegeben wird.

Wenn die vorhandenes SwapChain "directflipped" ist, kann die DWM in den Standbymodus wechseln und nur dann reaktivieren, wenn sich etwas außerhalb der Anwendung ändert. Ihre Anwendungsrahmen werden unabhängig voneinander direkt an den Bildschirm gesendet, mit der gleichen Effizienz wie Vollbild Exclusive. Dies ist "unabhängige kippen" und kann in allen oben aufgeführten Szenarien eintreten. Wenn andere Desktop Inhalte im Vordergrund stehen, kann die DWM entweder nahtlos in den zusammengesetzten Modus übergehen, den Inhalt auf der Grundlage der Anwendung auf effiziente Weise "umkehren", bevor Sie gekippt wird, oder MPO nutzen, um den unabhängigen Flip-Modus aufrechtzuerhalten.

Sehen Sie sich das [presentmon](https://github.com/GameTechDev/PresentMon) -Tool an, um zu erfahren, welche der oben genannten verwendet wurde.

## <a name="what-else-is-new-in-the-flip-model"></a>Welche weiteren Neuerungen gibt es im Flip-Modell?

Zusätzlich zu den oben genannten Verbesserungen, die sich auf Standard-SwapChain ohne besondere Besonderheiten beziehen, stehen mehrere Features für das Kippen von Modell Anwendungen zur Verwendung zur Verfügung:

-   Verringern der Latenzzeit mithilfe von DXGI-SwapChain-Flag zum Auslagern der **\_ \_ \_ \_ Rahmen \_ Latenz \_ \_** Wenn Sie sich im unabhängigen Flip-Modus befinden, können Sie bei den aktuellen Versionen von Windows auf einen Latenz Bereich mit einem ordnungsgemäßen Fall Back auf das minimal mögliche zurückgreifen.
    -   Einschränkungen: Es ist ein Problem aufgetreten, das mindestens zwei Latenzzeiten in Windows 10 Anniversary Update und früher ergab. Weitere Informationen finden Sie in [diesem Forumsthema](https://www.gamedev.net/forums/topic/686507-windows-10-dx12-low-latency-tearing-free-rendering/) . Dies wird bei der Aktualisierung des Fall Erstellers korrigiert.
-   **DXGI \_ \_Swapffekt \_ Flip \_ DISCARD** ermöglicht den Modus "umgekehrte Komposition" von Direct Flip. Dies führt zu einer geringeren Gesamtarbeit, um den Desktop anzuzeigen. Die DWM kann die Anwendungs Puffer schreiben und diese an den Bildschirm senden, anstatt eine vollständige Kopie in ihren eigenen Swapketten auszuführen.
-   **DXGI \_ Das Auslagerungs \_ Ketten \_ Flag zum Zulassen von \_ \_ Tränen** kann eine noch geringere Latenz als das Objekt mit Aktivier barkeit ermöglichen, auch in einem Fenster auf Systemen mit über Lagerungs Unterstützung mit mehreren Ebenen.
-   Anwendungen haben die Kontrolle über die Skalierung von Inhalten, die [während der Größen \_ ](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling) Änderung von Fenstern erfolgt
-   Der Inhalt in den HDR-Formaten (R10G10B10A2 \_ unorm oder R16G16B16A16 \_ float) wird nicht gebunden, es sei denn, er ist auf einem SZR-Desktop zusammengesetzt.
-   Aktuelle Statistiken sind im Fenstermodus verfügbar.
-   Die Kompatibilität mit dem UWP-Anwendungsmodell (universelle Windows-Plattform) und DX12 ist stärker kompatibel, da diese nur mit dem Flip-Modell kompatibel sind.

## <a name="what-do-i-have-to-do-to-use-the-flip-model"></a>Was muss ich tun, um das Flip-Modell zu verwenden?

Für das Kippen von Modell-SwapChain gelten einige zusätzliche Anforderungen zusätzlich zu BLT SwapChain:

1.  Die Puffer Anzahl muss mindestens 2 betragen.
2.  Nach dem [vorhanden](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) sein von aufrufen muss der Hintergrund Puffer explizit an den unmittelbaren D3D11-Kontext gebunden werden, bevor er wieder verwendet werden kann.
3.  Nach dem Aufruf von [setfullscreenstate](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)muss die Anwendung [resizebuffers](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) vor dem **vorhanden** sein.
4.  MSAA (Multisample Anti-Aliasing) SwapChain werden im Flip-Modell nicht direkt unterstützt, sodass die Anwendung eine MSAA-Auflösung ausführen muss, bevor die **vorhandene** ausgegeben wird.

## <a name="how-to-choose-the-right-rendering-and-presentation-resolutions"></a>Auswählen der richtigen Rendering-und Präsentations Auflösungen

Das herkömmliche Muster für Anwendungen in der Vergangenheit war die Bereitstellung einer Liste von Auflösungen, aus denen der Benutzer den exklusiven Vollbildmodus auswählt. Mit der Fähigkeit moderner Anzeige, Inhalte nahtlos zu skalieren, sollten Sie Benutzern die Möglichkeit geben, eine renderinglösung für die Leistungsskalierung unabhängig von einer Ausgabeauflösung und sogar im Fenstermodus auszuwählen. Darüber hinaus sollten Anwendungen **IDXGIOutput6:: checkhardwarecompositionsupport** nutzen, um zu bestimmen, ob Sie den Inhalt vor dem präsentieren skalieren müssen, oder ob die Hardware die Skalierung für die Hardware durchführen soll.

Der Inhalt muss möglicherweise im Rahmen des vorhandenen-oder Kompositions Vorgangs von einer GPU zu einer anderen migriert werden. Dies gilt häufig für multigpu-Laptops oder Systeme, bei denen externe GPUs angeschlossen sind. Wenn diese Konfigurationen allgemeiner werden, und wenn die Anzeige mit hoher Auflösung häufiger wird, erhöht sich der Aufwand für die Darstellung einer vollständigen Auflösung von vorhandenes SwapChain. Wenn das Ziel ihrer vorhandenes SwapChain nicht der primäre Punkt der Benutzerinteraktion ist, wie es häufig bei VR-Titeln der Fall ist, die eine 2D-Vorschau der VR-Szene in einem sekundären Fenster darstellen, sollten Sie die Verwendung einer niedrigeren Auflösungs-vorhandenes SwapChain in Erwägung nehmen, um die Bandbreite zu minimieren, die über verschiedene GPUs übertragen werden muss.

## <a name="other-considerations"></a>Andere Aspekte

Wenn Sie die GPU zum ersten Mal zum Schreiben in den vorhandenes SwapChain-Hintergrund Puffer auffordern, ist dies der Zeitpunkt, zu dem die GPU warten wird, bis der Puffer verfügbar wird. Verzögern Sie diesen Punkt nach Möglichkeit so weit wie möglich in den Frame.

 

 
