---
title: Direktes Verwenden von Deskriptoren in der Stammsignatur
description: Um zu vermeiden, dass ein Deskriptorhap durchgehen muss, können Sie einen Deskriptor direkt in die Stammsignatur einordnen.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9d459f3195a4cf722ea210edbe63e5c1bf3cc8
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489169"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Direktes Verwenden von Deskriptoren in der Stammsignatur

Um zu vermeiden, dass ein Deskriptorhap durchgehen muss, können Sie einen Deskriptor direkt in die Stammsignatur einordnen. Diese Deskriptoren nehmen viel Speicherplatz in der Stammsignatur ein (siehe [Grenzwerte](/windows/win32/direct3d12/root-signature-limits)für Stammsignaturen). Daher wird empfohlen, sie nur wenig zu verwenden.

Eine Beispielverwendung wäre, im Stammlayout eine konstante Pufferansicht (CONSTANT Buffer View, CBV) zu platzieren, die sich pro Zeichnen ändert. Dies bedeutet, dass der Deskriptor-Heapspeicher nicht von der Anwendung pro Zeichnen zugeordnet werden muss (und speichert das Verweisen auf eine Deskriptortabelle an der neuen Position im Deskriptor-Heap). Indem sie etwas in die Stammsignatur setzt, überliegt die Anwendung lediglich die Verantwortung für die Versionserstellung dem Treiber. aber dies ist die Infrastruktur, über die Treiber bereits verfügen.

Für Rendering, das nur sehr wenige Ressourcen verwendet, ist die Verwendung von Deskriptortabellen/Heaps möglicherweise überhaupt nicht erforderlich, wenn alle erforderlichen Deskriptoren direkt in der Stammsignatur platziert werden können.

Dies sind die einzigen Typen von Deskriptoren, die in der Stammsignatur unterstützt werden.

- Konstantenpufferansicht (CBVs).
- Shaderressourcenansichten (SRVs) bzw. ungeordnete Zugriffsansichten (UNOrdered Access Views, UAVs) von Pufferressourcen, bei denen keine Formatkonvertierung erforderlich ist (nicht typisierte Puffer). Beispiele für nicht typisierte Puffer, die mit Stammdeskriptoren gebunden werden können, sind `StructuredBuffer<type>` `RWStructuredBuffer<type>` , und `ByteAddressBuffer` `RWByteAddressBuffer` . Typierte Puffer wie `Buffer<uint>` und `Buffer<float2>` können nicht.
- SRVs von Raytracingbeschleunigungsstrukturen in lokalen oder globalen Stammsignaturen. 

Einem UAV im Stammverzeichnis können keine Leistungsindikatoren zugeordnet sein. Deskriptoren in der Stammsignatur werden jeweils als einzelne separate Deskriptoren angezeigt, &mdash; die nicht dynamisch indiziert werden können.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

Im obigen Beispiel kann nicht als Array deklariert werden, wie in , wenn es einem `mySceneData` Deskriptor in der Stammsignatur zugeordnet werden `cbuffer mySceneData[2]` soll. Das liegt daran, dass die Deskriptorübergreifende Indizierung in der Stammsignatur nicht unterstützt wird. Bei Wunsch können Sie separate einzelne konstante Puffer definieren und diese jeweils als separaten Eintrag in der Stammsignatur definieren. Beachten `mySceneData` Sie, dass sich in der obigen Ansicht ein Array `bar[2]` befindet. Die dynamische Indizierung innerhalb des Konstantenpuffers ist gültig. Ein Deskriptor in der Stammsignatur verhält sich genauso wie derselbe Deskriptor, wenn über einen &mdash; Deskriptor-Heap darauf zugegriffen wird. Dies steht im Gegensatz zu Inliningkonst konstanten direkt in der Stammsignatur, die auch wie ein konstanter Puffer erscheinen, mit Ausnahme der Einschränkung, dass die dynamische Indizierung innerhalb der Inlinekonst constants nicht zulässig ist und daher dort nicht zulässig `bar[2]` wäre.

Diese APIs (von der [**ID3D12GraphicsCommandList-Schnittstelle)**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) sind zum Festlegen von Deskriptoren direkt in der Stammsignatur.

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!NOTE]  
> Es gibt kein Konzept eines *Stammdeskriptorarrays* in Direct3D 12. Deskriptorarrays werden nur in Deskriptorhaps unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

* [Stammsignaturen](root-signatures.md)
