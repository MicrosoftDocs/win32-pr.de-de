---
description: Windows 8 bietet Unterstützung für das Flip Presentation Model und die zugehörigen aktuellen Statistiken in DXGI 1,2.
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: DXGI-Flip-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ee82febd13a3b57a06d93fd01eb8d230d6b78a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860310"
---
# <a name="dxgi-flip-model"></a>DXGI-Flip-Modell

Windows 8 bietet Unterstützung für das Flip Presentation Model und die zugehörigen aktuellen Statistiken in DXGI 1,2. Das DXGI Flip Presentation-Modell von Windows 8 ähnelt der Darstellung des [Direct3D 9Ex-Flip-Modus](../direct3darticles/direct3d-9ex-improvements.md)von Windows 7. Auf Video-oder Frameraten basierende Präsentations-apps wie Spiele können am meisten von der Verwendung eines Flip Presentation-Modells profitieren. Apps, die das DXGI Flip Presentation-Modell verwenden, verringern die Auslastung der Systemressourcen und erhöhen die Leistung. Apps können auch die aktuellen Statistik Erweiterungen mit dem Flip Presentation Model verwenden, um die Präsentations Rate besser zu steuern, indem Sie Echtzeitfeedback und Korrekturmechanismen bereitstellen.

-   [Vergleich zwischen dem DXGI-Flip-Modell und dem BitBLT-Modell](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [Verwenden des DXGI-Flip-Modells](#how-to-use-dxgi-flip-model)
-   [Frame Synchronisierung von DXGI-Flip Model-apps](#frame-synchronization-of-dxgi-flip-model-apps)
-   [Vermeiden, erkennen und Wiederherstellen von Störungen](#avoiding-detecting-and-recovering-from-glitches)
-   [Zugehörige Themen](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>Vergleich zwischen dem DXGI-Flip-Modell und dem BitBLT-Modell

Die Laufzeit verwendet die Bitblock Übertragung (BitBLT) und die Flip Presentation-Modelle, um Grafik Inhalte auf Anzeige Monitoren darzustellen. Der größte Unterschied zwischen den BitBlt-und der Flip Presentation-Modellen besteht darin, wie Hintergrund Puffer Inhalte für die Komposition in Windows 8 DWM gelangen. Im BitBLT-Modell werden die Inhalte des backpuffers bei jedem [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)auf die Umleitungs Oberfläche kopiert. Im Flip-Modell werden alle Back Puffer für den Desktopfenster-Manager (DWM) freigegeben. Aus diesem Grund kann der DWM-Vorgang direkt von diesen Back Puffern ohne zusätzliche Kopiervorgänge verfasst werden. Im Allgemeinen ist das Flip-Modell effizienter. Das Flip-Modell bietet auch weitere Funktionen, z. b. Erweiterte aktuelle Statistiken.

Wenn Sie über ältere Komponenten verfügen, die Windows Graphics Device Interface (GDI) verwenden, um direkt in ein [**HWND**](../winprog/windows-data-types.md) zu schreiben, verwenden Sie das BitBLT-Modell.

Leistungsverbesserungen des DXGI-Flip-Modells sind wichtig, wenn sich die APP im Fenstermodus befindet. In der Sequenz in dieser Tabelle und der Abbildung werden Speicher Bandbreiten-Verwendungen und System Lese-und Schreibvorgänge von Fenster Anwendungen verglichen, bei denen das Modell kippen im Vergleich zum BitBLT-Modell ausgewählt wird.



| Schritt | Für DWM vorhandenes BitBLT-Modell                                                                               | DXGI-Flip-Modell für DWM vorhanden                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | Die APP aktualisiert Ihren Frame (schreiben).<br/>                                                              | Die APP aktualisiert Ihren Frame (schreiben).<br/>                     |
| 2.   | Direct3D-Laufzeit kopiert Oberflächen Inhalte in eine DWM-Umleitungs Oberfläche (lesen, schreiben)<br/>            | Direct3D Runtime übergibt die APP-Oberfläche an DWM<br/>        |
| 3.   | Nachdem die freigegebene Oberflächen Kopie abgeschlossen ist, rendert DWM die APP-Oberfläche auf dem Bildschirm (lesen, schreiben)<br/> | DWM rendert die APP-Oberfläche auf dem Bildschirm (lesen, schreiben)<br/> |



 

![Abbildung eines Vergleichs zwischen dem BLT-Modell und dem Flip-Modell](images/blt-flip-mode-present.png)

Das Kippen-Modell reduziert die Systemspeicher Auslastung durch Verringern der Anzahl von Lese-und Schreibvorgängen durch die Direct3D-Laufzeit für die Zusammenstellung des Fensterrahmens durch DWM.

## <a name="how-to-use-dxgi-flip-model"></a>Verwenden des DXGI-Flip-Modells

Direct3D 11,1-apps, die auf Windows 8 abzielen, verwenden ein Flip-Modell, indem Sie die **SwapChain** mit dem [**DXGI- \_ \_ swapffekt-Wert \_ Flip \_ sequenzieller**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) Enumerationswert erstellen, der im SwapEffect-Member der [**\_ \_ \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) -Struktur Wenn Sie **SwapEffect** auf den **DXGI- \_ swapffekt als \_ \_ \_ sequenziell** festlegen, legen Sie auch diese Member der **DXGI- \_ \_ SwapChain \_ DESC1** auf die folgenden Werte fest:

-   **BUFFERCOUNT** auf einen Wert zwischen 2 und 16, um eine Leistungs Einbuße zu verhindern, weil darauf gewartet wird, dass DWM den vorherigen Präsentations Puffer freigibt.
-   **Format** im DXGI- \_ Format \_ R16G16B16A16 \_ float, DXGI- \_ Format \_ B8G8R8A8 \_ unorm oder DXGI- \_ Format \_ R8G8B8A8 \_ unorm
-   **Count** -Member der [**DXGI- \_ Beispiel \_**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) -Debug-Struktur, die vom **sampledebug** -Member an einen und der **Quality** -Member des DXGI-Samplingrate auf NULL festgelegt wird, da mehrere Sample Antialiasing (MSAA) nicht unterstützt werden. **\_ \_**

Wenn Sie [**DXGI- \_ \_ swapffekt \_ \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) bei Windows 7 oder einem älteren Betriebssystem als sequenziell verwenden, schlägt die Geräte Erstellung fehl. Wenn Sie das Modell "Kippen" verwenden, können Sie die voll Bild Anzeige im Fenstermodus verwenden. Das voll Bild Verhalten ist nicht betroffen. Wenn Sie **null** an den *pfullscreendebug* -Parameter von [**IDXGIFactory2:: anateswapchainforhwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) für eine Fensteraustausch Kette übergeben und **SwapEffect** auf den **DXGI- \_ Swap-Effekt in \_ \_ \_ sequenzieller Richtung** festlegen, erstellt die Laufzeit einen zusätzlichen Hintergrund Puffer und rotiert, welches Handle zu dem Puffer gehört, der zur Präsentationszeit zum vorderen Puffer wird.

Beachten Sie bei der Verwendung von Flip Model die folgenden Tipps:

-   Verwenden Sie eine kippen-Modell Austausch Kette pro [**HWND**](../winprog/windows-data-types.md). Verwenden Sie nicht mehrere Flip-Modell Austausch Ketten an dasselbe **HWND**.
-   Verwenden Sie keine Flip Model Swap-Kette mit der [**scrollwindow**](/windows/win32/api/winuser/nf-winuser-scrollwindow) -Funktion oder der [**scrollwindowex**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) -Funktion von GDI. Einige Direct3D-Apps verwenden die Funktionen **scrollwindow** und **scrollwindowex** von GDI zum Aktualisieren von Fenster Inhalten, nachdem ein Benutzer scrollereignis auftritt. **Scrollwindow** und **scrollwindowex** führen bitblts von Fenster Inhalten auf dem Bildschirm aus, während der Benutzer einen Bildlauf durchführt. Diese Funktionen erfordern auch BitBLT-Modell Updates für GDI-und Direct3D-Inhalte. Apps, die eine dieser Funktionen verwenden, zeigen nicht notwendigerweise sichtbare Fenster Inhalte an, die auf dem Bildschirm angezeigt werden, wenn sich die APP im Fenstermodus befindet. Es wird empfohlen, die Funktionen " **scrollwindow** " und " **scrollwindowex** " von GDI nicht zu verwenden, sondern stattdessen GDI-und Direct3D-Inhalte auf dem Bildschirm neu zu zeichnen
-   Verwenden Sie das Flip-Modell in einem [**HWND**](../winprog/windows-data-types.md) , das nicht auch von anderen APIs als Ziel verwendet wird, einschließlich DXGI BitBLT Presentation Model, Other Version of Direct3D oder GDI. Da das BitBLT-Modell eine zusätzliche Kopie der Oberfläche beibehält, können Sie GDI und andere Direct3D-Inhalte dem gleichen **HWND** hinzufügen, indem Sie schrittweise Updates von Direct3D und GDI ausführen. Wenn Sie das Flip-Modell verwenden, werden nur Direct3D-Inhalte in kippen Model-Austausch Ketten angezeigt, die die Laufzeit an DWM übergibt. Die Laufzeit ignoriert alle anderen BitBLT-Modell-Direct3D-oder GDI-Inhalts Updates.

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>Frame Synchronisierung von DXGI-Flip Model-apps

Aktuelle Statistiken sind Informationen zur Rahmen Zeit, die von Medien-Apps zum Synchronisieren von Video-und Audiodatenströmen und zum Wiederherstellen von Videowiedergabe-Störungen verwendet werden. Apps können die Informationen zur Rahmen Zeitangabe in der aktuellen Statistik verwenden, um die Präsentations Rate ihrer Video Frames für eine reibungslosere Darstellung anzupassen. Zum Abrufen der aktuellen Statistik Informationen rufen Sie die [**idxgiswapchain:: getframestatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) -Methode auf, um die Struktur der [**DXGI- \_ Frame \_ Statistik**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) abzurufen. **DXGI \_ Die Frame- \_ Statistik** enthält Statistiken zu [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) -aufrufen. Eine kippen-Modell Austausch Kette stellt die aktuellen Statistik Informationen sowohl im Fenstermodus als auch im Vollbildmodus bereit. Bei BitBLT-Modell Austausch Ketten im Fenstermodus sind alle **DXGI- \_ Frame \_ Statistik** Werte Nullen.

Für das Flip Model Present Statistics gibt [**idxgiswapchain:: getframestatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) in folgenden Situationen eine **Disjunktion der DXGI- \_ Fehler \_ Rahmen \_ Statistiken \_** zurück:

-   Erster [**getframestatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics)-Befehl, der den Anfang einer Sequenz angibt
-   Modusänderung: entweder der Fenstermodus zum oder vom Vollbildmodus oder vom Vollbildmodus bis zum voll Bild Übergang

Die Werte in den Elementen **presentfreshcount**, **synkrefreshcount** und **syncqpctime** der [**DXGI- \_ Frame \_ Statistiken**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) weisen die folgenden Eigenschaften auf:

-   **Presentfreshcount** ist gleich **synkrefreshcount** , wenn die APP bei jeder VSYNC angezeigt wird.
-   **Synkrefreshcount** wird im VSYNC-Intervall abgerufen, wenn der vorhandene gesendet wurde. **syncqpctime** ist ungefähr die Zeit, die dem VSYNC-Intervall zugeordnet ist.

Die [**idxgiswapchain:: getlastpresentcount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) -Methode gibt die letzte vorhandene Anzahl zurück, d. h. die aktuelle ID des letzten erfolgreichen [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) -Aufrufens von einem Anzeigegerät, das der Swapkette zugeordnet ist. Diese vorhandene ID ist der Wert des **presentcount** -Members der Struktur der [**DXGI- \_ Frame \_ Statistik**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) . Bei BitBLT-Modell Austausch Ketten werden im Fenstermodus alle **DXGI- \_ Frame \_ Statistik** Werte als Nullen angezeigt.

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>Vermeiden, erkennen und Wiederherstellen von Störungen

Führen Sie diese Schritte aus, um das Durchsuchen in der Frame Präsentation zu vermeiden, zu erkennen und wiederherzustellen:

1.  Queue [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) -Aufrufe (d. h. Aufrufen von **IDXGISwapChain1::P resent1** mehrmals, was dazu veranlasst, dass Sie in einer Warteschlange gesammelt werden).
2.  Erstellen Sie eine vorhandene Warteschlangen Struktur zum Speichern aller erfolgreich gesendeten [**IDXGISwapChain1::P**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)der vorhandenen ID (zurückgegeben von [**idxgiswapchain:: getlastpresentcount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)) und zugeordneten, berechneten/erwarteten **presenterfrischendes count** -Werten.
3.  So erkennen Sie einen Fehler:

    -   Aufrufen von [**idxgiswapchain:: getframestatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics).
    -   Für diesen Frame können Sie die aktuelle ID (**presentcount**) und die VSYNC-Anzahl anzeigen, bei der das Betriebssystem dem Monitor das letzte Bild angezeigt hat (**presenterfrischendes count**).
    -   Rufen Sie den erwarteten **presenterfrischend-Zähler** ab, der der aktuellen ID zugeordnet ist und die Sie zuvor in der Struktur der aktuellen Warteschlange gespeichert haben.
    -   Wenn die tatsächliche **presentaktuellem Anzahl** später als die erwartete **presenterfrischen-Anzahl** liegt, ist ein Fehler aufgetreten.

4.  So stellen Sie eine Wiederherstellung nach dem glitch durch:

    -   Berechnen Sie die Anzahl der Frames, die bei der Wiederherstellung nach dem glitch übersprungen werden. Wenn in Schritt 3 beispielsweise angezeigt wird, dass die erwartete VSYNC-Anzahl (**presenterfrischendes count**) für eine vorhandene ID (**presentcount**) 5 beträgt und die tatsächliche VSYNC-Anzahl für die vorhandene ID 8 ist, ist die Anzahl der zu über springenden Rahmen bei der Wiederherstellung aus dem Störung 3 Frames.
    -   Übergeben Sie 0 an den *syncinterval* -Parameter in dieser Anzahl von Aufrufen an [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , um diese Anzahl von Frames zu verwerfen und zu überspringen.

        > [!Note]  
        > Wenn das Störung aus einer großen Anzahl von Frames besteht, nennen Sie [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , wobei der *Flags* -Parameter auf [**DXGI \_ Present \_ Restart**](dxgi-present.md) festgelegt ist, um alle ausstehenden in der Warteschlange befindlichen Darstellung zu verwerfen und zu überspringen.

         

Im folgenden finden Sie ein Beispielszenario für die Wiederherstellung nach einem Fehler in der Frame Präsentation:

![Abbildung eines Beispiel Szenarios für die Wiederherstellung nach einem Fehler in der Frame Präsentation](images/frame-sync-glitch-recover.png)

Im Beispielszenario erwarten Sie, dass Frame a auf dem Bildschirm für die VSYNC-Anzahl 1 angezeigt wird. Sie erkennen aber tatsächlich den VSYNC-Zähler, dass Frame A auf dem Bildschirm 4 angezeigt wird. Daher können Sie feststellen, dass ein Fehler aufgetreten ist. Sie können dann drei Frames verwerfen, d. h., Sie können 0 an den *syncinterval* -Parameter in drei Aufrufen von [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)übergeben. Im vorangehenden Beispielszenario benötigen Sie zum Wiederherstellen nach dem glitch eine Summe von 8 **IDXGISwapChain1::P resent1** -aufrufen. Der 9. Frame wird dann gemäß der erwarteten VSYNC-Anzahl angezeigt.

Im folgenden finden Sie eine zeitanfolge von Präsentations Ereignissen. Jede vertikale Linie stellt eine VSYNC dar. Die horizontale Richtung ist die Zeit, die auf der rechten Seite zunimmt. Anhand der Abbildung können Sie sich vorstellen, wie Fehler auftreten können.

![Abbildung einer zeitanfolge der Präsentation eventsl](images/present-timeline.png)

Diese Sequenz wird in der Abbildung veranschaulicht:

1.  Die APP wird bei VSYNC reaktiviert, blau gerendert, [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)und dann wieder in den Standbymodus wechselt.
2.  Die Grafikverarbeitungseinheit (Graphics Processing Unit, GPU) wird aus dem Leerlauf aktiviert, führt das Rendering in blau aus und wechselt dann wieder in den Standbymodus.
3.  Die DWM wird bei der nächsten VSYNC reaktiviert, eine blaue in ihren Hintergrund Puffer setzt, [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)aufruft und dann wieder in den Standbymodus wechselt.
4.  Die APP wird reaktiviert, rendert grün, ruft [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)auf und wechselt dann wieder in den Standbymodus.
    > [!Note]  
    > Die APP wird gleichzeitig ausgeführt, während die GPU die Komposition von blau ausführt.

     

5.  Als nächstes rendert die GPU grün für die app.
6.  Zum Schluss zeigt der Digital to Analog Converter (DAC) die Ergebnisse der DWM-Komposition für den Monitor bei der nächsten VSYNC.

In der zeitanschlange können Sie sich die Latenz der aktuellen Statistiken und die Art der fehlerhafte Verwendung vorstellen. Wenn Sie z. b. einen DWM-Glitzer für die grüne Farbe anzeigen möchten, die auf dem Bildschirm angezeigt wird, stellen Sie sich vor, das grüne/rote Feld zu vergrößern, sodass die Rechte Seite des grünen/roten Felds mit der rechten Seite des lila/roten Felds übereinstimmt. In diesem Szenario zeigt die DAC zwei Rahmen blau und dann den grünen Rahmen an. Sie sehen, dass dieser Fehler beim Lesen der aktuellen Statistiken aufgetreten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern der Präsentation mit dem Flip-Modell, den geänderten Rechtecke und den Bereichen](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
