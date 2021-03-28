---
title: MultiThreading
description: Direct3D 11 implementiert die Unterstützung für das Erstellen und Rendering von Objekten mithilfe mehrerer Threads.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207078"
---
# <a name="multithreading"></a>MultiThreading

Direct3D 11 implementiert die Unterstützung für das Erstellen und Rendering von Objekten mithilfe mehrerer Threads.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Einführung in das Multithreading in Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | Multithreading ist darauf ausgelegt, die Leistung zu verbessern, indem Sie die Arbeit mit einem oder mehreren Threads gleichzeitig ausführen. <br/>                                                                                                         |
| [Objekt Erstellung mit Multithreading](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | Verwenden Sie die [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstelle zum Erstellen von Ressourcen und Objekten, und verwenden Sie [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) zum [Rendern](overviews-direct3d-11-render-multi-thread-render.md).<br/> |
| [Sofortiges und verzögertes Rendering](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | Direct3D 11 unterstützt zwei renderingtypen: direkt und verzögert. Beide werden mithilfe der [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Schnittstelle implementiert.<br/>                                                      |
| [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | Eine Befehlsliste ist eine Sequenz von GPU-Befehlen, die aufgezeichnet und wiedergegeben werden können. Eine Befehlsliste kann die Leistung verbessern, indem der von der Laufzeit generierte Verwaltungsaufwand verringert wird.<br/>                                    |
| [Threading Unterschiede zwischen Direct3D-Versionen](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | Viele multithreadprogrammierungs-Modelle verwenden Synchronisierungs primitive (z. b. Mutexen), um kritische Abschnitte zu erstellen und zu verhindern, dass der Zugriff auf Code von mehreren Threads gleichzeitig erfolgt.<br/>                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorgehensweise: Überprüfen der Treiberunterstützung](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[Darstellung](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





