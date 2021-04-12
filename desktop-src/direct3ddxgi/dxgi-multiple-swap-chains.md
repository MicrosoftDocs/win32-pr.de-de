---
description: Um die Leistung zu verbessern, können Sie mehrere SwapChain pro Direct3D-renderinggerät erstellen.
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: Verbessern der Leistung mit mehreren Austausch Ketten pro renderinggerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e356434521054bc13b553c8ae3d6e43d8d98ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481958"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>Verbessern der Leistung mit mehreren Austausch Ketten pro renderinggerät

Um die Leistung zu verbessern, können Sie mehrere SwapChain pro Direct3D-renderinggerät erstellen. Verwenden Sie diesen Ansatz, um Speicherplatz zu sparen, der erforderlich ist, indem zusätzliche Geräte erstellt werden, oder um die Renderingzeit für einzelne Austausch Vorgänge pro Gerät separat zu reduzieren oder um Speicherplatz zu sparen und die Renderingzeit zu verkürzen.

-   [App-Szenarien mit mehreren Austausch Ketten pro Gerät](#app-scenarios-with-multiple-swap-chains-per-device)
-   [Verwalten mehrerer Swapketten pro Gerät](#managing-multiple-swap-chains-per-device)
    -   [Festlegen der maximalen Frame Latenz](#setting-maximum-frame-latency)
    -   [Verwenden eines Flip-Modells mit mehreren Austausch Ketten pro Gerät](#using-flip-model-with-multiple-swap-chains-per-device)
-   [Zugehörige Themen](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>App-Szenarien mit mehreren Austausch Ketten pro Gerät

Verwenden Sie mehrere Ketten, wenn die APP-Szene aus separaten Anzeige Objekten besteht, die unabhängig gerendert und aktualisiert werden. Beispielsweise wird die Animation von der APP ständig geändert, z. b. Video auf einer Seite und Bild lauffähigen Text auf einer anderen Seite. Um Speicherplatz zu sparen, den Sie normalerweise benötigen, um ein zusätzliches Gerät zu erstellen und die Freigabe von Inhalten zwischen den beiden Austausch Ketten zu vereinfachen, können Sie beide Swapketten erstellen, die mit demselben Direct3D-renderinggerät verknüpft sind. Verwenden Sie eine Austausch Kette für Animationen und eine SwapChain für Text. Ein gängiges Beispiel für dieses Szenario ist eine Direct3D-APP, die auch die [directcomposition](../directcomp/directcomposition-portal.md) -API verwendet.

Ein anderes Szenario ist, wenn Sie die Renderingzeit speichern möchten, indem Sie mehrere Renderziele gleichzeitig auf mehreren Austausch Ketten festlegen. Nehmen Sie beispielsweise an, Sie möchten eine komplexe Szene mit vielen Texturen und Geometrie rendern, wie z. b. Rennwagen auf einer Spur, und Sie möchten, dass das App-Fensteransichten sowohl aus dem hinteren als auch dem Seitenspiegel in zwei Anzeige Fenstern anzeigt, die von zwei Austausch Ketten gerendert werden. Wenn Sie die mehrere Swapketten als Renderziele festlegen, muss Ihre APP die Renderingzeiten für jede SwapChain nicht separat wiederholen.

## <a name="managing-multiple-swap-chains-per-device"></a>Verwalten mehrerer Swapketten pro Gerät

Verwenden Sie die Richtlinien in diesem Abschnitt, um mehrere Austausch Ketten zu verwalten, die Sie für ein einzelnes Direct3D Rendering-Gerät erstellen.

### <a name="setting-maximum-frame-latency"></a>Festlegen der maximalen Frame Latenz

Verwenden Sie die [**IDXGIDevice1:: setmaximumframelatency**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) -Methode, um die maximale Anzahl von Vorgängen festzulegen, die das Betriebssystem zum Rendern der Anzeige in die Warteschlange stellen kann. Diese maximale Anzahl liegt bei Direct3D renderinggerät statt pro Swapkette. Um sicherzustellen, dass das Betriebssystem die aktuellen Vorgänge im vorgesehenen VSYNC-Intervall anzeigt, empfiehlt es sich daher, die maximale Frame Latenz nicht auf 1 festzulegen, wenn Sie mehrere Flip-oder BitBLT-Modell Austausch Ketten pro Gerät erstellen und wenn mehr als eine dieser Austausch Ketten für jeden Frame gerencht wird. Als allgemeine Regel gilt: Wenn Sie zuverlässig nur 2 Vorgänge pro Frame zwischen allen Austausch Ketten desselben Geräts übermitteln, können Sie die maximale Frame Latenz auf 2 festlegen. Wenn Sie die aktuellen Vorgänge pro Frame nicht zuverlässig übermitteln und zählen können, können Sie [aktuelle Statistiken](dxgi-flip-model.md) verwenden, um zu verfolgen, wann das Betriebssystem vorhandene Vorgänge anzeigt.

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>Verwenden eines Flip-Modells mit mehreren Austausch Ketten pro Gerät

Verwenden Sie diese Richtlinien, wenn Sie das [DXGI-Flip-Modell](dxgi-flip-model.md) mit mehreren Austausch Ketten verwenden, die Sie für ein einzelnes Direct3D Rendering-Gerät erstellen.

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>Bestimmte VSYNC-Intervalle mit den aktuellen Vorgängen der SwapChain als Ziel

Wenn Sie zwei oder mehr Modell Austausch Ketten pro Gerät erstellen, achten Sie auf die Anzeige Unterschiede, wenn Sie die Sequenz des Geräte Zustands und die Abfolge der Aufrufe der [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) -Methode aller Austausch Ketten verwalten. Um sicherzustellen, dass das Betriebssystem den aktuellen Vorgang jeder SwapChain im vorgesehenen VSYNC-Intervall anzeigt, empfiehlt es sich, sicherzustellen, dass die Anzahl der in der Warteschlange befindlichen Vorgänge immer mindestens eine geringere Anzahl von backpuffern für die Swapkette mit der geringsten Anzahl von backpuffern ist.

### <a name="flip-model-swap-chains-with-two-buffers"></a>Modell Austausch Ketten mit zwei Puffern kippen

Ihre APP kann bestimmte VSYNC-Intervalle als Ziel haben, wenn die Anzahl der in der Warteschlange befindlichen Vorgänge kleiner oder gleich der Anzahl von backpuffern ist – 1. Außerdem müssen Sie für jede SwapChain separat verwenden oder Rendering und dann die Verwendung der einzelnen SwapChain mit einem aktuellen Vorgang beenden. Wenn Sie also jeden aktuellen Vorgang für eine zwei-Puffer-Swapkette mit einem Flip-Modell einreichen, erreichen Sie den Schwellenwert für die Anzahl der Back Puffer, bei denen Sie besondere Aufmerksamkeit benötigen, wenn Sie möchten, dass Ihre APP bestimmte VSYNC-Intervalle als Ziel hat.

Im Fall von 2-Puffer Austausch Ketten müssen Sie vor dem Renderingvorgang zum nächsten Puffer sicherstellen, dass das Betriebssystem die Anzeige aller vorhandenen SwapChain-Vorgänge beendet. Es wird empfohlen, dass Sie das Festlegen der renderzielansicht und des anderen Renderingzustands, das nächste rendern, abschließen und dann [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) für jeden der beiden Puffer einer Swapkette aufzurufen, bevor Sie für eine andere austauschkette dasselbe tun. Wenn Sie mit zwei oder mehr Austausch Ketten arbeiten, müssen Sie für jede Swapkette das Renderziel und den Renderingzustand auf dem Gerät zurücksetzen. Der Vorteil dieses Ansatzes besteht darin, den Fall zu vermeiden, in dem eine oder mehrere der aktuellen Vorgänge der SwapChain das gewünschte VSYNC-Intervall übersehen. Im ersten Beispiel wird für die APP mit veränderlichen Animationen und Text, wie in [App-Szenarien mit mehreren Austausch Ketten pro Gerät](#app-scenarios-with-multiple-swap-chains-per-device)beschrieben, durch die Ausrichtung auf bestimmte aktuelle Intervalle sichergestellt, dass beim Aktualisieren der Animation in einem Anzeige Fenster der entsprechende Text, der von einer separaten Swapkette gerendert wird, auch in einem anderen Anzeige Fenster gleichzeitig angezeigt wird. Wenn Ihre APP bestimmte VSYNC-Intervalle als Ziel verwenden muss, müssen Sie diese Anleitung befolgen.

Dieses Diagramm zeigt ein Beispiel für den Codefluss des Auslagerungs Ketten Rendering und der Darstellung in einer APP, die zwei Flip-Model-Austausch Ketten mit jeweils zwei Puffern enthält. In diesem Fall müssen Sie für jeden aktuellen Vorgang ein bestimmtes vorhandenes Intervall als Ziel haben.

![Abbildung des Kippen von Modellen mit zwei Puffern](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>Reduzieren der Renderingzeit durch gleichzeitiges Festlegen mehrerer Austausch Ketten als Renderziele

Im zweiten Beispiel, wie in [App-Szenarios mit mehreren Austausch Ketten pro Gerät](#app-scenarios-with-multiple-swap-chains-per-device)beschrieben, empfiehlt es sich, die Zielvorgabe für bestimmte aktuelle VSYNC-Intervalle mit der gleichzeitigen Durchführung mehrerer Renderingziele für alle Austausch Ketten abzugleichen. Legen Sie in diesem Fall mehrere Renderziele gleichzeitig fest, rendersie die Szene auf jeder Swapkette, und nennen Sie dann [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) für jede Swapkette, die in der Szene verwendet wird. Der Vorteil dieses Ansatzes ist, dass Sie die Renderingzeit verringern. Die Beschränkung dieses Ansatzes besteht darin, dass bei der gleichzeitigen Austausch Kette vorhandene Vorgänge nicht auf dieselbe VSYNC abzielen können, wenn Sie 2-Puffer-Austausch Ketten verwenden. Das Betriebssystem zeigt z. b. den Inhalt der racewagen-Ansichts Spiegelung bis zu 1 VSYNC an, nachdem derselbe Inhalt aus dem racewagen-Spiegel Spiegel angezeigt wird.

Dieses Diagramm zeigt ein Beispiel für den Codefluss des Verlaufs der Austausch Kette und die Darstellung in einer APP mit zwei Swapketten, die jeweils zwei Puffer lang sind. In diesem Beispiel speichern Sie Renderingzeiten, um die Ketten 1 und 2 für die Puffer A und C auszutauschen. Sie können jedoch nicht die VSYNC-Intervalle synchronisieren, bei denen die aktuellen Vorgänge für die Puffer A und C angezeigt werden. Diese Muster werden für Frame 2 wiederholt.

![Darstellung der gleichzeitigen Festlegung mehrerer Austausch Ketten als Renderziele](images/multi-swap-chains-as-render-targets.png)

Um zu vermeiden, dass das gewünschte VSYNC-Intervall aufgrund von vielen in der Warteschlange befindlichen Vorgängen vorhanden ist, können Sie die Anzahl der Back Puffer in jeder Swapkette erhöhen. Diese Technik verwendet jedoch mehr Video Arbeitsspeicher. Um fehlende Ziel-VSYNC-Intervalle zu vermeiden, wird empfohlen, die Anzahl der in der Warteschlange befindlichen Vorgänge immer kleiner als die Anzahl der Back Puffer in der SwapChain mit der geringsten Anzahl von backpuffern beizubehalten. Wenn Sie zwei Swapketten als mehrere Renderziele festlegen, wird empfohlen, dass Sie Swapketten mit mindestens drei Puffern erstellen, da Sie zwei vorhandene Vorgänge gleichzeitig in beiden Austausch Ketten in die Warteschlange stellen.

Das nächste Diagramm zeigt ein Beispiel für den Codefluss des Verlaufs von Swap-Chain-Rendering und-Darstellung in einer APP mit zwei Flip-Model-Austausch Ketten, die jeweils drei Puffer lang sind. Da die Anzahl der in der Warteschlange befindlichen Darstellung für einen bestimmten Frame 2 beträgt, was kleiner ist als die Anzahl von backpuffern pro Swapkette, kann Ihre APP mehrere Renderziele festlegen und die gleichen VSYNC-Intervalle für die Puffer A und D in Frame 2 sowie für die Puffer in nachfolgenden Frames als Ziel festlegen.

![Darstellung der gleichzeitigen Festlegung mehrerer Austausch Ketten als Renderziele für die gleiche VSYNC](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern der Präsentation mit dem Flip-Modell, den geänderten Rechtecke und den Bereichen](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
