---
title: Einführung in das Multithreading in Direct3D 11
description: Multithreading ist darauf ausgelegt, die Leistung zu verbessern, indem Sie die Arbeit mit einem oder mehreren Threads gleichzeitig ausführen.
ms.assetid: b4bef1e4-8d34-455c-8aed-01af974c66c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527b78d8b29a507247c8eb067c20739004ace687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315200"
---
# <a name="introduction-to-multithreading-in-direct3d-11"></a>Einführung in das Multithreading in Direct3D 11

Multithreading ist darauf ausgelegt, die Leistung zu verbessern, indem Sie die Arbeit mit einem oder mehreren Threads gleichzeitig ausführen.

In der Vergangenheit wurde dies häufig durch das Erzeugen eines einzelnen Haupt Threads für das Rendering und eines oder mehrerer Threads für Vorbereitungsaufgaben wie das Erstellen, laden, verarbeiten usw. von Objekten erreicht. Mit der integrierten Synchronisierung in Direct3D 11 besteht das Ziel von Multithreading darin, jeden CPU-und GPU-Cycle zu verwenden, ohne dass ein Prozessor auf einen anderen Prozessor wartet (vor allem, wenn die GPU nicht gewartet wird, weil Sie sich direkt auf die Frame Rate auswirkt). Auf diese Weise können Sie den meisten Arbeitsaufwand generieren und gleichzeitig die beste Framerate beibehalten. Das Konzept eines einzelnen Frames zum Rendern ist nicht mehr erforderlich, da die API die Synchronisierung implementiert.

Multithreading erfordert eine bestimmte Synchronisierungs Form. Wenn z. b. mehrere Threads, die in einer Anwendung ausgeführt werden, auf einen einzelnen Gerätekontext ([**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)) zugreifen müssen, muss diese Anwendung einige Synchronisierungs Mechanismen (z. b. kritische Abschnitte) verwenden, um den Zugriff auf diesen Gerätekontext zu synchronisieren. Dies liegt daran, dass bei der Verarbeitung der Rendering-Befehle (in der Regel auf der GPU) und beim Erzeugen der Rendering-Befehle (in der Regel auf der CPU durch Objekt Erstellung, Laden von Daten, Zustandsänderung, Datenverarbeitung) häufig dieselben Ressourcen (Texturen, Shader, Pipeline Status usw.) verwendet werden. Wenn Sie die Arbeit über mehrere Threads hinweg organisieren, ist eine Synchronisierung erforderlich, um zu verhindern, dass ein Thread Daten ändert, die von einem anderen Thread geändert werden.

Obwohl die Verwendung eines Geräte Kontexts ([**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)) nicht Thread sicher ist, ist die Verwendung eines Direct3D 11-Geräts ([**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) Thread sicher. Da jede **Verknüpfung id3d11devicecontext aus** Single Thread ist, kann jeweils nur ein Thread eine **Verknüpfung id3d11devicecontext aus** -aufrufszeit aufzurufen. Wenn mehrere Threads auf eine einzelne **Verknüpfung id3d11devicecontext aus** zugreifen müssen, müssen Sie einen Synchronisierungs Mechanismus, wie z. b. kritische Abschnitte, verwenden, um den Zugriff auf diese **Verknüpfung id3d11devicecontext aus** zu synchronisieren. Es ist jedoch nicht erforderlich, dass mehrere Threads wichtige Abschnitte oder Synchronisierungs primitive verwenden, um auf eine einzelne **ID3D11Device** zuzugreifen. Wenn eine Anwendung zum Erstellen von Ressourcen Objekten **ID3D11Device** verwendet, ist es daher nicht erforderlich, die Synchronisierung zu verwenden, um mehrere Ressourcen Objekte gleichzeitig zu erstellen.

Multithreading-Unterstützung dividiert die API in zwei unterschiedliche Funktionsbereiche:

-   [Objekt Erstellung mit Multithreading](overviews-direct3d-11-render-multi-thread-create.md)
-   [Sofortiges und verzögertes Rendering](overviews-direct3d-11-render-multi-thread-render.md)

Die Multithreading-Leistung hängt von der Treiberunterstützung ab. Vorgehens [Weise: Überprüfen der Treiberunterstützung](overviews-direct3d-11-render-multi-thread-support.md) bietet weitere Informationen zum Abfragen des Treibers und zu den Ergebnissen der Ergebnisse.

Direct3D 11 wurde von Grund auf für die Unterstützung von Multithreading entwickelt. Direct3D 10 implementiert mithilfe der [Thread sicheren Schicht](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers)eingeschränkte Unterstützung für Multithreading. Auf dieser Seite sind die Verhaltensunterschiede zwischen den beiden Versionen von DirectX aufgeführt: [Threading Unterschiede zwischen Direct3D-Versionen](overviews-direct3d-11-render-multi-thread-differences.md).

## <a name="multithreading-and-dxgi"></a>Multithreading und DXGI

Der unmittelbare Kontext sollte jeweils nur von einem Thread verwendet werden. Allerdings sollte Ihre Anwendung auch denselben Thread für DXGI-Vorgänge (Microsoft DirectX Graphics Infrastructure) verwenden, insbesondere dann, wenn die Anwendung Aufrufe an die [**idxgiswapchain::P Resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) -Methode sendet.

> [!Note]  
> Es ist ungültig, einen unmittelbaren Kontext gleichzeitig mit den meisten der DXGI-Schnittstellen Funktionen zu verwenden. Für DirectX-sdche vom März 2009 und höher sind die einzigen DXGI-Funktionen, die sicher sind, [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)und [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

 

Weitere Informationen zur Verwendung von DXGI mit mehreren Threads finden Sie unter [Überlegungen zu Multithreads](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 