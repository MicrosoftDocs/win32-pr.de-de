---
title: Ressourcenbindung
description: Bindung ist der Prozess, bei dem Ressourcenobjekte mit den Shadern der Grafikpipeline verknüpft werden.
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93ca7fb75e65c58aee2b2dffbb220830e2911f2c8d7ce9186a09926fa11373f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912244"
---
# <a name="resource-binding"></a>Ressourcenbindung

Bindung ist der Prozess, bei dem Ressourcenobjekte mit den Shadern der Grafikpipeline verknüpft werden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [Übersicht über Ressourcenbindungen](resource-binding-flow-of-control.md) | Der Schlüssel zur Ressourcenbindung in DirectX 12 sind die Konzepte eines *Deskriptors,* *deskriptortabellen,* *Deskriptorheaps* und einer *Stammsignatur.* |
| [Unterschiede im Bindungsmodell von Direct3D 11](binding-model.md) | Eine der wichtigsten Entwurfsentscheidungen hinter der DirectX12-Bindung besteht darin, sie von anderen Verwaltungsaufgaben zu trennen. Dies stellt einige Anforderungen an die App, um bestimmte potenzielle Risiken zu bewältigen. |
| [Deskriptoren](descriptors.md) | Deskriptoren sind die primäre Bindungseinheit für eine einzelne Ressource in D3D12. |
| [Deskriptorheaps](descriptor-heaps.md) | Ein Deskriptorheap ist eine Auflistung zusammenhängender Zuordnungen von Deskriptoren, eine Zuordnung für jeden Deskriptor. |
| [Deskriptortabellen](descriptor-tables.md) | Eine Deskriptortabelle ist logisch ein Array von Deskriptoren. |
| [Stammsignaturen](root-signatures.md) | Die Stammsignatur definiert, welche Ressourcentypen an die Grafikpipeline gebunden sind. |
| [Abfragen der Funktionalität](capability-querying.md) | Ihre Anwendung kann mit einem Aufruf von [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)den Grad der Unterstützung für die Ressourcenbindung und viele andere Features ermitteln. |
| [Ressourcenbindung in HLSL](resource-binding-in-hlsl.md) | In diesem Thema werden einige spezifische Features der Verwendung von [HLSL-Shadermodell 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) (High Level Shader Language) mit Direct3D 12 beschrieben. Die gesamte Direct3D 12-Hardware unterstützt shader Model 5.1, sodass die Unterstützung für dieses Modell nicht von der Hardwarefeatureebene abhängt. |
| [UMA-Optimierungen: Barrierefreie CPU-Texturen und Swizzle-Standardtest](default-texture-mapping.md) | UMA-GPUs (Universal Memory Architecture) bieten einige Effizienzvorteile gegenüber diskreten GPUs, insbesondere bei der Optimierung für mobile Geräte. Wenn Sie Ressourcen CPU-Zugriff erteilen, wenn die GPU UMA ist, kann die Menge an Kopiervorgang zwischen CPU und GPU reduziert werden. Anwendungen sollten zwar keinen blinden CPU-Zugriff auf alle Ressourcen in UMA-Entwürfen gewähren, aber es gibt Möglichkeiten, die Effizienz zu verbessern, indem sie den richtigen Ressourcen CPU-Zugriff gewähren. Im Gegensatz zu diskreten GPUs kann die CPU technisch gesehen einen Zeiger auf alle Ressourcen haben, auf die die GPU zugreifen kann. |
| [Typisiertes Laden von ungeordneten Zugriffsansichten](typed-unordered-access-view-loads.md) | Unordered Access View (UAV) Typed Load ist die Möglichkeit für einen Shader, aus einem UAV mit einem bestimmten [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)zu lesen. |
| [Menge gekachelter Ressourcen](volume-tiled-resources.md) | Volumentexturen (3D) können als kachelbasierte Ressourcen verwendet werden. Dabei wird darauf hinzuweisen, dass die Kachelauflösung dreidimensional ist. |
| [Unterressourcen](subresources.md) | Beschreibt, wie eine Ressource in Unterressourcen unterteilt wird und wie auf eine einzelne, mehrere oder einen Slice von Unterressourcen verwiesen wird. |

## <a name="related-topics"></a>Zugehörige Themen

* [Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)
* [Videotutorials für erweitertes DirectX-Lernen: Ressourcenbindung in DirectX 12](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [Speicherverwaltung](memory-management.md)