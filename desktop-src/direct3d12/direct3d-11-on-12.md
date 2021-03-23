---
title: Direct3D 11 on 12
description: D3D11On12 ist ein Mechanismus, mit dem Entwickler D3D11-Schnittstellen und-Objekte verwenden können, um die D3D12-API zu steuern.
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62816ea0d7d7969cd56e0a9f525b2c412c8da182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548643"
---
# <a name="direct3d-11-on-12"></a>Direct3D 11 on 12

D3D11On12 ist ein Mechanismus, mit dem Entwickler D3D11-Schnittstellen und-Objekte verwenden können, um die D3D12-API zu steuern. D3D11on12 ermöglicht die Verwendung von Komponenten, die mit D3D11 (z. b. D2D Text und UI) geschrieben wurden, mit Komponenten, die für die D3D12-API geschrieben wurden. D3D11on12 ermöglicht außerdem die inkrementelle Portierung einer Anwendung von D3D11 auf D3D12, indem Teile der App zur Vereinfachung der Ausrichtung auf D3D11 verwendet werden, während andere für die Leistung vorgesehen sind, während andere für die Leistung vorgesehen sind D3D11On12 vereinfacht die Verwendung von Interop-Techniken zum Freigeben von Ressourcen und Synchronisieren von Arbeit zwischen den beiden APIs.

-   [Initialisieren von D3D11On12](#initializing-d3d11on12)
-   [Beispiel Verwendung](#example-usage)
-   [Hintergrund](#background)
-   [Bereinigen](#cleaning-up)
-   [Einschränkungen](#limitations)
-   [APIs](#apis)
-   [Verwandte Themen](#related-topics)

## <a name="initializing-d3d11on12"></a>Initialisieren von D3D11On12

Der erste Schritt besteht darin, ein D3D12-Gerät und eine Befehls Warteschlange zu erstellen, um D3D11On12 zu verwenden. Diese Objekte werden als Eingabe für die Initialisierungs Methode [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice)bereitgestellt. Sie können sich diese Methode als Erstellen eines D3D11-Geräts mit dem imaginären Treibertyp D3D \_ Driver \_ Type \_ 11on12 vorstellen, wobei der D3D11-Treiber für das Erstellen von Objekten und das Übermitteln von Befehlslisten an die D3D12-API zuständig ist.

Nachdem Sie ein D3D11-Gerät und den unmittelbaren Kontext haben, können Sie das `QueryInterface` Gerät für die [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) -Schnittstelle ausschalten. Dies ist die primäre Schnittstelle, die für Interop zwischen D3D11 und D3D12 verwendet wird. Damit sowohl der D3D11-Gerätekontext als auch die D3D12-Befehlslisten auf denselben Ressourcen angewendet werden können, ist es erforderlich, mithilfe der [**createwrappdresource**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) -API "umschließende Ressourcen" zu erstellen. Diese Methode stuft eine D3D12-Ressource herauf, damit Sie in D3D11 verständlich ist. Eine umschließende Ressource beginnt im Zustand "abgerufen", einer Eigenschaft, die von den Methoden [**acquirewrappeer dresources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) und [**releasewrappdresources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) bearbeitet wird.

## <a name="example-usage"></a>Beispielverwendung

Die typische Verwendung von D3D11On12 wäre die Verwendung von D2D zum Rendering von Text oder Bildern oberhalb eines D3D12 backpuffers. Beispielcode finden Sie im D3D11On12-Beispiel. Im folgenden finden Sie einen groben Überblick über die Schritte, die Sie ausführen müssen:

-   Erstellen Sie ein D3D12-Gerät ([**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)) und eine D3D12 Swap-Kette ("[**kreateswapchain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) " mit einem [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) als Eingabe).
-   Erstellen Sie ein D3D11On12-Gerät mit dem D3D12-Gerät und derselben Befehls Warteschlange als Eingabe.
-   Rufen Sie die zurück Puffer der Austausch Kette ab, und erstellen Sie für jede einzelne D3D11-umschließende Ressourcen. Der verwendete Eingabe Zustand sollte die letzte Methode sein, die von D3D12 verwendet wurde (z. b. \_ Renderziel), und der Ausgabe Zustand sollte so lauten, wie D3D12 ihn nach Beendigung von D3D11 verwendet (z. b. vorhanden).
-   Initialisieren Sie D2D, und stellen Sie die D3D11-umschließenen Ressourcen für D2D bereit, um das Rendering vorzubereiten.

Führen Sie dann in jedem Frame die folgenden Schritte aus:

-   Rendering in den aktuellen SwapChain-Hintergrund Puffer mithilfe einer D3D12-Befehlsliste, und führen Sie Sie aus.
-   Rufen Sie die umschließende Ressource des aktuellen Hintergrund Puffers ([**acquirewrappdresources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)) ab.
-   Issue D2D renderingbefehle.
-   Geben Sie die umschließende Ressource ([**releasewrapetdresources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)) frei.
-   Leeren Sie den D3D11 unmittelbaren Kontext.
-   Vorhanden ([**IDXGISwapChain1::P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)).

## <a name="background"></a>Hintergrund

D3D11On12 arbeitet systematisch. Jeder D3D11-API-Befehl durchläuft die typische Lauf Zeit Validierung und führt den Treiber aus. Auf der Treiber Ebene zeichnet der besondere 11on12-Treiber den Status auf und gibt Rendering-Vorgänge in D3D12-Befehlslisten aus. Diese Befehlslisten werden bei Bedarf übermittelt (z. b. eine Abfrage `GetData` oder Ressource `Map` erfordert möglicherweise, dass Befehle geleert werden) oder wie von Flush angefordert. Das Erstellen eines D3D11-Objekts führt normalerweise dazu, dass das entsprechende D3D12-Objekt erstellt wird. Einige funktionsfunktionsrendering-Vorgänge in D3D11, z. b. `GenerateMips` oder `DrawAuto` , werden in D3D12 nicht unterstützt. daher emuliert D3D11On12 diese mithilfe von Shader und zusätzlichen Ressourcen.

Bei Interop ist es wichtig zu verstehen, wie D3D11On12 mit den D3D12-Objekten interagiert, die von der App erstellt und bereitgestellt wurden. Um sicherzustellen, dass die Arbeit in der richtigen Reihenfolge erfolgt, muss der D3D11 immediate-Kontext geleert werden, bevor zusätzliche D3D12-Arbeit an diese Warteschlange gesendet werden kann. Außerdem ist es wichtig sicherzustellen, dass die Warteschlange, die an D3D11On12 übergeben wird, jederzeit drazierbar sein muss. Dies bedeutet, dass warte Vorgänge in der Warteschlange letztendlich erfüllt werden müssen, auch wenn der D3D11-Renderthread unbegrenzt blockiert wird. Seien Sie vorsichtig, wenn Sie keine Abhängigkeit davon treffen möchten, wann D3D11On12 Leerungen oder warte Vorgänge einfügt, da dies bei zukünftigen Releases möglicherweise geändert wird. Zusätzlich werden Ressourcen Zustände von D3D11On12 nachverfolgt und manipuliert. Die einzige Möglichkeit, die Konsistenz der Zustandsübergänge sicherzustellen, besteht darin, die Abruf-/Release-APIs zu verwenden, um die Zustandsüberwachung so zu ändern, dass Sie den Anforderungen der APP entspricht.

## <a name="cleaning-up"></a>Bereinigen

Um eine D3D11On12-umschließende Ressource freizugeben, müssen in dieser Reihenfolge zwei Dinge vorkommen:

-   Alle Verweise auf die Ressource, einschließlich aller Ansichten der Ressource, müssen freigegeben werden.
-   Die verzögerte Zerstörungs Verarbeitung muss stattfinden. Die einfachste Möglichkeit, dies zu gewährleisten, besteht darin, die unmittelbare Kontext-API aufzurufen `Flush` .

Nachdem beide Schritte ausgeführt wurden, sollten alle von der umschließenden Ressource aufgenommenen Verweise freigegeben werden, und die D3D12-Ressource wird ausschließlich im Besitz der D3D12-Komponente. Beachten Sie, dass D3D12 noch vor dem vollständigen Freigeben einer Ressource auf den GPU-Abschluss warten muss. Achten Sie daher darauf, einen Verweis auf die Ressource zu speichern, bevor Sie die beiden obigen Schritte ausführen, es sei denn, Sie haben bereits bestätigt, dass die GPU nicht mehr die Ressource verwendet.

Alle anderen Ressourcen oder Objekte, die von D3D11On12 erstellt wurden, werden zu dem richtigen Zeitpunkt bereinigt, wenn die GPU die Verwendung mithilfe des verzögerten Zerstörungs Mechanismus D3D11's abgeschlossen hat. Wenn Sie jedoch versuchen, das D3D11On12-Gerät selbst freizugeben, während die GPU noch ausgeführt wird, kann die Zerstörung blockiert werden, bis die GPU abgeschlossen ist.

## <a name="limitations"></a>Einschränkungen

Die D3D11On12-Ebene implementiert eine sehr große Teilmenge der D3D11-API. es gibt jedoch einige bekannte Lücken (zusätzlich zu Fehlern in der Implementierung, die ein falsches Rendering verursachen können).

Ab Windows 10, Version 1809 (10,0; Build 17763), solange D3D11On12 auf einem Treiber ausgeführt wird, der das Shadermodell 6,0 oder höher unterstützt, kann er Shader ausführen, die Schnittstellen verwenden. In früheren Versionen von Windows ist das Shader-Schnittstellen Feature in D3D11On12 nicht implementiert, und der Versuch, das Feature zu verwenden, führt zu Fehlern und Debugmeldungen.

Ab Windows 10, Version 1803 (10,0; Build 17134), Austausch Ketten werden auf D3D11On12-Geräten unterstützt. In früheren Versionen von Windows ist dies nicht der Fall.

D3D11On12 wurde nicht für die Leistung optimiert. Im Vergleich zu einem standardmäßigen D3D11-Treiber, minimaler GPU-Aufwand, wird der CPU-Aufwand wahrscheinlich erheblich reduziert, und es ist ein erheblicher Speicher Aufwand zu erwarten. Daher empfiehlt es sich nicht, D3D11On12 für komplizierte 3D-Szenen zu verwenden, und es wird stattdessen für einfache Szenen oder das 2D-Rendering empfohlen.

## <a name="apis"></a>APIs

APIs, die die 11on12-Ebene ausmachen, werden in [11on12-Referenz](direct3d-11on12-reference.md)beschrieben.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[D2D using D3D11on12-Exemplarische Vorgehensweise](d2d-using-d3d11on12.md)
</dt> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D](direct3d-12-interop.md)
</dt> </dl>

 

 