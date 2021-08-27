---
title: Beispiele für Stammsignaturen
description: Der folgende Abschnitt zeigt Stammsignaturen, deren Komplexität von leer bis vollständig variiert.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2332a6efb36b309c5dc74a8578a0be9d2f46298375c309872cae8718d5bc5950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529411"
---
# <a name="example-root-signatures"></a>Beispiele für Stammsignaturen

Der folgende Abschnitt zeigt Stammsignaturen, deren Komplexität von leer bis vollständig variiert.

-   [Eine leere Stammsignatur](#an-empty-root-signature)
-   [Eine Konstante](#one-constant)
-   [Hinzufügen einer Stammkonst konstanten Pufferansicht](#adding-a-root-constant-buffer-view)
-   [Binden von Deskriptortabellen](#binding-descriptor-tables)
-   [Eine komplexere Stammsignatur](#a-more-complex-root-signature)
-   [Streaming-Shader-Ressourcenansichten](#streaming-shader-resource-views)
-   [Zugehörige Themen](#related-topics)

## <a name="an-empty-root-signature"></a>Eine leere Stammsignatur

![Eine leere Stammsignatur verfügt über keine Bindungen.](images/root-tables-0.png)

Eine leere Stammsignatur ist wahrscheinlich nicht nützlich, kann aber in einem trivialen Rendering-Durchgang verwendet werden, bei dem nur der Eingabe-Assembler und minimale Vertex- und Pixel-Shader verwendet werden, die nicht auf Deskriptoren zugreifen. Auch die Phasen "Blend", "Renderziel" und "Tiefen-Schablone" sind verfügbar, auch mit einer leeren Stammsignatur.

## <a name="one-constant"></a>Eine Konstante

![eine einzelne Stammkonst constant](images/root-tables-constant.png)

Im API-Bindungsslot wird das Stammargument für diesen Parameter zum Zeitpunkt des Befehlslistendatensatz gebunden. Die Anzahl der API-Bindungsslots ist implizit, basierend auf der Reihenfolge der Parameter in der Stammsignatur (der erste ist immer 0 (null). Im HLSL-Bindungsslot wird für den Shader der Stammparameter angezeigt. Der Typ ("uint" im obigen Beispiel) ist der Hardware nicht bekannt, sondern nur ein Kommentar im Image. Die Hardware sieht einfach das einzelne DWORD als Inhalt.

Um eine Konstante zur Befehlslisten-Datensatzzeit zu binden, wird ein Befehl ähnlich dem folgenden verwendet:

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a>Hinzufügen einer Stammkonst konstanten Pufferansicht

![fügt der Stammsignatur eine konstante Pufferansicht hinzu.](images/root-tables-cbv.png)

In diesem Beispiel werden zwei Stammkonst constants und eine Stamm-CBV (Constant Buffer View) gezeigt, die zwei DWORD-Slots kostet.

Verwenden Sie zum Binden einer konstanten Pufferansicht einen Befehl wie den folgenden. Beachten Sie, dass der erste Parameter (2) der in der Abbildung angezeigte Slot ist. In der Regel wird ein Array von Konstanten eingerichtet und dann den Shadern bei b0 als CBV zur Verfügung gestellt.

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a>Binden von Deskriptortabellen

![fügt Deskriptortabellen zur Stammsignatur hinzu.](images/root-tables-2.png)

In diesem Beispiel wird die Verwendung von zwei Deskriptortabellen veranschaulicht: Eine, die eine Tabelle mit fünf Deskriptoren deklariert, die zur Ausführungszeit in einem CBV SRV-UAV-Deskriptorhap verfügbar ist, und eine andere, die eine Tabelle mit zwei Deskriptoren deklariert, die zur Ausführungszeit in einem \_ \_ Samplerdeskriptor-Heap angezeigt wird.

So binden Sie Deskriptortabellen beim Aufzeichnen einer Befehlsliste.

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

Ein weiteres Feature der Stammsignatur ist die Float4-Stammkonst constant, die vier DWORDS-Größen hat. Der folgende Befehl bindet nur die mittleren zwei DWORDS der vier.

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a>Eine komplexere Stammsignatur

![eine komplexe Stammsignatur mit vielen Elementen](images/root-tables-3.png)

Dieses Beispiel zeigt eine dichte Stammsignatur mit den meisten Typen von Einträgen. Zwei der Deskriptortabellen (an den Slots 3 und 6) enthalten Arrays mit ungebundener Größe. Die Last besteht hier in der Anwendung, nur gültige Deskriptoren in einem Heap zu berühren. Für ungebundene oder sehr große Arrays ist die Hardwareebene 2 und mehr der Ressourcenbindungsunterstützung erforderlich.

Es gibt zwei statische Sampler (gebunden ohne Stammsignaturslots).

Bei Slot 9 werden UAV u4 und UAV u5 am gleichen Deskriptortabellenoffset deklariert. Dies ist die Verwendung eines Aliasdeskriptors. Ein Deskriptor im Arbeitsspeicher wird sowohl als u4 als auch als u5 in den HLSL-Shadern angezeigt. In diesem Fall muss der Shader mit der OPTION D3D10 SHADER RESOURCES MAY ALIAS oder der Option \_ \_ oder in \_ \_ `/res_may_alias` FXC kompiliert werden. Aliasdeskriptoren ermöglichen es einem Deskriptor, an mehrere Bindungspunkte gebunden zu werden, ohne änderungen an den Shadern vornehmen zu müssen.

## <a name="streaming-shader-resource-views"></a>Streaming-Shader-Ressourcenansichten

![Streamen von Shaderressourcenansichten in dieser Stammsignatur](images/root-tables-4.png)

Diese Stammsignatur veranschaulicht ein Szenario, in dem alle SRVs ein- und aus einem großen Array gestreamt werden. Zur Ausführungszeit kann eine Deskriptortabelle einmal festgelegt werden, wenn die Stammsignatur festgelegt wird. Anschließend werden alle Texturlesewerte durch Indizierung in das Array über Konstanten durchgeführt, die über die ersten Stammargumente gespeist werden. Es wird nur ein einzelner Deskriptorhap benötigt und nur aktualisiert, wenn Texturen in oder aus freien Deskriptorslots gestreamt werden.

Die Deskriptoroffsets im großen Heap werden von Shadern identifiziert, die die Konstanten in den Konstantenpufferansichten verwenden. Wenn einem Shader beispielsweise eine Material-ID gegeben wird, kann er mithilfe der -Konstante in das eine große Array indizieren, um auf den erforderlichen Deskriptor zu zugreifen (der auf die erforderliche Textur verweist).

Für dieses Szenario ist Hardware mit Ressourcenbindungsebene2+erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardwareebenen für Die Ressourcenbindung](hardware-support.md)
</dt> <dt>

[Ressourcenbindung in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Stammsignaturen](root-signatures.md)
</dt> </dl>

 

 




