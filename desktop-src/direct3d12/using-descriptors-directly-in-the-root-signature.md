---
title: Verwenden von Deskriptoren direkt in der Stammsignatur
description: Anwendungen können Deskriptoren direkt in die Stamm Signatur einfügen, um zu vermeiden, dass Sie einen deskriptorheap durchlaufen müssen.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548742"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Verwenden von Deskriptoren direkt in der Stammsignatur

Anwendungen können Deskriptoren direkt in die Stamm Signatur einfügen, um zu vermeiden, dass Sie einen deskriptorheap durchlaufen müssen. Diese Deskriptoren belegen viel Platz in der Stamm Signatur (siehe den Abschnitt root Signature Limits), sodass Anwendungen Sie sparsam verwenden müssen.

Ein Beispiel für die Verwendung ist das Platzieren einer Konstanten Puffer Ansicht (Constant Buffer views, CBV), die pro zeichnen im Stamm Layout geändert wird, sodass der deskriptorheap-Speicherplatz nicht von der Anwendung pro zeichnen zugeordnet werden muss (und das verweisen auf eine Deskriptortabelle an der neuen Position im deskriptorheap gespeichert werden). Wenn Sie etwas in die Stamm Signatur einfügen, übergibt die Anwendung lediglich die Versionskontrolle an den Treiber, aber dies ist die Infrastruktur, die Sie bereits haben.

Für das Rendering, das sehr wenige Ressourcen verwendet, ist möglicherweise keine Deskriptortabelle/Heap-Verwendung erforderlich, wenn alle benötigten Deskriptoren direkt in die Stamm Signatur eingefügt werden können.

In der Stamm Signatur werden nur die folgenden deskriptortypen unterstützt:
- Cbvs.
- Shader-Ressourcen Sichten (Srvs)/unordered Access views (UAVs) der Puffer Ressourcen, in denen das SRV/UAV-Format nur 32 Bit Float/uint/Sint-Komponenten enthält (es gibt keine Formatkonvertierung).
- Srvs von Raytracing-beschleunigungsstrukturen in lokalen oder globalen Stamm Signaturen. 

UAVs im Stamm können keine Indikatoren zugeordnet werden. Deskriptoren in der Stamm Signatur werden jeweils als einzelne separate Deskriptoren angezeigt, &mdash; die nicht dynamisch indiziert werden können.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

Im obigen Beispiel `mySceneData` kann nicht als Array deklariert werden, wie in, `cbuffer mySceneData[2]` Wenn es in einem Deskriptor in der Stamm Signatur zugeordnet werden soll, da die Indizierung über Deskriptoren in der Stamm Signatur nicht unterstützt wird. Die Anwendung kann separate einzelne Konstante Puffer definieren und Sie bei Bedarf als separaten Eintrag in der Stamm Signatur definieren. Beachten Sie, dass `mySceneData` ein Array innerhalb von oben vorhanden ist `bar[2]` . Die dynamische Indizierung innerhalb des Konstanten Puffers ist gültig. ein Deskriptor in der Stamm Signatur verhält sich so, wie sich der gleiche Deskriptor verhält, wenn er über einen deskriptorheap aufgerufen wird. Dies steht im Gegensatz zu Inlining-Konstanten direkt in der Stamm Signatur, die auch wie ein konstanter Puffer angezeigt werden, außer mit der Einschränkung, dass die dynamische Indizierung innerhalb der Inline Konstanten nicht zulässig ist `bar[2]` .

Die folgenden APIs (von der [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Schnittstelle) dienen zum Festlegen von Deskriptoren direkt auf der Stamm Signatur:

-   [**Setcomputerootconstantbufferview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**Setgraphicsrootconstantbufferview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**Setcomputerootshaderresourceview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**Setgraphicsrootshaderresourceview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**Setcomputerootunorderedaccessview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**Setgraphicsrootunorderedaccessview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> Es gibt kein Konzept eines "root Deskriptor Array" in Direct3D 12. Deskriptorarrays werden nur in deskriptorheaps unterstützt.

## <a name="related-topics"></a>Verwandte Themen

[Stamm Signaturen](root-signatures.md)
