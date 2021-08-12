---
title: Direct3D 11 on 12
description: D3D11On12 ist ein Mechanismus, mit dem Entwickler D3D11-Schnittstellen und -Objekte verwenden können, um die D3D12-API zu steuern.
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a67c7e0cd3592d35af80f280fc9f1893f4741fcadcc73afd3753880bccda3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530228"
---
# <a name="direct3d-11-on-12"></a>Direct3D 11 on 12

D3D11On12 ist ein Mechanismus, mit dem Entwickler D3D11-Schnittstellen und -Objekte verwenden können, um die D3D12-API zu steuern. D3D11on12 ermöglicht es Komponenten, die mit D3D11 geschrieben wurden (z.B. D2D-Text und -Benutzeroberfläche), mit Komponenten zusammenzuarbeiten, die für die D3D12-API geschrieben wurden. D3D11on12 ermöglicht auch die inkrementelle Portierung einer Anwendung von D3D11 zu D3D12, indem Teile der App der Einfachheit halber weiterhin D3D11 als Ziel verwenden können, während andere D3D12 für die Leistung verwenden, während sie immer über vollständiges und korrektes Rendering verfügen. D3D11On12 vereinfacht die Verwendung von Interop-Techniken, um Ressourcen freizugeben und die Arbeit zwischen den beiden APIs zu synchronisieren.

-   [Initialisieren von D3D11On12](#initializing-d3d11on12)
-   [Beispielverwendung](#example-usage)
-   [Hintergrund](#background)
-   [Bereinigen](#cleaning-up)
-   [Einschränkungen](#limitations)
-   [APIs](#apis)
-   [Zugehörige Themen](#related-topics)

## <a name="initializing-d3d11on12"></a>Initialisieren von D3D11On12

Um mit der Verwendung von D3D11On12 zu beginnen, besteht der erste Schritt darin, ein D3D12-Gerät und eine Befehlswarteschlange zu erstellen. Diese Objekte werden als Eingabe für die Initialisierungsmethode [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice)bereitgestellt. Sie können sich diese Methode als Erstellen eines D3D11-Geräts mit dem imaginären Treibertyp D3D \_ DRIVER \_ TYPE \_ 11ON12 vorstellen, wobei der D3D11-Treiber für das Erstellen von Objekten und das Übermitteln von Befehlslisten an die D3D12-API zuständig ist.

Nachdem Sie über ein D3D11-Gerät und einen unmittelbaren Kontext verfügen, können Sie `QueryInterface` das Gerät für die [**ID3D11On12Device-Schnittstelle**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) deaktivieren. Dies ist die primäre Schnittstelle, die für die Interop zwischen D3D11 und D3D12 verwendet wird. Damit sowohl der D3D11-Gerätekontext als auch die D3D12-Befehlslisten für dieselben Ressourcen ausgeführt werden, müssen Sie mithilfe der [**CreateWrappedResource-API**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) "umschlossene Ressourcen" erstellen. Diese Methode "heraufgestuft" eine D3D12-Ressource, um in D3D11 verständlich zu sein. Eine umschlossene Ressource beginnt im Zustand "acquired", einer Eigenschaft, die von den [**Methoden AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) und [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) bearbeitet wird.

## <a name="example-usage"></a>Beispielverwendung

Die typische Verwendung von D3D11On12 wäre die Verwendung von D2D zum Rendern von Text oder Bildern auf einem D3D12-Hintergrundpuffer. Beispielcode finden Sie im Beispiel D3D11On12. Hier finden Sie eine grobe Übersicht über die erforderlichen Schritte:

-   Erstellen Sie ein D3D12-Gerät ([**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)) und eine D3D12-Swapkette ([**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) mit einer [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) als Eingabe).
-   Erstellen Sie ein D3D11On12-Gerät mithilfe des D3D12-Geräts und derselben Befehlswarteschlange wie die Eingabe.
-   Rufen Sie die Puffer der Swapkette zurück, und erstellen Sie D3D11-Umschlossene Ressourcen für jeden dieser Puffer. Der verwendete Eingabezustand sollte die letzte Art und Weise sein, wie D3D12 ihn verwendet hat (z. B. RENDER \_ TARGET), und der Ausgabezustand sollte die Art und Weise sein, wie D3D12 ihn verwendet, nachdem D3D11 abgeschlossen wurde (z. B. PRESENT).
-   Initialisieren Sie D2D, und stellen Sie die umschlossenen D3D11-Ressourcen für D2D bereit, um das Rendering vorzubereiten.

Gehen Sie dann auf jedem Frame wie folgt vor:

-   Rendern Sie mithilfe einer D3D12-Befehlsliste in den aktuellen Swap Chain Back-Puffer, und führen Sie ihn aus.
-   Abrufen der umschlossenen Ressource des aktuellen Backpuffers ([**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)).
-   Problem mit D2D-Renderingbefehlen.
-   Geben Sie die umschlossene Ressource frei ([**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)).
-   Leeren Sie den unmittelbaren D3D11-Kontext.
-   Vorhanden ([**IDXGISwapChain1::P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)).

## <a name="background"></a>Hintergrund

D3D11On12 funktioniert systematisch. Jeder D3D11-API-Aufruf durchläuft die typische Laufzeitvalidierung und wechselt zum Treiber. Auf Treiberebene zeichnet der spezielle 11on12-Treiber den Zustand auf und gibt Rendervorgänge an D3D12-Befehlslisten aus. Diese Befehlslisten werden nach Bedarf übermittelt (z. B. kann es sein, dass für eine Abfrage `GetData` oder Ressource `Map` Befehle geleert werden müssen) oder wie von Flush angefordert. Das Erstellen eines D3D11-Objekts führt in der Regel dazu, dass das entsprechende D3D12-Objekt erstellt wird. Einige Rendervorgänge fester Funktionen in D3D11 wie `GenerateMips` oder `DrawAuto` werden in D3D12 nicht unterstützt. D3D11On12 emuliert sie daher mit Shadern und zusätzlichen Ressourcen.

Für Interop ist es wichtig zu verstehen, wie D3D11On12 mit den D3D12-Objekten interagiert, die die App erstellt und bereitgestellt hat. Um sicherzustellen, dass die Arbeit in der richtigen Reihenfolge erfolgt, muss der direkte D3D11-Kontext geleert werden, bevor zusätzliche D3D12-Arbeiten an diese Warteschlange übermittelt werden können. Es ist auch wichtig sicherzustellen, dass die an D3D11On12 übergebene Warteschlange jederzeit entleerbar sein muss. Das bedeutet, dass alle Wartezeiten in der Warteschlange letztendlich erfüllt werden müssen, auch wenn der D3D11-Renderthread unbegrenzt blockiert wird. Achten Sie darauf, keine Abhängigkeit von zu übernehmen, wenn D3D11On12 Leerungen oder Wartezeichen einfügt, da sich dies mit zukünftigen Releases ändern kann. Darüber hinaus verfolgt und bearbeitet D3D11On12 eigenständig Ressourcenzustände. Die einzige Möglichkeit, die Koherität von Zustandsübergängen sicherzustellen, besteht darin, die Acquire/Release-APIs zu verwenden, um die Zustandsnachverfolgung an die Anforderungen der App anzupassen.

## <a name="cleaning-up"></a>Bereinigen

Um eine umschlossene D3D11On12-Ressource freizugeben, müssen zwei Dinge in dieser Reihenfolge geschehen:

-   Alle Verweise auf die Ressource, einschließlich aller Ansichten der Ressource, müssen freigegeben werden.
-   Die verzögerte Zerstörungsverarbeitung muss erfolgen. Die einfachste Möglichkeit, dies sicherzustellen, besteht darin, die API für den unmittelbaren Kontext `Flush` aufzurufen.

Nachdem beide Schritte abgeschlossen sind, sollten alle Verweise der umschlossenen Ressource freigegeben werden, und die D3D12-Ressource befindet sich ausschließlich im Besitz der D3D12-Komponente. Beachten Sie, dass D3D12 immer noch warten muss, bis die GPU abgeschlossen ist, bevor Sie eine Ressource vollständig freigeben. Stellen Sie daher sicher, dass Sie einen Verweis auf die Ressource speichern, bevor Sie die beiden obigen Schritte ausführen, es sei denn, Sie haben bereits bestätigt, dass die GPU die Ressource nicht mehr verwendet.

Alle anderen Ressourcen oder Objekte, die von D3D11On12 erstellt wurden, werden zum richtigen Zeitpunkt bereinigt, wenn die GPU sie nicht mehr verwendet hat, indem der D3D11-Mechanismus für die verzögerte Zerstörung verwendet wird. Wenn Sie jedoch versuchen, das D3D11On12-Gerät selbst freizugeben, während die GPU noch ausgeführt wird, kann die Zerstörung blockiert werden, bis die GPU abgeschlossen ist.

## <a name="limitations"></a>Einschränkungen

Die D3D11On12-Schicht implementiert eine sehr große Teilmenge der D3D11-API, aber es gibt einige bekannte Lücken (zusätzlich zu Fehlern in der Implementierung, die zu falschem Rendering führen können).

Ab Windows 10, Version 1809 (10.0; Build 17763), solange D3D11On12 auf einem Treiber ausgeführt wird, der Shader Model 6.0 oder höher unterstützt, kann er Shader ausführen, die Schnittstellen verwenden. In früheren Versionen von Windows ist das Shaderschnittstellenfeature in D3D11On12 nicht implementiert, und der Versuch, das Feature zu verwenden, verursacht Fehler und Debugmeldungen.

Ab Windows 10 Version 1803 (10.0; Build 17134), Swapketten werden auf D3D11On12-Geräten unterstützt. In früheren Versionen von Windows nicht.

D3D11On12 wurde nicht für die Leistung optimiert. Im Vergleich zu einem D3D11-Standardtreiber wird wahrscheinlich ein moderater CPU-Mehraufwand, minimaler GPU-Mehraufwand und bekanntlich ein erheblicher Arbeitsspeicheraufwand entstehen. Daher wird nicht empfohlen, D3D11On12 für komplizierte 3D-Szenen zu verwenden, und es wird stattdessen für einfache Szenen oder 2D-Rendering empfohlen.

## <a name="apis"></a>APIs

APIs, die die Ebene 11on12 bilden, werden in [11on12 Reference (Referenz zu 11on12)](direct3d-11on12-reference.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Exemplarische D2D-Verwendung von D3D11on12](d2d-using-d3d11on12.md)
</dt> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D](direct3d-12-interop.md)
</dt> </dl>

 

 