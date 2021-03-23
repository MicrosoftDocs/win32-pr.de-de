---
title: Verwenden einer Stamm Signatur
description: Bei der Stamm Signatur handelt es sich um die Definition einer beliebig angeordneten Auflistung von deskriptortabellen (einschließlich Layout), Stamm Konstanten und Stamm Deskriptoren.
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3babe26dc06d4f85ce3d6fb771e18c78b54a3701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104909"
---
# <a name="using-a-root-signature"></a>Verwenden einer Stamm Signatur

Bei der Stamm Signatur handelt es sich um die Definition einer beliebig angeordneten Auflistung von deskriptortabellen (einschließlich Layout), Stamm Konstanten und Stamm Deskriptoren. Jeder Eintrag hat einen Kosten Wert für eine Obergrenze, sodass die Anwendung das Gleichgewicht zwischen der Anzahl der einzelnen Eintrags Typen, die die Stamm Signatur enthalten wird, abwägen kann.

-   [Befehlslisten Semantik](#command-list-semantic)
-   [Bündel Semantik](#bundle-semantics)
-   [Verwandte Themen](#related-topics)

Die Stamm Signatur ist ein Objekt, das von der manuellen Spezifikation an der API erstellt werden kann. Alle Shader in einem PSO müssen mit dem mit dem PSO angegebenen Stamm Layout kompatibel sein. andernfalls müssen die einzelnen Shader eingebettete Stamm Layouts enthalten, die einander entsprechen. Andernfalls schlägt die PSO-Erstellung fehl. Eine Eigenschaft der Stamm Signatur ist, dass Shader beim Schreiben nicht wissen müssen, obwohl Stamm Signaturen bei Bedarf auch direkt in Shadern erstellt werden können. Für vorhandene Shader-Assets müssen keine Änderungen mit Stamm Signaturen kompatibel sein. Das Shader-Modell 5,1 wird eingeführt, um zusätzliche Flexibilität (dynamische Indizierung von Deskriptoren innerhalb von Shader) bereitzustellen, und kann nach Bedarf inkrementell aus vorhandenen Shader-Assets übernommen werden.

## <a name="command-list-semantic"></a>Befehlslisten Semantik

Am Anfang einer Befehlsliste ist die Stamm Signatur nicht definiert. Grafik-Shader haben eine separate Stamm Signatur vom Compute-Shader, die jeweils unabhängig von der Befehlsliste zugewiesen werden. Die Stamm Signatur, die in einer Befehlsliste oder einem Bundle festgelegt ist, muss auch mit dem aktuell festgelegten PSO bei Draw/Dispatch identisch sein. Andernfalls ist das Verhalten nicht definiert. Vorübergehende Stamm Signatur Konflikte vor dem Zeichnen/verteilen, wie z. b. das Festlegen eines inkompatiblen PSO-Fehlers vor dem Wechsel zu einer kompatiblen Stamm Signatur (sofern diese durch den Aufruf von Draw/Dispatch kompatibel sind). Wenn Sie ein PSO festlegen, wird die Stamm Signatur nicht geändert. Die Anwendung muss eine dedizierte API zum Festlegen der Stamm Signatur abrufen.

Nachdem eine Stamm Signatur in einer Befehlsliste festgelegt wurde, definiert das Layout den Satz von Bindungen, die von der Anwendung bereitgestellt werden sollen, und welche PSOs verwendet werden können (solche, die mit demselben Layout kompiliert werden) für die nächsten Draw-/dispatchaufrufe. Beispielsweise könnte eine Stamm Signatur von der Anwendung so definiert werden, dass Sie die folgenden Einträge hat. Jeder Eintrag wird als "Slot" bezeichnet.

-   \[0 \] ein Inline-CBV-Deskriptor (Stamm Deskriptoren)
-   \[1 \] eine Deskriptortabelle mit 2 Srvs, 1 cbvs und 1 UAV
-   \[2 \] eine Deskriptortabelle mit einem Sampler
-   \[3 \] eine 4x32-Bit-Auflistung von Stamm Konstanten
-   \[4 \] eine Deskriptortabelle mit einer nicht angegebenen Anzahl von Srvs

In diesem Fall wird erwartet, dass die Anwendung die entsprechende Bindung für jeden der Slots \[ 0.. 4, die \] die Anwendung mit der aktuellen Stamm Signatur definiert hat, festgelegt, bevor Sie eine Draw/Dispatch ausgeben kann. Beispielsweise muss an Slot \[ 1 \] eine Deskriptortabelle gebunden werden, bei der es sich um einen zusammenhängenden Bereich in einem deskriptorheap handelt, der 2 Srvs, 1 cbvs und 1 UAV enthält (oder bei der Ausführung enthalten). Ebenso müssen deskriptortabellen in den Slots \[ 2 und 4 festgelegt werden \] \[ \] .

Die Anwendung kann einen Teil der Stamm Signatur Bindungen gleichzeitig ändern (der Rest bleibt unverändert). Wenn z. b. nur eine der Konstanten an Slot \[ 2 geändert \] werden muss, muss die Anwendung die Bindung wiederherstellen. Wie bereits erläutert, werden die Treiber-/Hardwareversionen alle den Stamm Signatur-Bindungs Status aufweisen, da Sie automatisch geändert werden. Wenn eine Stamm Signatur in einer Befehlsliste geändert wird, werden alle vorherigen Stamm Signatur Bindungen veraltet, und alle neu erwarteten Bindungen müssen vor dem Zeichnen/Dispatch festgelegt werden. Andernfalls ist das Verhalten nicht definiert. Wenn die Stamm Signatur redundant auf denselben Wert festgelegt ist, der zurzeit festgelegt ist, werden vorhandene Stamm Signatur Bindungen nicht veraltet.

## <a name="bundle-semantics"></a>Bündel Semantik

Pakete erben die Stamm Signatur Bindungen der Befehlsliste (die Bindungen zu den verschiedenen Slots im obigen Beispiel der Befehlsliste). Wenn ein Bündel einige der geerbten Stamm Signatur Bindungen ändern muss, muss die Stamm Signatur zuerst auf die gleiche wie die aufrufende Befehlsliste festgelegt werden (die geerbten Bindungen werden nicht veraltet). Wenn das Paket die Stamm Signatur auf andere als die aufrufende Befehlsliste festlegt, hat dies denselben Effekt wie das Ändern der Stamm Signatur in der oben beschriebenen Befehlsliste: alle vorherigen Stamm Signatur Bindungen sind veraltet, und vor zeichnen/Dispatch müssen neue Bindungen festgelegt werden. Andernfalls ist das Verhalten nicht definiert. Wenn ein Bundle keine Stamm Signatur Bindungen ändern muss, muss die Stamm Signatur nicht festgelegt werden.

Der folgende Code zeigt ein Beispiel für einen Flow in ein Bündel.

``` syntax
// Command List
...
pCmdList->SetGraphicsRootSignature(pRootSig); // new parameter space
MyEngine_SetTextures(); // bundle inherits descriptor table setting
MyEngine_SetAnimationFactor(fTime); // bundle inherits root constant
pCmdList->ExecuteBundle(...);
...
// Bundle
pBundle->SetGraphicsRootSignature(pRootSig); // same as caller, in order to inherits bindings
pBundle->SetPipelineState(pPS); 
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,0,drawIDOffset);
pBundle->Draw(...); // using inherited textures / animation factor
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,1,drawIDOffset);
pBundle->Draw(...);
...
```

Wenn Sie aus einem Bundle kommen, werden alle Änderungen des stammlayoutlayouts und/oder Bindungs Änderungen, die ein Bündel vornimmt, in der aufrufenden Befehlsliste geerbt, wenn die Ausführung eines Pakets abgeschlossen ist.

Weitere Informationen zur Vererbung finden Sie im Abschnitt " **Grafik Pipeline State-Vererbung** " unter [Verwalten des Grafik Pipeline Zustands in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> </dl>

 

 




