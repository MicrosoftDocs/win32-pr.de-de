---
title: Bewährte Methoden für die DirectX-Grafik Infrastruktur (DXGI)
description: In diesem Artikel werden wichtige Portierungsprobleme behandelt.
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f576368674d05af74e3161d4251301ebc066a489
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390773"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>DirectX-Grafik Infrastruktur (DXGI): bewährte Methoden

Microsoft DirectX Graphics Infrastructure (DXGI) ist ein neues Subsystem, das mit Windows Vista eingeführt wurde und einige der Low-Level-Aufgaben kapselt, die von Direct3D 10, 10,1, 11 und 11,1 benötigt werden. Aus der Perspektive eines Direct3D 9-Programmierers umfasst DXGI den größten Teil des Codes für Enumeration, Austausch Ketten Erstellung und Präsentation, der zuvor in die Direct3D 9-APIs gepackt wurde. Wenn Sie eine APP auf DXGI und Direct3D 10. x und Direct3D 11. x portieren, müssen Sie einige Überlegungen in Betracht ziehen, um sicherzustellen, dass der Prozess reibungslos verläuft.

In diesem Artikel werden wichtige Portierungsprobleme behandelt.

-   [Voll Bild Probleme](#full-screen-issues)
-   [Mehrere Monitore](#multiple-monitors)
-   [Fenster Stile und DXGI](#window-styles-and-dxgi)
-   [Multithreading und DXGI](#multithreading-and-dxgi)
-   [Gamma und DXGI](#gamma-and-dxgi)
-   [DXGI 1,1](#dxgi-11)
-   [DXGI 1,2](#dxgi-12)

## <a name="full-screen-issues"></a>Full-Screen Probleme

Beim Portieren von Direct3D 9 auf DXGI und Direct3D 10. x oder Direct3D 11. x können Probleme, die mit der Umstellung von windoting in den Vollbildmodus verbunden sind, häufig für Entwickler zu Problemen führen. Die Hauptprobleme treten auf, weil Direct3D 9-Anwendungen im Gegensatz zu DXGI-Anwendungen einen mehr praktischen Ansatz für die Nachverfolgung von Fenster Stilen und Fenster Zuständen erfordern. Wenn der modusändernde Code zur DXGI-Durchführung portiert wird, führt dies häufig zu unerwartetem Verhalten.

Häufig haben Direct3D 9 Anwendungen den Übergang in den Vollbildmodus übertragen, indem Sie die Auflösung des Front Puffers festgelegt haben, das Gerät in den Vollbildmodus für den exklusiven Modus versetzen und dann die Auflösung des backpuffers entsprechend festlegen. Ein separater Pfad wurde für Änderungen an der Fenstergröße verwendet, da Sie immer dann über den Fenster Prozess verwaltet werden mussten, wenn die Anwendung eine WM- \_ Größen Nachricht erhalten hat.

DXGI versucht, diesen Ansatz zu vereinfachen, indem die beiden Fälle kombiniert werden. Wenn der Fensterrahmen beispielsweise im Fenstermodus gezogen wird, erhält die Anwendung eine WM- \_ Größen Meldung. DXGI fängt diese Nachricht ab und passt automatisch die Größe des Front Puffers an. Die Anwendung muss lediglich [**idxgiswapchain:: resizebuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) aufrufen, um die Größe des Hintergrund Puffers auf die Größe zu ändern, die als Parameter in der WM-Größe übergeben wurde \_ . Ebenso kann die Anwendung, wenn Sie zwischen dem Vollbildmodus und dem Fenstermodus wechseln muss, einfach [**idxgiswapchain:: setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)aufrufen. DXGI ändert die Größe des Front Puffers, sodass er dem neu ausgewählten Vollbildmodus entspricht, und sendet eine WM- \_ Größen Meldung an die Anwendung. Die Anwendung ruft **resizebuffers** erneut auf, so wie es auch der Fall wäre, wenn der Fensterrahmen gezogen wurde.

Die Methodik der vorangehenden Erläuterung folgt einem sehr bestimmten Pfad. DXGI legt die voll Bildauflösung standardmäßig auf die Desktop Auflösung fest. Viele Anwendungen wechseln jedoch zu einer bevorzugten voll Bildauflösung. In einem solchen Fall stellt DXGI [**idxgiswapchain:: resizetarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)bereit. Dies sollte vor dem Aufruf von [**setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)aufgerufen werden. Obwohl diese Methoden in umgekehrter Reihenfolge aufgerufen werden können (zuerst **setfullscreenstate** , gefolgt von **resizetarget**), bewirkt dies, dass eine zusätzliche WM- \_ Größen Meldung an die Anwendung gesendet wird. (Dies kann auch zu einem Flimmern führen, da DXGI gezwungen werden kann, zwei Modusänderungen auszuführen.) Nach **dem Aufruf** von **setfullscreenstate** empfiehlt es sich, **resizetarget** erneut mit dem Element "aktualisierungsmitglied" des [**DXGI- \_ Modus " \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) " aufzurufen. Dies entspricht einer Anweisung ohne Vorgang in DXGI, kann jedoch Probleme mit der Aktualisierungsrate vermeiden, die im folgenden erläutert werden.

Im Vollbildmodus ist die Desktopfenster-Manager (DWM) deaktiviert. DXGI kann einen Flip-Vorgang ausführen, um den Hintergrund Pufferinhalt darzustellen, anstatt einen Blit zu verwenden, der im Fenstermodus ausgeführt würde. Dieser Leistungsgewinn kann rückgängig gemacht werden, wenn bestimmte Anforderungen nicht erfüllt werden. Um sicherzustellen, dass DXGI einen Flip anstelle eines Blits durchführt, muss der Vorder-und Hintergrund Puffer identisch sein. Wenn die Anwendung die Nachrichten der WM-Größe ordnungsgemäß verarbeitet \_ , sollte dies kein Problem darstellen. Außerdem müssen die Formate identisch sein.

Das Problem bei den meisten Anwendungen ist die Aktualisierungsrate. Die im aufruber von [**resizetarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) angegebene Aktualisierungsrate muss eine Aktualisierungsrate sein, die durch das [**idxgioutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) -Objekt, das die SwapChain verwendet, aufgelistet wird. DXGI kann diesen Wert automatisch berechnen, wenn die Anwendung den Aktualisier **enden Member des** [**DXGI- \_ Modus \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) , der an **resizetarget** übermittelt wird, nullt. Es ist wichtig, nicht davon auszugehen, dass bestimmte Aktualisierungs Raten immer unterstützt werden und einfach einen Wert hart codieren. Häufig wählen Entwickler 60 Hz als Aktualisierungsrate aus und wissen nicht, dass die aufgelistete Aktualisierungsrate des Monitors ungefähr 60.000/1.001 Hz vom Monitor ist. Wenn die Aktualisierungsrate nicht der erwarteten Aktualisierungsrate von 60 entspricht, wird DXGI gezwungen, ein Blit im Vollbildmodus anstelle eines kippen auszuführen.

Das letzte Problem, dem Entwickler häufig begegnen, ist das Ändern von Vollbildauflösungen im Vollbildmodus. Das Aufrufen von [**resizetarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) und [**setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) ist manchmal erfolgreich, aber die voll Bildauflösung bleibt die Desktop Auflösung. Außerdem können Entwickler eine voll Bildaustausch Kette erstellen und eine bestimmte Auflösung durchführen, um zu ermitteln, ob DXGI standardmäßig die Desktop Auflösung verwendet, unabhängig von den in der Übergabe angegebenen Zahlen. Sofern nicht anders festgelegt, verwendet DXGI standardmäßig die Desktop Auflösung für Vollbild-Austausch Ketten. Beim Erstellen einer Vollbild-Swapkette muss der Flag **-Member der** [**\_ \_ \_ DESC-Struktur der DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) -SwapChain auf [**DXGI- \_ SwapChain- \_ \_ Flag \_ zulassen \_ \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) festgelegt werden, um das Standardverhalten von DXGI zu überschreiben. Dieses Flag kann auch an **resizetarget** übermittelt werden, um diese Funktion dynamisch zu aktivieren oder zu deaktivieren.

## <a name="multiple-monitors"></a>Mehrere Monitore

Bei der Verwendung von DXGI mit mehreren Monitoren müssen zwei Regeln befolgt werden.

Die erste Regel gilt für die Erstellung von zwei oder mehr voll Bildaustausch Ketten auf mehreren Monitoren. Beim Erstellen solcher Austausch Ketten empfiehlt es sich, alle Austausch Ketten als Fenster zu erstellen und diese dann auf den voll Bildschirm festzulegen. Wenn Swapketten im Vollbildmodus erstellt werden, bewirkt die Erstellung einer zweiten Swapkette, dass eine Modusänderung an die erste Swapkette gesendet wird, was zu einer Beendigung des Vollbildmodus führen könnte.

Die zweite Regel gilt für Ausgaben. Achten Sie auf Ausgaben, die beim Erstellen von Austausch Ketten verwendet werden. Mit DXGI steuert das [**idxgioutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) -Objekt, welche Überwachung die Swapkette verwendet, wenn Sie in den Vollbildmodus versetzt wird. Anders als bei DXGI verfügte Direct3D 9 über kein Konzept der Ausgaben.

## <a name="window-styles-and-dxgi"></a>Fenster Stile und DXGI

Direct3D 9-Anwendungen waren bei Wechsel zwischen den Modi für den Vollbildmodus und den Fenster Umfang viel Arbeit zu erledigen. Der Großteil dieser Arbeit umfasste das Ändern von Fenster Stilen zum Hinzufügen und Entfernen von Rahmen, zum Hinzufügen von Scrollleisten usw. Wenn Anwendungen zu DXGI und Direct3D 10. x oder Direct3D 11. x portiert werden, bleibt dieser Code häufig bestehen. Abhängig von den vorgenommenen Änderungen kann das Wechseln zwischen Modi zu unerwartetem Verhalten führen. Wenn Sie z. b. zum Fenstermodus wechseln, verfügt die Anwendung möglicherweise nicht mehr über einen Fensterrahmen oder Fensterrahmen, obwohl Code vorhanden ist, der diese Formate speziell festlegt. Dies liegt daran, dass DXGI nun einen Großteil dieses Stils übernimmt, der sich selbst ändert. Die manuelle Einstellung von Fenster Stilen kann DXGI beeinträchtigen, was zu unerwartetem Verhalten führen kann.

Das empfohlene Verhalten besteht darin, so wenig Arbeit wie möglich zu tun und DXGI den größten Teil der Interaktion mit den Fenstern zu ermöglichen. Wenn die Anwendung jedoch Ihr eigenes windowingverhalten verarbeiten muss, kann [**idxgifactory:: makewindowassociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) verwendet werden, um DXGI mitzuteilen, dass die automatische Fenster Behandlung deaktiviert werden soll.

## <a name="multithreading-and-dxgi"></a>Multithreading und DXGI

Bei der Verwendung von DXGI in einer Multithread-Anwendung muss besonders darauf geachtet werden, dass keine Deadlocks auftreten. Aufgrund der engen Interaktion von DXGI mit windowingsendet Sie gelegentlich Fenster Meldungen an das zugehörige Anwendungsfenster. DXGI erfordert, dass die Fenster Änderungen erfolgen, bevor Sie fortgesetzt werden kann. Daher wird [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)verwendet, bei dem es sich um einen synchronen-Vorgang handelt. Die Anwendung muss die Fenster Meldung verarbeiten, bevor **SendMessage** zurückgegeben wird.

In einer Anwendung, in der DXGI-Aufrufe und die Nachrichten Pumpe sich im gleichen Thread (oder einer Single Thread-Anwendung) befinden, müssen nur wenige Schritte durchgeführt werden. Wenn sich der DXGI-Aufruf im gleichen Thread wie die nachrichtenpump befindet, ruft [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) das Fenster [*Windows proc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))auf. Dadurch wird die Meldungs Pumpe umgangen, und die Ausführung kann nach dem **aufrufsend von SendMessage** fortgesetzt werden. Beachten Sie, dass [**idxgiswapchain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) -Aufrufe, wie z. b. [**idxgiswapchain::P Resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present), auch als DXGI-Aufrufe angesehen werden. DXGI kann die Arbeit von [**resizebuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) oder [**resizetarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) verzögern, bis " **Present** " aufgerufen wird.

Wenn sich der DXGI-Rückruf und die nachrichtenpump in unterschiedlichen Threads befinden, muss darauf geachtet werden, dass Deadlocks vermieden werden. Wenn sich die nachrichtenpump und SendMessage in verschiedenen Threads befinden, fügt [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) der Nachrichten Warteschlange des Fensters eine Nachricht hinzu und wartet, bis das Fenster diese Nachricht verarbeitet. Wenn die Fenster Prozedur ausgelastet ist oder nicht von der nachrichtenpump aufgerufen wird, wird die Nachricht möglicherweise nie verarbeitet, und DXGI wartet unbegrenzt.

Wenn z. b. eine Anwendung, deren Meldungs Pump in einem Thread und deren Rendering auf einem anderen Thread angezeigt wird, den Modus ändern kann. Der Message Pump Thread weist den Renderingthread an, den Modus zu ändern, und wartet, bis die Modusänderung beendet ist. Der Renderingthread ruft jedoch DXGI-Funktionen auf, die wiederum [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)aufrufen, das blockiert, bis die Nachrichten Pumpe die Nachricht verarbeitet. Ein Deadlock tritt auf, weil beide Threads jetzt blockiert sind und aufeinander warten. Um dies zu vermeiden, blockieren Sie das nachrichtenpump nie. Wenn ein-Block unvermeidlich ist, sollten alle DXGI-Interaktionen im gleichen Thread wie das nachrichtenpump erfolgen.

## <a name="gamma-and-dxgi"></a>Gamma und DXGI

Obwohl Gamma in Direct3D 10. x oder Direct3D 11. x am besten mithilfe von sRGB-Texturen verarbeitet werden kann, kann die Gamma-Rampe für Entwickler nützlich sein, die einen anderen Gamma Wert als 2,2 verwenden möchten oder wenn Sie ein renderzielformat verwenden, das sRGB nicht unterstützt. Beachten Sie zwei Probleme beim Festlegen der Gamma-Rampe durch dxgi. Das erste Problem besteht darin, dass die in [**idxgioutput:: setgammacontrol eingegebenen**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) Ausgangswerte float-Werte und keine **Wort** Werte sind. Stellen Sie außerdem sicher, dass der von Direct3D 9 portierte Code nicht versucht, in **Word** -Werte zu konvertieren, bevor diese an **setgammacontrol** übergeben werden.

Das zweite Problem besteht darin, dass [**setgammacontrol**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) nach dem Wechsel in den Vollbildmodus möglicherweise nicht mehr funktioniert, abhängig vom verwendeten [**idxgioutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) -Objekt. Wenn Sie in den Vollbildmodus wechseln, erstellt DXGI ein neues Ausgabe Objekt und verwendet das-Objekt für alle nachfolgenden Vorgänge in der Ausgabe. Wenn **setgammacontrol** für eine Ausgabe aufgerufen wird, die vor einem Schalter im Vollbildmodus aufgezählt wird, wird der Aufruf nicht an die von DXGI aktuell verwendete Ausgabe weitergeleitet. Um dies zu vermeiden, müssen Sie [**idxgiswapchain:: getcontainingoutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) aufrufen, um die aktuelle Ausgabe abzurufen, und dann **setgammacontrol** für diese Ausgabe aufrufen, um das richtige Verhalten zu erhalten.

Informationen zum Verwenden der Gammakorrektur finden Sie unter [using Gammakorrektur](/windows/desktop/direct3ddxgi/using-gamma-correction).

## <a name="dxgi-11"></a>DXGI 1,1

Die Direct3D 11-Laufzeit, die in Windows 7 enthalten und auf Windows Vista (siehe [KB971644](https://support.microsoft.com/kb/971644)) installiert ist, enthält die Version 1,1 von dxgi. Mit diesem Update werden Definitionen für eine Reihe neuer Formate (insbesondere BGRA, 10-Bit x2 Bias und die BC6H-und bzw bc7-Textur Komprimierung von Direct3D 11) sowie eine neue Version der DXGI-Factory und Adapter Schnittstellen ([**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1), [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1), [**IDXGIAdapter1**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)) zum Auflisten von Remote Desktop Verbindungen hinzugefügt.

Wenn Sie Direct3D 11 verwenden, verwendet die Laufzeit standardmäßig DXGI 1,1, wenn [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) mit einem NULL- [**idxgiadapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) -Zeiger aufgerufen wird. Das Mischen der Verwendung von DXGI 1,0 und DXGI 1,1 im gleichen Prozess wird nicht unterstützt. Das Mischen von DXGI-Objektinstanzen aus verschiedenen Factorys im gleichen Prozess wird ebenfalls nicht unterstützt. Wenn Sie DirectX 11 verwenden, wird daher bei jeder expliziten Verwendung der DXGI-Schnittstellen eine [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) verwendet, die vom [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) -Einstiegspunkt in "DXGI.DLL" erstellt wurde, um sicherzustellen, dass die Anwendung immer DXGI 1,1 verwendet.

## <a name="dxgi-12"></a>DXGI 1,2

Die Direct3D 11,1-Runtime, die in Windows 8 enthalten ist, enthält auch Version 1,2 von dxgi.

DXGI 1,2 aktiviert diese Features:

-   Stereo-Rendering
-   16 Bit pro Pixel-Format

    -   DXGI \_ \_ -Format B5G6R5 \_ unorm-und DXGI- \_ Format \_ B5G5R5A1 \_ unorm werden jetzt vollständig unterstützt.
    -   ein neues DXGI- \_ Format \_ B5G5R5A1 \_ unorm-Format wurde hinzugefügt.

-   Videoformate
-   neue DXGI-Schnittstellen

Weitere Informationen zu DXGI 1,2-Features finden Sie unter [DXGI 1,2-Verbesserungen](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements).

 

 