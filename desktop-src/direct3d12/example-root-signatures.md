---
title: Beispiel Stamm Signaturen
description: Der folgende Abschnitt zeigt die Stamm Signaturen, die bei der Komplexität variieren, von leer bis vollständig.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104314"
---
# <a name="example-root-signatures"></a>Beispiel Stamm Signaturen

Der folgende Abschnitt zeigt die Stamm Signaturen, die bei der Komplexität variieren, von leer bis vollständig.

-   [Eine leere Stamm Signatur](#an-empty-root-signature)
-   [Eine Konstante](#one-constant)
-   [Hinzufügen einer Stamm Konstanten-Puffer Ansicht](#adding-a-root-constant-buffer-view)
-   [Bindungs deskriptortabellen](#binding-descriptor-tables)
-   [Eine komplexere Stamm Signatur](#a-more-complex-root-signature)
-   [Streaming-Shader-Ressourcen Sichten](#streaming-shader-resource-views)
-   [Verwandte Themen](#related-topics)

## <a name="an-empty-root-signature"></a>Eine leere Stamm Signatur

![eine leere Stamm Signatur hat keine Bindungen.](images/root-tables-0.png)

Eine leere Stamm Signatur ist wahrscheinlich nicht nützlich, kann aber in einem trivialen Renderingdurchlauf verwendet werden, der nur den Eingabe Assembler verwendet, und minimale Scheitelpunkt-und Pixel-Shader, die nicht auf Deskriptoren zugreifen. Außerdem sind die Phasen Blend, Renderziel und tiefen Schablone verfügbar, auch mit einer leeren Stamm Signatur.

## <a name="one-constant"></a>Eine Konstante

![eine einzelne Stamm Konstante](images/root-tables-constant.png)

Der API-Bindungs Slot ist der Ort, an dem das Root-Argument für diesen Parameter an der Befehlslisten-Daten Satz Zeit gebunden wird. Die Anzahl der API-Bindungs Slots ist implizit, basierend auf der Reihenfolge der Parameter in der Stamm Signatur (die erste ist immer null). Der HLSL-Bindungs Slot ist der Ort, an dem der Shader anzeigt, dass der Root-Parameter angezeigt wird. Der Typ ("uint" im obigen Beispiel) ist der Hardware nicht bekannt, aber es handelt sich nur um einen Kommentar im Image. die Hardware sieht einfach nur das einzige DWORD als Inhalt.

Um eine Konstante an der Befehlslisten-Daten Satz Zeit zu binden, wird ein Befehl ähnlich dem folgenden verwendet:

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a>Hinzufügen einer Stamm Konstanten-Puffer Ansicht

![Fügt der Stamm Signatur eine Konstante Puffer Ansicht hinzu.](images/root-tables-cbv.png)

In diesem Beispiel werden zwei Stamm Konstanten und eine Stamm Konstante-Puffer Ansicht (CBV) gezeigt, die zwei DWORD-Slots kostet.

Verwenden Sie zum Binden einer Konstanten Puffer Ansicht einen Befehl wie den folgenden. Beachten Sie, dass der erste Parameter (2) der Slot ist, der im Bild angezeigt wird. In der Regel wird ein Array von Konstanten eingerichtet und dann den Shadern bei B0 als CBV zur Verfügung gestellt.

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a>Bindungs deskriptortabellen

![Fügt der Stamm Signatur deskriptortabellen hinzu.](images/root-tables-2.png)

Dieses Beispiel zeigt die Verwendung von zwei deskriptortabellen. eine Tabelle mit fünf Deskriptoren, die zur Ausführungszeit in einem CBV \_ -SRV \_ -UAV-deskriptorheap verfügbar ist, und eine andere Tabelle mit zwei Deskriptoren, die zur Ausführungszeit in einem Sampler-deskriptorheap angezeigt werden.

Zum Binden von deskriptortabellen beim Aufzeichnen einer Befehlsliste.

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

Ein weiteres Feature der Stamm Signatur ist die Stamm Konstante float4, die vier DWords groß ist. Mit dem folgenden Befehl werden nur die beiden mittleren DWords der vier Daten gebunden.

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a>Eine komplexere Stamm Signatur

![eine komplexe Stamm Signatur mit vielen Elementen](images/root-tables-3.png)

Dieses Beispiel zeigt eine Dichte Stamm Signatur mit den meisten Typen von Einträgen. Zwei der deskriptortabellen (in den Slots 3 und 6) enthalten Arrays für die unbegrenzte Größe. Der Aufwand für die Anwendung besteht darin, nur gültige Deskriptoren in einem Heap zu berühren. Unbegrenzte oder sehr große Arrays erfordern Hardwareebene 2 + Ressourcen Bindungs Unterstützung.

Es gibt zwei statische Samplern (gebunden ohne Stamm Signatur Slots).

An Slot 9 werden UAV U4 und UAV-U5 mit dem gleichen deskriptortabellenoffset deklariert. Dies wird für einen Alias Deskriptor verwendet, und ein Deskriptor im Arbeitsspeicher wird in den HLSL-Shadern sowohl als als auch als "..." angezeigt. In diesem Fall muss der Shader mit der Option "d3d10 \_ Shader \_ Resources \_ \_ Alias" oder der `/res_may_alias` Option oder in FXC kompiliert werden. Mit Alias Deskriptoren kann ein Deskriptor an mehrere Bindungs Punkte gebunden werden, ohne dass Änderungen an den Shadern vorgenommen werden müssen.

## <a name="streaming-shader-resource-views"></a>Streaming-Shader-Ressourcen Sichten

![Streaming-Shader-Ressourcen Sichten in dieser Stamm Signatur](images/root-tables-4.png)

Diese Stamm Signatur veranschaulicht ein Szenario, in dem alle Srvs in ein und aus einem großen Array gestreamt werden. Zur Ausführungszeit kann eine Deskriptortabelle einmal festgelegt werden, wenn die Stamm Signatur festgelegt ist. Anschließend werden alle Textur Lesevorgänge durch die Indizierung in das Array durch Konstanten durch die ersten Stamm Argumente durchgeführt. Es ist nur ein einzelner deskriptorheap erforderlich, und er wird nur aktualisiert, wenn Texturen in oder aus freien deskriptorslots gestreamt werden.

Die deskriptoroffsets im großen Heap werden durch Shader identifiziert, die die Konstanten in den konstanten Puffer Sichten verwenden. Wenn ein Shader z. b. eine Material-ID erhält, kann er mit der-Konstante in das ein großes Array indizieren, um auf den erforderlichen Deskriptor (der auf die erforderliche Textur verweist) zuzugreifen.

Für dieses Szenario ist Hardware mit Ressourcen Bindung Instanzen + erforderlich.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Hardware Ebenen für die Ressourcen Bindung](hardware-support.md)
</dt> <dt>

[Ressourcen Bindung in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> </dl>

 

 




