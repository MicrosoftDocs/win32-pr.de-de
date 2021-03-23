---
title: Ressourcen Bindung
description: Die Bindung ist der Prozess, bei dem Ressourcen Objekte mit den Shadern der Grafik Pipeline verknüpft werden.
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086a14beec32447cb91e2a345f4fecda8d5480fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548709"
---
# <a name="resource-binding"></a>Ressourcen Bindung

Die Bindung ist der Prozess, bei dem Ressourcen Objekte mit den Shadern der Grafik Pipeline verknüpft werden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [Übersicht über Ressourcen Bindungen](resource-binding-flow-of-control.md) | Der Schlüssel zur Ressourcen Bindung in DirectX 12 besteht aus den Konzepten eines *Deskriptors*, *deskriptortabellen*, *deskriptorheaps* und einer Stamm *Signatur*. |
| [Unterschiede im Bindungs Modell von Direct3D 11](binding-model.md) | Eine der wichtigsten Entwurfsentscheidungen hinter der DirectX12-Bindung besteht darin, Sie von anderen Verwaltungsaufgaben zu trennen. Dadurch sind einige Anforderungen an die APP erforderlich, um bestimmte potenzielle Gefahren zu verwalten. |
| [Deskriptoren](descriptors.md) | Deskriptoren sind die primäre Bindungs Einheit für eine einzelne Ressource in D3D12. |
| [Deskriptorheaps](descriptor-heaps.md) | Ein deskriptorheap ist eine Auflistung zusammenhängender Belegungen von Deskriptoren, eine Zuordnung für jeden Deskriptor. |
| [Deskriptortabellen](descriptor-tables.md) | Eine Deskriptortabelle ist logisch ein Array von Deskriptoren. |
| [Stamm Signaturen](root-signatures.md) | Die Stamm Signatur definiert, welche Typen von Ressourcen an die Grafik Pipeline gebunden sind. |
| [Funktions Abfrage](capability-querying.md) | Die Anwendung kann den Grad der Unterstützung für die Ressourcen Bindung und viele weitere Features mit einem [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)-Befehl ermitteln. |
| [Ressourcen Bindung in HLSL](resource-binding-in-hlsl.md) | In diesem Thema werden einige spezifische Features der Verwendung des HLSL- [Shader-Modells 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1) (High Level Shader Language) mit Direct3D 12 beschrieben. Alle Direct3D 12-Hardware unterstützt das Shader-Modell 5,1. die Unterstützung für dieses Modell hängt daher nicht von der Hardware Funktionsebene ab. |
| [Umdrehungen-Optimierungen: auf die CPU zugreif Bare Texturen und standardend](default-texture-mapping.md) | Die GPUs der Universal Memory Architecture (UMA) bieten einige Effizienzvorteile gegenüber diskreten GPUs, insbesondere bei der Optimierung mobiler Geräte. Wenn Ressourcen CPU-Zugriff erhalten, wenn die GPU "Uma" ist, kann das Kopieren zwischen CPU und GPU reduziert werden. Wir empfehlen, dass Anwendungen den CPU-Zugriff auf alle Ressourcen bei Uma-Entwürfen Blind gewähren. es gibt jedoch Möglichkeiten, um die Effizienz zu verbessern, indem Sie die richtigen Ressourcen für den CPU-Zugriff Im Gegensatz zu diskreten GPUs kann die CPU technisch einen Zeiger auf alle Ressourcen aufweisen, auf die die GPU zugreifen kann. |
| [Typisierte nicht geordnete zugriffsansichts Ladungen](typed-unordered-access-view-loads.md) | Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)zu lesen. |
| [Menge an Kacheln](volume-tiled-resources.md) | Volumessourcen (3D) können als Kachel Ressourcen verwendet werden, wobei festgestellt wird, dass die Kachel Auflösung dreidimensional ist. |
| [Unterressourcen](subresources.md) | Beschreibt, wie eine Ressource in unter Ressourcen aufgeteilt wird und wie auf eine einzelne, mehrere oder ein Slice von unter Ressourcen verwiesen wird. |

## <a name="related-topics"></a>Verwandte Themen

* [Direct3D 12-Programmier Handbuch](directx-12-programming-guide.md)
* [Video-Tutorials zu DirectX Advanced Learning: Ressourcen Bindung in DirectX 12](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [Speicherverwaltung](memory-management.md)