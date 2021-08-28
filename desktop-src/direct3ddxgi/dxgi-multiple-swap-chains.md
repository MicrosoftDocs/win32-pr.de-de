---
description: Um die Leistung zu verbessern, sollten Sie mehr als eine Swapkette pro Direct3D-Renderinggerät erstellen.
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: Verbessern der Leistung mit mehreren Austauschketten pro Renderinggerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91445660bf9efc59e9e39c88819587dce3960325df0659487eaae67a845a7329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627493"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>Verbessern der Leistung mit mehreren Austauschketten pro Renderinggerät

Um die Leistung zu verbessern, sollten Sie mehr als eine Swapkette pro Direct3D-Renderinggerät erstellen. Verwenden Sie diesen Ansatz, um Arbeitsspeicher zu sparen, der durch das Erstellen zusätzlicher Geräte erforderlich ist, oder um die Renderingzeit zu reduzieren, die separat in einzelnen Austauschketten pro Gerät gerendert werden soll, oder um Arbeitsspeicher zu sparen und die Renderingzeit zu reduzieren.

-   [App-Szenarien mit mehreren Austauschketten pro Gerät](#app-scenarios-with-multiple-swap-chains-per-device)
-   [Verwalten mehrerer Austauschketten pro Gerät](#managing-multiple-swap-chains-per-device)
    -   [Festlegen der maximalen Framelatenz](#setting-maximum-frame-latency)
    -   [Verwenden eines Flip-Modells mit mehreren Austauschketten pro Gerät](#using-flip-model-with-multiple-swap-chains-per-device)
-   [Zugehörige Themen](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>App-Szenarien mit mehreren Austauschketten pro Gerät

Erwägen Sie die Verwendung mehrerer Ketten, wenn die App-Szene aus separaten Anzeigeobjekten besteht, die unabhängig gerendert und aktualisiert werden. Beispielsweise verfügt die App über ständig geänderte Animationen, z. B. Video auf einer Seite und scrollbaren Text auf einer anderen Seite. Um Arbeitsspeicher zu sparen, den Sie normalerweise benötigen, um ein zusätzliches Gerät zu erstellen, und um die Freigabe von Inhalten zwischen den beiden Austauschketten zu erleichtern, können Sie beide Austauschketten erstellen, die an dasselbe Direct3D-Renderinggerät gebunden sind. Verwenden Sie eine Auslagerungskette für Animationen und eine Austauschkette für Text. Ein gängiges Beispiel für dieses Szenario ist eine Direct3D-App, die auch die [DirectComposition-API](../directcomp/directcomposition-portal.md) verwendet.

Ein weiteres Szenario ist, wenn Sie Renderingzeit sparen möchten, indem Sie mehrere Renderziele auf mehreren Austauschketten gleichzeitig festlegen. Angenommen, Sie möchten eine komplexe Szene mit vielen Texturen und Geometrien rendern, z. B. Autorennwagen auf einer Spur, und sie möchten, dass das App-Fenster Ansichten von der Rückseite und den Seitenspiegeln in zwei Anzeigefenstern zeigt, die von zwei Austauschketten gerendert werden. Wenn Sie die mehrfachen Auslagerungsketten als Renderziele festlegen, muss Ihre App die Renderingzeiten für jede Austauschkette nicht separat wiederholen.

## <a name="managing-multiple-swap-chains-per-device"></a>Verwalten mehrerer Austauschketten pro Gerät

Verwenden Sie die Richtlinien in diesem Abschnitt, um mehrere Austauschketten zu verwalten, die Sie für ein einzelnes Direct3D-Renderinggerät erstellen.

### <a name="setting-maximum-frame-latency"></a>Festlegen der maximalen Framelatenz

Verwenden Sie [**die IDXGIDevice1::SetMaximumFrameLatency-Methode,**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) um die maximale Anzahl vorhandener Vorgänge, die das Betriebssystem für das Rendern in der Anzeige in die Warteschlange stellen kann, festlegen. Diese maximale Anzahl gilt pro Direct3D-Renderinggerät und nicht pro Austauschkette. Um sicherzustellen, dass das Betriebssystem die aktuellen Vorgänge im vorgesehenen vsync-Intervall anzeigt, empfiehlt es sich daher, die maximale Framelatenz nicht auf 1 zu setzen, wenn Sie mehrere Austauschketten für Flip- oder Bitblt-Modelle pro Gerät erstellen und wenn mehr als eine dieser Austauschketten für jeden Frame gerendert wird. Wenn Sie zuverlässig nur zwei aktuelle Vorgänge pro Frame zwischen allen Austauschketten desselben Geräts übermitteln, können Sie die maximale Framelatenz auf 2 festlegen. Wenn Sie die aktuellen Vorgänge nicht zuverlässig pro Frame übermitteln [](dxgi-flip-model.md) und zählen können, können Sie aktuelle Statistiken verwenden, um zu verfolgen, wann das Betriebssystem aktuelle Vorgänge anzeigt.

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>Verwenden eines Flip-Modells mit mehreren Austauschketten pro Gerät

Verwenden Sie diese Richtlinien, wenn Sie das [DXGI-Flip-Modell](dxgi-flip-model.md) mit mehreren Austauschketten verwenden, die Sie für ein einzelnes Direct3D-Renderinggerät erstellen.

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>Ausrichtung auf bestimmte vsync-Intervalle mit den aktuellen Vorgängen der einzelnen Swapketten

Wenn Sie zwei oder mehr Flipmodell-Austauschketten pro Gerät erstellen, achten Sie auf die Anzeigeunterschiede, wenn Sie die Sequenz des Gerätestatus und die Sequenz von Aufrufen der [**IDXGISwapChain1::P resent1-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) aller Austauschketten verwalten. Um sicherzustellen, dass das Betriebssystem den aktuellen Vorgang jeder Auslagerungskette im vorgesehenen vsync-Intervall anzeigt, sollten Sie sicherstellen, dass die Anzahl der in der Warteschlange gespeicherten aktuellen Vorgänge immer mindestens eins kleiner als die Anzahl der Backpuffer für die Swapkette mit der geringsten Anzahl von Backpuffern ist.

### <a name="flip-model-swap-chains-with-two-buffers"></a>Tauschketten für Flip-Modelle mit zwei Puffern

Ihre App kann bestimmte vsync-Intervalle als Ziel verwenden, wenn die Anzahl der in die Warteschlange gestellten aktuellen Vorgänge kleiner oder gleich der Anzahl der Zurückpuffer ist – 1. Außerdem müssen Sie jede Auslagerungskette separat verwenden oder rendern und dann die Verwendung jeder Austauschkette mit einem aktuellen Vorgang beenden. Wenn Sie also jeden aktuellen Vorgang für eine 2-Puffer-Swapkette des Flip-Modells übermitteln, erreichen Sie den Schwellenwert für die Anzahl der Hintergrundpuffer, bei denen Sie besondere Aufmerksamkeit darauf achten müssen, wenn Ihre App bestimmte vsync-Intervalle als Ziel verwenden soll.

Im Fall von 2-Puffer-Swapketten müssen Sie sicherstellen, dass das Betriebssystem die Anzeige des aktuellen Vorgangs jeder Austauschkette beendet, um bestimmte vsync-Intervalle als Ziel zu verwenden, bevor Sie zum nächsten Puffer rendern. Es wird empfohlen, dass Sie das Festlegen der Renderzielansicht und anderer Renderingstatus beenden, das nächste Rendern und dann [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) für jeden der beiden Puffer einer Auslagerungskette aufrufen, bevor Sie dies für eine andere Austauschkette tun. Wenn Sie mit zwei oder mehr Austauschketten arbeiten, müssen Sie das Renderziel und den Renderingzustand auf dem Gerät für jede Austauschkette zurücksetzen. Der Vorteil dieses Ansatzes besteht in der Vermeidung von Fällen, in denen ein oder mehrere der aktuellen Vorgänge der Austauschkette das beabsichtigte vsync-Intervall nicht erhalten. Für das erste Beispiel, eine App mit sich ändernden Animationen und Text, wie unter [App-Szenarien](#app-scenarios-with-multiple-swap-chains-per-device)mit mehreren Austauschketten pro Gerät beschrieben, durch Die Ausrichtung auf bestimmte aktuelle Intervalle wird sichergestellt, dass beim Aktualisieren der Animation in einem Anzeigefenster der entsprechende Text, der von einer separaten Austauschkette gerendert wird, ebenfalls gleichzeitig in einem anderen Anzeigefenster angezeigt wird. Wenn Ihre App bestimmte vsync-Intervalle als Ziel verwenden muss, müssen Sie diese Anleitung befolgen.

Dieses Diagramm zeigt ein Beispiel für den Codefluss des Austauschkettenrenderings und der Darstellung in einer App mit zwei Flip-Model-Austauschketten mit jeweils zwei Puffern. In diesem Fall müssen Sie für jeden aktuellen Vorgang ein bestimmtes aktuelles Intervall als Ziel haben.

![Abbildung eines Flip-Modells mit zwei Puffern](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>Reduzieren der Renderingzeit durch gleichzeitiges Festlegen mehrerer Swapketten als Renderziele

Im zweiten Beispiel, Den Autorennen auf einer Spur, wie in [App-Szenarien](#app-scenarios-with-multiple-swap-chains-per-device)mit mehreren Austauschketten pro Gerät beschrieben, sollten Sie gegen bestimmte aktuelle vsync-Intervalle mit den Renderingzeiteinsparungen abwechseln, die Sie erzielen, indem Sie mehrere Renderziele auf allen Austauschketten gleichzeitig festlegen. Legen Sie in diesem Fall mehrere Renderziele gleichzeitig fest, rendern Sie die Szene in jeder Swapkette, und rufen Sie dann [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) für jede Swapkette auf, die in der Szene verwendet wird. Der Vorteil dieses Ansatzes ist, dass Sie die Renderingzeit reduzieren. Die Einschränkung dieses Ansatzes besteht in ihren gleichzeitigen Swap chain present-Vorgängen, die nicht auf dieselbe vsync-Funktion zielen können, wenn Sie 2-Puffer-Swapketten verwenden. Beispielsweise zeigt das Betriebssystem den Inhalt der Seitenansichtsspiegel des Racewagens erst nach 1 vsync an, nachdem der gleiche Inhalt aus dem Rückspiegel des Racewagens angezeigt wurde.

Dieses Diagramm zeigt ein Beispiel für den Codefluss des Austauschkettenrenderings und der Darstellung in einer App mit zwei Flip-Model-Austauschketten mit jeweils zwei Puffern. In diesem Beispiel sparen Sie Renderingzeiten, um die Ketten 1 und 2 für die Puffer A und C zu tauschen. Sie können jedoch nicht die vsync-Intervalle synchronisieren, in denen aktuelle Vorgänge für die Puffer A und C angezeigt werden. Dieses Muster wird für Frame 2 wiederholt.

![Abbildung des gleichzeitigen Festlegens mehrerer Swapketten als Renderziele](images/multi-swap-chains-as-render-targets.png)

Um zu vermeiden, dass das vorgesehene vsync-Intervall aufgrund von zu vielen in der Warteschlange gespeicherten aktuellen Vorgängen fehlt, können Sie die Anzahl der Backpuffer in jeder Swapkette erhöhen. Bei diesem Verfahren wird jedoch mehr Videospeicher verwendet. Um zu vermeiden, dass vsync-Zielintervalle fehlen, empfiehlt es sich, die Anzahl der in der Warteschlange gespeicherten aktuellen Vorgänge immer kleiner als die Anzahl der Backpuffer in der Swapkette mit der geringsten Anzahl von Backpuffern zu halten. Wenn Sie zwei Swapketten als mehrere Renderziele festlegen, da Sie zwei aktuelle Vorgänge gleichzeitig auf beiden Swapketten in die Warteschlange stellen, wird empfohlen, Austauschketten mit mindestens drei Puffern zu erstellen.

Das nächste Diagramm zeigt ein Beispiel für den Codefluss des Austauschkettenrenderings und der Darstellung in einer App mit zwei Flip-Model-Austauschketten mit jeweils drei Puffern. Da hier die Anzahl der in der Warteschlange angezeigten Daten für einen bestimmten Frame 2 beträgt, was kleiner als die Anzahl der Backpuffer pro Swapkette ist, kann Ihre App mehrere Renderziele festlegen und weiterhin die gleichen vsync-Intervalle für die Puffer A und D in Frame 2 und für die Puffer in nachfolgenden Frames als Ziel verwenden.

![Abbildung des gleichzeitigen Festlegens mehrerer Swapketten als Renderziele für die gleiche vsync](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern der Präsentation mit dem Flip-Modell, dirty rectangles und scrolled areas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
