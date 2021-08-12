---
description: Windows 8 fügt Unterstützung für das Flip-Präsentationsmodell und die zugehörigen aktuellen Statistiken in DXGI 1.2 hinzu.
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: DXGI Flip-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b4b4cf8f792a23d4d32e5cb4b4273594745283cb803a638ea3d0cf4c45977f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289442"
---
# <a name="dxgi-flip-model"></a>DXGI Flip-Modell

Windows 8 fügt Unterstützung für das Flip-Präsentationsmodell und die zugehörigen aktuellen Statistiken in DXGI 1.2 hinzu. das DXGI-Flip-Präsentationsmodell von Windows 8 ähnelt Windows 7 [direct3D 9EX Flip Mode Presentation](../direct3darticles/direct3d-9ex-improvements.md). Video- oder Bildfrequenzbasierte Präsentations-Apps wie Spiele können am meisten von der Verwendung des Flip-Präsentationsmodells profitieren. Apps, die das DXGI-Flip-Präsentationsmodell verwenden, reduzieren die Auslastung der Systemressourcen und steigern die Leistung. Apps können auch aktuelle Statistikverbesserungen mit dem Flip-Präsentationsmodell verwenden, um die Präsentationsrate durch Bereitstellen von Echtzeitfeedback und Korrekturmechanismen besser zu steuern.

-   [Vergleichen des DXGI-Flip-Modells mit dem BitBlt-Modell](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [Verwenden des DXGI-Flip-Modells](#how-to-use-dxgi-flip-model)
-   [Framesynchronisierung von DXGI-Flip-Modell-Apps](#frame-synchronization-of-dxgi-flip-model-apps)
-   [Vermeiden, Erkennen und Wiederherstellen von Störungen](#avoiding-detecting-and-recovering-from-glitches)
-   [Zugehörige Themen](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>Vergleichen des DXGI-Flip-Modells mit dem BitBlt-Modell

Die Runtime verwendet die Bitblockübertragungs- (bitblt) und Flip-Präsentationsmodelle, um Grafikinhalte auf Anzeigemonitoren darzustellen. Der größte Unterschied zwischen bitblt- und flip-Präsentationsmodellen besteht darin, wie Backpufferinhalte zur Komposition zum Windows 8 DWM gelangen. Im bitblt-Modell wird der Inhalt des Hintergrundpuffers bei jedem Aufruf von [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)in die Umleitungsoberfläche kopiert. Im Flip-Modell werden alle Hintergrundpuffer für die Desktopfenster-Manager (DWM) freigegeben. Daher kann der DWM ohne zusätzliche Kopiervorgänge direkt aus diesen Rückpuffern zusammensetzen. Im Allgemeinen ist das Flip-Modell effizienter. Das Flip-Modell bietet auch weitere Features, z. B. erweiterte aktuelle Statistiken.

Wenn Sie über Legacykomponenten verfügen, die Windows Graphics Device Interface (GDI) verwenden, um direkt in ein [**HWND**](../winprog/windows-data-types.md) zu schreiben, verwenden Sie das bitblt-Modell.

Leistungsverbesserungen des DXGI-Flip-Modells sind wichtig, wenn sich die App im Fenstermodus befindet. Die Sequenz in dieser Tabelle und die Abbildung vergleichen die Speicherbandbreitennutzung und die Systemlese- und -schreibvorgänge von Fenster-Apps, die das Flip-Modell auswählen, mit dem Bitblt-Modell.



| Schritt | BitBlt-Modell für DWM vorhanden                                                                               | DXGI flip model present to DWM                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | Die App aktualisiert ihren Frame (Schreiben).<br/>                                                              | Die App aktualisiert ihren Frame (Schreiben).<br/>                     |
| 2.   | Direct3D-Runtime kopiert Oberflächeninhalte auf eine DWM-Umleitungsoberfläche (Lesen, Schreiben).<br/>            | Direct3D-Runtime übergibt die App-Oberfläche an DWM<br/>        |
| 3.   | Nach Abschluss der Kopie der freigegebenen Oberfläche rendert DWM die App-Oberfläche auf dem Bildschirm (Lesen, Schreiben).<br/> | DWM rendert die App-Oberfläche auf dem Bildschirm (Lesen, Schreiben)<br/> |



 

![Abbildung eines Vergleichs des Blt-Modells und des Flip-Modells](images/blt-flip-mode-present.png)

Das Flip-Modell reduziert die Systemspeicherauslastung, indem die Anzahl der Lese- und Schreibvorgänge durch die Direct3D-Runtime für die Framekomposition im Fenster durch DWM reduziert wird.

## <a name="how-to-use-dxgi-flip-model"></a>Verwenden des DXGI-Flip-Modells

Direct3D 11.1-Apps, die Windows 8 flip model verwenden, indem sie die Swapkette mit dem [**DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL-Enumerationswert**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) erstellen, der im **SwapEffect-Member** der [**DXGI SWAP CHAIN \_ \_ \_ DESC1-Struktur**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) festgelegt ist. Wenn Sie **SwapEffect** auf **DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL** festlegen, legen Sie auch diese Member von **DXGI SWAP CHAIN \_ \_ \_ DESC1** auf die angegebenen Werte fest:

-   **BufferCount** auf einen Wert zwischen 2 und 16, um leistungseinbußen zu vermeiden, da dwm darauf wartet, den vorherigen Präsentationspuffer freizugeben.
-   **Formatieren** in DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT, DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM oder DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM
-   **Count** member of the [**DXGI \_ SAMPLE \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) structure that the **SampleDesc** member specifies to one and the **Quality** member of **DXGI \_ SAMPLE \_ DESC** to zero because multiple sample antialiasing (MSAA) is not supported

Wenn Sie [**DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) auf Windows 7 oder früheren Betriebssystemen verwenden, tritt bei der Geräteerstellung ein Fehler auf. Wenn Sie das Flip-Modell verwenden, können Sie die im Fenstermodus vorhandenen Statistiken im Vollbildmodus verwenden. Das Vollbildverhalten ist nicht betroffen. Wenn Sie **NULL** an den *pFullscreenDesc-Parameter* von [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) für eine Swapkette mit Fenstern übergeben und **SwapEffect** auf **DXGI SWAP EFFECT FLIP \_ \_ \_ \_ SEQUENTIAL** festlegen, erstellt die Laufzeit einen zusätzlichen Hintergrundpuffer und rotiert das handle, das zum Puffer gehört, der zur Präsentationszeit zum Frontpuffer wird.

Wenn Sie das Flip-Modell verwenden, beachten Sie die folgenden Tipps:

-   Verwenden Sie eine Flip-Modell-Swapkette pro [**HWND.**](../winprog/windows-data-types.md) Richten Sie sich nicht an mehrere Flip-Modell-Swapketten für den gleichen **HWND.**
-   Verwenden Sie keine Swapkette für Flip-Modelle mit der [**ScrollWindow-**](/windows/win32/api/winuser/nf-winuser-scrollwindow) oder [**ScrollWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) von GDI. Einige Direct3D-Apps verwenden die GDI-Funktionen **ScrollWindow** und **ScrollWindowEx,** um den Inhalt des Fensters zu aktualisieren, nachdem ein Benutzerbildlaufereignis aufgetreten ist. **ScrollWindow** und **ScrollWindowEx** führen Bitblts von Fensterinhalten auf dem Bildschirm aus, während der Benutzer in einem Fenster scrollt. Diese Funktionen erfordern auch Bitblt-Modellupdates für GDI- und Direct3D-Inhalte. Apps, die eine der beiden Funktionen verwenden, zeigen nicht unbedingt sichtbare Fensterinhalte an, die auf dem Bildschirm scrollen, wenn sich die App im Fenstermodus befindet. Es wird empfohlen, die Funktionen **ScrollWindow** und **ScrollWindowEx** von GDI nicht zu verwenden und stattdessen GDI- und Direct3D-Inhalte auf dem Bildschirm neu zu zeichnen, um scrollen zu können.
-   Verwenden Sie das Flip-Modell in einem [**HWND,**](../winprog/windows-data-types.md) das nicht auch für andere APIs vorgesehen ist, z. B. DXGI-Bitblt-Präsentationsmodell, andere Versionen von Direct3D oder GDI. Da das Bitblt-Modell eine zusätzliche Kopie der Oberfläche beibehält, können Sie GDI- und andere Direct3D-Inhalte dem gleichen **HWND** durch teilliche Updates von Direct3D und GDI hinzufügen. Wenn Sie das Flip-Modell verwenden, sind nur Direct3D-Inhalte in Swapketten des Flipmodells sichtbar, die die Laufzeit an DWM übergibt. Die Runtime ignoriert alle anderen Bitblt-Modellupdates für Direct3D- oder GDI-Inhalte.

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>Framesynchronisierung von DXGI-Flip-Modell-Apps

Aktuelle Statistiken sind Frame-Timing-Informationen, die Medien-Apps verwenden, um Video- und Audiostreams zu synchronisieren und nach Störungen bei der Videowiedergabe wiederherzustellen. Apps können die Frame-Timing-Informationen in aktuellen Statistiken verwenden, um die Präsentationsrate ihrer Videoframes für eine reibungslose darstellung anzupassen. Um aktuelle Statistikinformationen abzurufen, rufen Sie die [**IDXGISwapChain::GetFrameStatistics-Methode**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) auf, um die [**DXGI \_ FRAME \_ STATISTICS-Struktur**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) abzurufen. **DXGI \_ FRAME \_ STATISTICS** enthält Statistiken zu [**IDXGISwapChain1::P resent1-Aufrufen.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) Eine Swapkette für Flip-Modelle stellt sowohl im Fenstermodus als auch im Vollbildmodus aktuelle Statistikinformationen bereit. Bei Bitblt-Modellaustauschketten im Fenstermodus sind alle **DXGI \_ FRAME \_ STATISTICS-Werte** Nullen.

Für aktuelle Statistiken des Flip-Modells gibt [**IDXGISwapChain::GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) **DXGI \_ ERROR FRAME \_ STATISTICS \_ \_ DISJOINT** in folgenden Situationen zurück:

-   Erster Aufruf von [**GetFrameStatistics,**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics)der den Anfang einer Sequenz angibt
-   Modusänderung: Entweder im Fenstermodus oder von Vollbild- oder Vollbild- zu Vollbildübergängen

Die Werte in **den Membern PresentRefreshCount,** **SyncRefreshCount** und **SyncQPCTime** von [**DXGI \_ FRAME \_ STATISTICS**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) weisen die folgenden Merkmale auf:

-   **PresentRefreshCount** ist gleich **SyncRefreshCount,** wenn die App auf jeder vsync dargestellt wird.
-   **SyncRefreshCount** wird im vsync-Intervall abgerufen, als das aktuelle übermittelt wurde. **SyncQPCTime** entspricht ungefähr der Zeit, die dem vsync-Intervall zugeordnet ist.

Die [**IDXGISwapChain::GetLastPresentCount-Methode**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) gibt die letzte aktuelle Anzahl zurück, d.h. die aktuelle ID des letzten [**erfolgreichen IDXGISwapChain1::P resent1-Aufrufs,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) der von einem Anzeigegerät erfolgt ist, das der Swapkette zugeordnet ist. Diese aktuelle ID ist der Wert des **PresentCount-Elements** der [**DXGI \_ FRAME \_ STATISTICS-Struktur.**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) Bei Bitblt-Modellaustauschketten sind im Fenstermodus alle **DXGI \_ FRAME \_ STATISTICS-Werte** Nullen.

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>Vermeiden, Erkennen und Wiederherstellen von Störungen

Führen Sie diese Schritte aus, um Störungen in der Framepräsentation zu vermeiden, zu erkennen und nach diesen wiederherzustellen:

1.  [**Warteschlangen-IDXGISwapChain1::P resent1-Aufrufe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (d.b. **mehrmals IDXGISwapChain1::P resent1** aufrufen, wodurch sie in einer Warteschlange erfasst werden).
2.  Erstellen Sie eine present-queue-Struktur, um alle erfolgreich [**übermittelten IDXGISwapChain1::P resent1-Id**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)(zurückgegeben von [**IDXGISwapChain::GetLastPresentCount)**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)und die zugehörigen, berechneten/erwarteten **PresentRefreshCount-Werte** zu speichern.
3.  So erkennen Sie eine Störung:

    -   Rufen Sie [**IDXGISwapChain::GetFrameStatistics auf.**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics)
    -   Für diesen Frame erhalten Sie die aktuelle ID (**PresentCount**) und die vsync-Anzahl, bei der das Betriebssystem dem Monitor das letzte Image angezeigt hat (**PresentRefreshCount**).
    -   Rufen Sie das erwartete **PresentRefreshCount** ab, das der aktuellen ID zugeordnet ist und die Sie zuvor in der Present-Queue-Struktur gespeichert haben.
    -   Wenn das tatsächliche **PresentRefreshCount-Element** höher als das erwartete **PresentRefreshCount-Element** ist, ist eine Störung aufgetreten.

4.  So stellen Sie die Wiederherstellung nach der Störung her:

    -   Berechnen Sie die Anzahl der Frames, die bei der Wiederherstellung nach der Störung übersprungen werden sollen. Wenn beispielsweise Schritt 3 ergibt, dass die erwartete vsync-Anzahl (**PresentRefreshCount**) für eine aktuelle ID (**PresentCount**) 5 und die tatsächliche vsync-Anzahl für die aktuelle ID 8 ist, beträgt die Anzahl der Frames, die zur Wiederherstellung nach der Störung übersprungen werden sollen, 3 Frames.
    -   Übergeben Sie 0 an den *SyncInterval-Parameter* in dieser Anzahl von Aufrufen von [**IDXGISwapChain1::P resent1,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) um diese Anzahl von Frames zu verwerfen und zu überspringen.

        > [!Note]  
        > Wenn die Störung aus einer großen Anzahl von Frames besteht, rufen [**Sie IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) auf, wobei der *Flags-Parameter* auf [**DXGI \_ PRESENT \_ RESTART**](dxgi-present.md) festgelegt ist, um alle ausstehenden Präsentierten in der Warteschlange zu verwerfen und zu überspringen.

         

Hier sehen Sie ein Beispielszenario für die Wiederherstellung nach Störungen in der Framepräsentation:

![Abbildung eines Beispielszenarios für die Wiederherstellung nach Störungen in der Framepräsentation](images/frame-sync-glitch-recover.png)

Im Beispielszenario erwarten Sie, dass Frame A auf dem Bildschirm mit einer vsync-Anzahl von 1 angezeigt wird. Tatsächlich erkennen Sie jedoch die vsync-Anzahl, dass Frame A auf dem Bildschirm als 4 angezeigt wird. Daher stellen Sie fest, dass eine Störung aufgetreten ist. Sie können dann drei Frames verwerfen, d.h. Sie können 0 in drei Aufrufen von [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)an den *SyncInterval-Parameter* übergeben. Im vorherigen Beispielszenario benötigen Sie insgesamt 8 **IDXGISwapChain1::P resent1-Aufrufe,** um nach der Störung wiederherzustellen. Der 9. Frame wird dann gemäß der erwarteten vsync-Anzahl angezeigt.

Hier ist eine Zeitzeile mit Präsentationsereignissen. Jede vertikale Linie stellt eine vsync dar. Die horizontale Richtung ist die Zeit, die nach rechts zunimmt. Anhand der Abbildung können Sie sich vorstellen, wie Störungen auftreten können.

![Abbildung einer Zeitlinie von Präsentationsereignissenl](images/present-timeline.png)

Die Abbildung veranschaulicht diese Sequenz:

1.  Die App aktiviert vsync, rendert blau, ruft [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)auf und wechselt dann wieder in den Ruhezustand.
2.  Die Grafikverarbeitungseinheit (GPU) wird aus dem Leerlauf aktiviert, führt das Rendern in Blau aus und wechselt dann wieder in den Standbymodus.
3.  Der DWM wird bei der nächsten vsync aktiviert, erstellt blau in seinem Hintergrundpuffer, ruft [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)auf und wechselt dann wieder in den Standbymodus.
4.  Die App wird aktiviert, wird grün gerendert, ruft [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)auf und wechselt dann wieder in den Ruhezustand.
    > [!Note]  
    > Die App wird gleichzeitig ausgeführt, während die GPU die Blau-Erstellung ausführt.

     

5.  Als Nächstes wird die GPU für die App grün gerendert.
6.  Schließlich zeigt der digitale zu analoge Konverter (Digital to Analog Converter, DAC) ergebnisse der DWM-Komposition auf dem Monitor bei der nächsten vsync an.

In der Zeitlinie können Sie sich die Latenz der aktuellen Statistiken und die Art und Weise vorstellen, wie Störungen auftreten können. Um beispielsweise eine DWM-Störung für die grüne Farbe anzuzeigen, die auf dem Bildschirm angezeigt wird, stellen Sie sich vor, das grüne/rote Feld zu erweitern, sodass die rechte Seite des grün/rot-Felds rechts vom violetten/roten Feld übereinstimmt. In diesem Szenario zeigt die DAC zwei blaue Und dann den grünen Rahmen an. Sie können sehen, dass diese Störung beim Lesen vorhandener Statistiken aufgetreten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern der Darstellung mit dem Flip-Modell, den geänderten Rechtecke und scrollbaren Bereichen](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
