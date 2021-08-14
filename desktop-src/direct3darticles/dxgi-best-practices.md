---
title: DirectX Graphic Infrastructure (DXGI) – Bewährte Methoden
description: In diesem Artikel werden wichtige Portierungsprobleme erläutert.
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be992fe2346868eb3481482325297a2c9ec27ee61bdd2c65f83b0f916fc22308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290237"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>DirectX Graphic Infrastructure (DXGI): Bewährte Methoden

Microsoft DirectX Graphic Infrastructure (DXGI) ist ein neues Subsystem, das mit Windows Vista eingeführt wurde und einige der aufgaben auf niedriger Ebene kapselt, die für Direct3D 10, 10.1, 11 und 11.1 erforderlich sind. Aus Sicht eines Direct3D 9-Programmierers umfasst DXGI den größten Teil des Codes für enumeration, swap-chain creation und presentation, der zuvor in die Direct3D 9-APIs gepackt war. Wenn Sie eine App zu DXGI und Direct3D 10.x und Direct3D 11.x portieren, müssen Sie einige Überlegungen berücksichtigen, um sicherzustellen, dass der Prozess reibungslos ausgeführt wird.

In diesem Artikel werden wichtige Portierungsprobleme erläutert.

-   [Vollbildprobleme](#full-screen-issues)
-   [Mehrere Monitore](#multiple-monitors)
-   [Fensterstile und DXGI](#window-styles-and-dxgi)
-   [Multithreading und DXGI](#multithreading-and-dxgi)
-   [Gamma und DXGI](#gamma-and-dxgi)
-   [DXGI 1.1](#dxgi-11)
-   [DXGI 1.2](#dxgi-12)

## <a name="full-screen-issues"></a>Full-Screen Probleme

Beim Portieren von Direct3D 9 auf DXGI und auf Direct3D 10.x oder Direct3D 11.x können Probleme im Zusammenhang mit dem Wechsel vom Fenstermodus in den Vollbildmodus häufig zu Problemen für Entwickler führen. Die Hauptprobleme treten auf, da Direct3D 9-Anwendungen im Gegensatz zu DXGI-Anwendungen einen praxisorientierten Ansatz zum Nachverfolgen von Fensterstilen und Fensterzuständen erfordern. Wenn der Code, der den Modus ändert, portiert wird, um auf DXGI ausgeführt zu werden, führt dies häufig zu unerwartetem Verhalten.

Häufig haben Direct3D 9-Anwendungen den Übergang in den Vollbildmodus verarbeitet, indem sie die Auflösung des Frontpuffers festgelegt, das Gerät in den exklusiven Vollbildmodus gezwungen und dann die Auflösung des Hintergrundpuffers auf Übereinstimmung festgelegt haben. Für Änderungen an der Fenstergröße wurde ein separater Pfad verwendet, da sie immer dann über den Fensterprozess verwaltet werden mussten, wenn die Anwendung eine WM \_ SIZE-Nachricht empfangen hat.

DXGI versucht, diesen Ansatz zu vereinfachen, indem die beiden Fälle kombiniert werden. Wenn der Fensterrahmen beispielsweise im Fenstermodus gezogen wird, empfängt die Anwendung eine WM \_ SIZE-Meldung. DXGI fängt diese Nachricht ab und passt automatisch die Größe des Frontpuffers an. Die Anwendung muss nur [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) aufrufen, um die Größe des Hintergrundpuffers auf die Größe zu ändern, die als Parameter in WM SIZE übergeben \_ wurde. Wenn die Anwendung zwischen Vollbildmodus und Fenstermodus wechseln muss, kann die Anwendung [**idXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)einfach aufrufen. DXGI passt die Größe des Frontpuffers an den neu ausgewählten Vollbildmodus an und sendet eine WM \_ SIZE-Nachricht an die Anwendung. Die Anwendung ruft erneut **ResizeBuffers auf,** genau wie beim Ziehen des Fensterrahmens.

Die Methodik der vorherigen Erklärung folgt einem sehr bestimmten Pfad. DXGI: Legen Sie die Vollbildauflösung standardmäßig auf die Desktopauflösung fest. Viele Anwendungen wechseln jedoch zu einer bevorzugten Vollbildauflösung. In diesem Fall bietet DXGI [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget). Dieser sollte aufgerufen werden, bevor [**SetFullscreenState aufgerufen wird.**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) Obwohl diese Methoden in umgekehrter Reihenfolge aufgerufen werden können (**SetFullscreenState** zuerst, gefolgt von **ResizeTarget**), führt dies dazu, dass eine zusätzliche WM SIZE-Nachricht an die Anwendung \_ gesendet wird. (Dies kann auch zu Flackern führen, da DXGI gezwungen werden könnte, zwei Modusänderungen durchzuführen.) Nach dem **Aufruf von SetFullscreenState** empfiehlt es sich, **ResizeTarget** erneut aufrufen, wenn das **RefreshRate-Member** von [**DXGI MODE \_ \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) auf null gesetzt ist. Dies entspricht einer Anweisung ohne Vorgang in DXGI, kann jedoch Probleme mit der Aktualisierungsrate vermeiden, die im Nächsten erläutert werden.

Im Vollbildmodus ist die Desktopfenster-Manager (DWM) deaktiviert. DXGI kann eine Kippung durchführen, um den Inhalt des Hintergrundpuffers anzuzeigen, anstatt einen Blit zu verwenden, was im Fenstermodus der Fall wäre. Dieser Leistungsgewinn kann jedoch rückgängig gemacht werden, wenn bestimmte Anforderungen nicht erfüllt werden. Um sicherzustellen, dass DXGI eine Kippung anstelle eines Blits vorschlägt, müssen der Frontpuffer und der Hintergrundpuffer identisch dimensioniert werden. Wenn die Anwendung ihre WM \_ SIZE-Meldungen ordnungsgemäß verarbeitet, sollte dies kein Problem darstellen. Außerdem müssen die Formate identisch sein.

Das Problem bei den meisten Anwendungen ist die Aktualisierungsrate. Die Aktualisierungsrate, die im Aufruf von [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) angegeben wird, muss eine Aktualisierungsrate sein, die vom [**IDXGIOutput-Objekt**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) aufzählt wird, das die Swapkette verwendet. DXGI kann diesen Wert automatisch berechnen, wenn die Anwendung das **RefreshRate-Member** von [**DXGI \_ MODE \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) ausrechent, das an **ResizeTarget übergeben wird.** Es ist wichtig, nicht davon auszugehen, dass bestimmte Aktualisierungsraten immer unterstützt werden, und einfach einen Wert hart zu coden. Entwickler wählen häufig 60 Hz als Aktualisierungsrate aus und wissen nicht, dass die aufzählte Aktualisierungsrate vom Monitor ungefähr 60.000/1.001 Hz vom Monitor beträgt. Wenn die Aktualisierungsrate nicht mit der erwarteten Aktualisierungsrate von 60 abschneiden kann, wird DXGI gezwungen, anstelle eines Kippens einen Blit im Vollbildmodus durchzuführen.

Das letzte Problem, mit dem Entwickler häufig konfrontiert sind, besteht in der Änderung der Vollbildauflösung, während sie im Vollbildmodus bleiben. Das [**Aufrufen von ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) [**und SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) ist manchmal erfolgreich, aber die Vollbildauflösung bleibt die Desktopauflösung. Außerdem können Entwickler eine Auslagerungskette im Vollbildmodus erstellen und eine bestimmte Auflösung geben, nur um zu finden, dass DXGI unabhängig von den übergebenen Zahlen standardmäßig die Desktopauflösung verwendet. Sofern nicht anders angegeben, verwendet DXGI standardmäßig die Desktopauflösung für Vollbild-Swapketten. Beim Erstellen einer Vollbild-Swapkette muss das **Flags-Member** der [**DXGI \_ SWAP CHAIN \_ \_ DESC-Struktur**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) auf [**DXGI SWAP CHAIN FLAG \_ ALLOW MODE \_ \_ \_ \_ \_ SWITCH**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) festgelegt werden, um das Standardverhalten von DXGI zu überschreiben. Dieses Flag kann auch an **ResizeTarget** übergeben werden, um diese Funktion dynamisch zu aktivieren oder zu deaktivieren.

## <a name="multiple-monitors"></a>Mehrere Monitore

Bei verwendung von DXGI mit mehreren Monitoren müssen zwei Regeln gelten.

Die erste Regel gilt für die Erstellung von zwei oder mehr Vollbild-Swapketten auf mehreren Monitoren. Wenn Sie solche Swapketten erstellen, ist es am besten, alle Swapketten im Fenstermodus zu erstellen und dann auf Vollbildmodus zu setzen. Wenn Austauschketten im Vollbildmodus erstellt werden, führt die Erstellung einer zweiten Austauschkette dazu, dass eine Modusänderung an die erste Austauschkette gesendet wird, was zur Beendigung des Vollbildmodus führen kann.

Die zweite Regel gilt für Ausgaben. Achten Sie auf Ausgaben, die beim Erstellen von Austauschketten verwendet werden. Mit DXGI verwendet das [**IDXGIOutput-Objektsteuerelemente,**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) die die Swapkette überwachen, wenn sie vollbildig wird. Im Gegensatz zu DXGI hatte Direct3D 9 kein Konzept von Ausgaben.

## <a name="window-styles-and-dxgi"></a>Fensterstile und DXGI

Direct3D 9-Anwendungen hatten viel Arbeit zu tun, wenn sie zwischen Vollbild- und Fenstermodus wechseln. Ein Teil dieser Arbeit war das Ändern von Fensterstilen zum Hinzufügen und Entfernen von Rahmen, zum Hinzufügen von Scrollleisten und so weiter. Wenn Anwendungen zu DXGI und Direct3D 10.x oder Direct3D 11.x portiert werden, bleibt dieser Code häufig erhalten. Abhängig von den vorgenommenen Änderungen kann das Wechseln zwischen Modi zu unerwartetem Verhalten führen. Wenn sie z. B. in den Fenstermodus wechselt, hat die Anwendung möglicherweise keinen Fensterrahmen oder Fensterrahmen mehr, obwohl sie über Code verfügen, der diese Stile speziell definiert. Dies liegt daran, dass DXGI jetzt einen großen Teil dieses Stils selbst verarbeitet. Das manuelle Festlegen von Fensterstilen kann DXGI beeinträchtigen und zu unerwartetem Verhalten führen.

Es wird empfohlen, so wenig Arbeit wie möglich zu unternehmen und DXGI die meisten Interaktionen mit den Fenstern zu ermöglichen. Wenn die Anwendung jedoch ihr eigenes Fensterverhalten verarbeiten muss, kann [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) verwendet werden, um DXGI an,einen Teil der automatischen Fensterbehandlung zu deaktivieren.

## <a name="multithreading-and-dxgi"></a>Multithreading und DXGI

Bei der Verwendung von DXGI in einer Multithreadanwendung ist besondere Vorsicht zu tun, um sicherzustellen, dass keine Deadlocks auftreten. Aufgrund der engen Interaktion von DXGI mit Windowing werden gelegentlich Fenstermeldungen an das zugeordnete Anwendungsfenster gesendet. DXGI muss die Fensteränderungen vornehmen, bevor sie fortgesetzt werden können. Daher wird [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)verwendet, bei dem es sich um einen synchronen Aufruf handelt. Die Anwendung muss die Fensternachricht verarbeiten, bevor **SendMessage zurückgegeben** wird.

In einer Anwendung, in der DXGI aufruft und sich die Nachrichtenpumpe im selben Thread (oder in einer Singlethreadanwendung) befindet, muss nur wenig getan werden. Wenn sich der DXGI-Aufruf im selben Thread wie der Message Pump befindet, ruft [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) die [*WindowProc des Fensters auf.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Dadurch wird der Nachrichtenpump umgangen, und die Ausführung kann nach dem Aufruf von **SendMessage fortgesetzt werden.** Denken Sie daran, dass [**IDXGISwapChain-Aufrufe**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) wie [**IDXGISwapChain::P resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)auch als DXGI-Aufrufe betrachtet werden. DXGI kann die Arbeit von [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) oder [**ResizeTarget zurückhalten,**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) bis **Present** aufgerufen wird.

Wenn sich der DXGI-Aufruf und das Nachrichtenpump in unterschiedlichen Threads befinden, müssen Sie darauf achten, Deadlocks zu vermeiden. Wenn sich message pump und SendMessage in verschiedenen Threads befinden, fügt [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) der Nachrichtenwarteschlange des Fensters eine Nachricht hinzu und wartet, bis das Fenster diese Nachricht verarbeiten kann. Wenn die Fensterprozedur ausgelastet ist oder nicht vom Nachrichtenpump aufgerufen wird, wird die Nachricht möglicherweise nie verarbeitet, und DXGI wartet unbegrenzt.

Wenn z. B. eine Anwendung, deren Meldungspump auf einem Thread und ihr Rendering in einem anderen Thread ausgeführt wird, die Modi ändern möchten. Der Message Pump-Thread weist den Renderingthread an, die Modi zu ändern, und wartet, bis die Modusänderung abgeschlossen ist. Der Renderingthread ruft jedoch DXGI-Funktionen auf, die wiederum [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)aufrufen, wodurch blockiert wird, bis die Nachricht vom Nachrichtenpump verarbeitet wird. Ein Deadlock tritt auf, weil beide Threads jetzt blockiert sind und aufeinander warten. Um dies zu vermeiden, blockieren Sie nie die Nachrichtenpumpe. Wenn ein Block unvermeidbar ist, sollten alle DXGI-Interaktionen im selben Thread wie der Nachrichtenpump erfolgen.

## <a name="gamma-and-dxgi"></a>Gamma und DXGI

Obwohl Gamma in Direct3D 10.x oder Direct3D 11.x am besten mit SRGB-Texturen behandelt werden kann, kann die Gamma-Rampe dennoch für Entwickler nützlich sein, die einen anderen Gammawert als 2.2 wünschen oder ein Renderzielformat verwenden, das SRGB nicht unterstützt. Beachten Sie beim Festlegen der Gamma-Rampe durch DXGI zwei Probleme. Das erste Problem ist, dass die an [**IDXGIOutput::SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) übergebenen Rampenwerte float-Werte und keine **WORD-Werte** sind. Stellen Sie außerdem sicher, dass der von Direct3D 9 portierte Code nicht versucht, in **WORD-Werte** zu konvertieren, bevor Sie diese an **SetGammaControl übergeben.**

Das zweite Problem ist, dass [**SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) nach dem Wechsel in den Vollbildmodus möglicherweise nicht funktioniert, abhängig vom verwendeten [**IDXGIOutput-Objekt.**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) Beim Wechsel in den Vollbildmodus erstellt DXGI ein neues Ausgabeobjekt und verwendet das -Objekt für alle nachfolgenden Vorgänge in der Ausgabe. Wenn **Sie SetGammaControl** für eine Ausgabe aufrufen, die vor einem Vollbildmodusschalter aufzählt wird, wird der Aufruf nicht an die Ausgabe geleitet, die DXGI derzeit verwendet. Um dies zu vermeiden, rufen Sie [**IDXGISwapChain::GetContainingOutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) auf, um die aktuelle Ausgabe zu erhalten, und rufen Sie **dann SetGammaControl** aus dieser Ausgabe auf, um das richtige Verhalten zu erhalten.

Informationen zur Verwendung der Gammakorrektur finden Sie unter [Verwenden der Gammakorrektur.](/windows/desktop/direct3ddxgi/using-gamma-correction)

## <a name="dxgi-11"></a>DXGI 1.1

Die in Windows 7 enthaltene und auf Windows Vista installierte Direct3D 11-Runtime (siehe [KB971644)](https://support.microsoft.com/kb/971644)enthält Version 1.1 von DXGI. Dieses Update fügt Definitionen für eine Reihe neuer Formate (insbesondere BGRA, 10-Bit X2-Bias und BC6H- und BC7-Texturkomprimierung von Direct3D 11) sowie eine neue Version der DXGI-Factory- und Adapterschnittstellen [**(CreateDXGIFactory1,**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) [**IDXGIFactory1,**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) [**IDXGIAdapter1)**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)zum Aufzählen von Remotedesktopverbindungen hinzu.

Wenn Sie Direct3D 11 verwenden, verwendet die Runtime standardmäßig DXGI 1.1 beim Aufrufen von [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) mit einem [**NULL-IDXGIAdapter-Zeiger.**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) Die Verwendung von DXGI 1.0 und DXGI 1.1 im selben Prozess wird nicht unterstützt. Das Mischen von DXGI-Objektinstanzen aus verschiedenen Factorys im selben Prozess wird ebenfalls nicht unterstützt. Wenn Sie DirectX 11 verwenden, verwendet daher jede explizite Verwendung der DXGI-Schnittstellen eine [**IDXGIFactory1,**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) die vom [**Einstiegspunkt CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) in "DXGI.DLL" erstellt wurde, um sicherzustellen, dass die Anwendung immer DXGI 1.1 verwendet.

## <a name="dxgi-12"></a>DXGI 1.2

Die Direct3D 11.1-Runtime, die in Windows 8 enthalten ist, enthält auch Version 1.2 von DXGI.

DXGI 1.2 ermöglicht die folgenden Features:

-   Stereorendering
-   16-Bit-pro-Pixel-Formate

    -   DXGI \_ FORMAT \_ B5G6R5 \_ UNORM und DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM werden jetzt vollständig unterstützt
    -   Ein neues DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM-Format wurde hinzugefügt.

-   Videoformate
-   Neue DXGI-Schnittstellen

Weitere Informationen zu DXGI 1.2-Features finden Sie unter [DXGI 1.2 Improvements](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements).

 

 