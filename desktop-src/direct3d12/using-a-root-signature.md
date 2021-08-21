---
title: Verwenden einer Stammsignatur
description: Die Stammsignatur ist die Definition einer beliebig angeordneten Auflistung von Deskriptortabellen (einschließlich ihres Layouts), Stammkonstten und Stammdeskriptoren.
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17fdefe5e0f6633cb81755a0344caba7823e24986334bdddba7f20eb309dfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806670"
---
# <a name="using-a-root-signature"></a>Verwenden einer Stammsignatur

Die Stammsignatur ist die Definition einer beliebig angeordneten Auflistung von Deskriptortabellen (einschließlich ihres Layouts), Stammkonstten und Stammdeskriptoren. Für jeden Eintrag werden Kosten in Richtung eines maximalen Grenzwerts an kosten, sodass die Anwendung das Gleichgewicht zwischen der Anzahl der einzelnen Eintragstypen, die in der Stammsignatur enthalten sein werden, ausgleichen kann.

-   [Befehlslistensemantik](#command-list-semantic)
-   [Bündelsemantik](#bundle-semantics)
-   [Zugehörige Themen](#related-topics)

Die Stammsignatur ist ein Objekt, das durch manuelle Spezifikation in der API erstellt werden kann. Alle Shader in einem PSO müssen mit dem mit dem PSO angegebenen Stammlayout kompatibel sein, da die einzelnen Shader sonst eingebettete Stammlayouts enthalten müssen, die miteinander übereinstimmen. Andernfalls kann pso nicht erstellt werden. Eine Eigenschaft der Stammsignatur ist, dass Shader diese beim Erstellen nicht kennen müssen, obwohl Stammsignaturen bei Wunsch auch direkt in Shadern erstellen können. Vorhandene Shaderressourcen erfordern keine Änderungen, um mit Stammsignaturen kompatibel zu sein. ShaderModell 5.1 wurde eingeführt, um zusätzliche Flexibilität zu bieten (dynamische Indizierung von Deskriptoren innerhalb von Shadern) und kann inkrementell übernommen werden, beginnend mit vorhandenen Shaderressourcen nach Wunsch.

## <a name="command-list-semantic"></a>Befehlslistensemantik

Am Anfang einer Befehlsliste ist die Stammsignatur nicht definiert. Grafik-Shader verfügen über eine separate Stammsignatur vom Compute-Shader, die jeweils unabhängig in einer Befehlsliste zugewiesen sind. Der Stammsignatursatz für eine Befehlsliste oder ein Paket muss auch mit dem derzeit festgelegten PSO bei Draw/Dispatch übereinstimmen. Andernfalls ist das Verhalten nicht definiert. Vorübergehende Stammsignaturkonflikte vor Draw/Dispatch sind in Ordnung, z. B. das Festlegen eines inkompatiblen PSO vor dem Wechsel zu einer kompatiblen Stammsignatur (solange diese mit dem Zeitpunkt kompatibel sind, zu dem Draw/Dispatch aufgerufen wird). Durch festlegen eines PSO wird die Stammsignatur nicht geändert. Die Anwendung muss eine dedizierte API zum Festlegen der Stammsignatur aufrufen.

Sobald eine Stammsignatur für eine Befehlsliste festgelegt wurde, definiert das Layout den Satz von Bindungen, die die Anwendung bereitstellen soll, und welche PSOs (mit dem gleichen Layout kompiliert) für die nächsten Draw/Dispatch-Aufrufe verwendet werden können. Beispielsweise kann eine Stammsignatur von der Anwendung so definiert werden, dass sie über die folgenden Einträge verfügen kann. Jeder Eintrag wird als "Slot" bezeichnet.

-   \[0 \] Ein CBV-Deskriptor inline (Stammdeskriptoren)
-   \[1 \] Eine Deskriptortabelle mit 2 SRVs, 1 CBVs und 1 UAV
-   \[2 \] Eine Deskriptortabelle mit 1 Sampler
-   \[3 \] Eine 4x32-Bit-Auflistung von Stammkonst konstanten
-   \[4 \] Eine Deskriptortabelle mit einer nicht angegebenen Anzahl von SRVs

In diesem Fall muss die Anwendung die entsprechende Bindung auf jeden der Slots 0..4 festlegen, die die Anwendung mit ihrer aktuellen Stammsignatur definiert hat, bevor sie eine Draw/Dispatch-Ausgabe erstellen \[ \] kann. Beispielsweise muss an Slot 1 eine Deskriptortabelle gebunden werden. Dies ist ein zusammenhängender Bereich in einem \[ \] Deskriptorhap, der 2 SRVs, 1 CBVs und 1 UAV enthält (oder bei der Ausführung enthalten wird). Ebenso müssen Deskriptortabellen an den Slots \[ 2 \] und \[ 4 festgelegt \] werden.

Die Anwendung kann einen Teil der Stammsignaturbindungen gleichzeitig ändern (der Rest bleibt unverändert). Wenn sich beispielsweise nur eine der Konstanten in Slot 2 ändern muss, muss die Anwendung erneut \[ \] gebunden werden. Wie bereits erwähnt, wird der Bindungsstatus aller Stammsignaturen vom Treiber bzw. der Hardwareversion automatisch geändert. Wenn eine Stammsignatur in einer Befehlsliste geändert wird, werden alle vorherigen Stammsignaturbindungen veraltet, und alle neu erwarteten Bindungen müssen vor Draw/Dispatch festgelegt werden. Andernfalls ist das Verhalten nicht definiert. Wenn die Stammsignatur redundant auf die gleiche festgelegt ist, die derzeit festgelegt ist, werden vorhandene Stammsignaturbindungen nicht veraltet.

## <a name="bundle-semantics"></a>Bündelsemantik

Bundles erben die Stammsignaturbindungen der Befehlsliste (die Bindungen zu den verschiedenen Slots im obigen Befehlslistenbeispiel). Wenn ein Paket einige der geerbten Stammsignaturbindungen ändern muss, muss es zuerst die Stammsignatur so festlegen, dass sie mit der aufrufenden Befehlsliste identisch ist (die geerbten Bindungen werden nicht veraltet). Wenn das Paket die Stammsignatur als anders als die aufrufende Befehlsliste festgelegt hat, hat dies die gleiche Auswirkung wie das Ändern der Stammsignatur in der oben beschriebenen Befehlsliste: Alle vorherigen Stammsignaturbindungen sind veraltet, und neu erwartete Bindungen müssen vor Draw/Dispatch festgelegt werden. Andernfalls ist das Verhalten nicht definiert. Wenn ein Paket keine Stammsignaturbindungen ändern muss, muss es die Stammsignatur nicht festlegen.

Der folgende Code zeigt einen Beispielaufruffluss in ein Paket.

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

Aus einem Bündel heraus werden alle Änderungen am Stammlayout und/oder Bindungsänderungen, die ein Bündel vor sich hat, wieder an die aufrufende Befehlsliste geerbt, wenn die Ausführung eines Pakets abgeschlossen ist.

Weitere Informationen zur Vererbung finden Sie im Abschnitt Vererbung des Grafikpipelinezustands unter Verwalten des [Grafikpipelinezustands in Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md) 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stammsignaturen](root-signatures.md)
</dt> </dl>

 

 




