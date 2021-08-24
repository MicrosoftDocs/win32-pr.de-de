---
title: Multithreading
description: Direct3D 11 implementiert Unterstützung für die Objekterstellung und das Rendering mit mehreren Threads.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 718d80d9b70db0d6102d746168f338ddd8099339cee349724d87036714b16580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124325"
---
# <a name="multithreading"></a>Multithreading

Direct3D 11 implementiert Unterstützung für die Objekterstellung und das Rendering mit mehreren Threads.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                   | Beschreibung                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Einführung in das Multithreading in Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | Multithreading wurde entwickelt, um die Leistung durch gleichzeitiges Ausführen von Arbeiten mit einem oder mehreren Threads zu verbessern. <br/>                                                                                                         |
| [Objekterstellung mit Multithreading](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | Verwenden Sie [**die ID3D11Device-Schnittstelle,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) um Ressourcen und Objekte zu erstellen, und verwenden Sie [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) zum [Rendern von](overviews-direct3d-11-render-multi-thread-render.md).<br/> |
| [Sofortiges und verzögertes Rendering](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | Direct3D 11 unterstützt zwei Arten von Rendering: unmittelbar und verzögert. Beide werden mithilfe der [**ID3D11DeviceContext-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) implementiert.<br/>                                                      |
| [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | Eine Befehlsliste ist eine Sequenz von GPU-Befehlen, die aufgezeichnet und abgespielt werden können. Eine Befehlsliste kann die Leistung verbessern, indem der von der Laufzeit generierte Mehraufwand reduziert wird.<br/>                                    |
| [Threadingunterschiede zwischen Direct3D-Versionen](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | Viele Multithread-Programmiermodelle verwenden Synchronisierungsprimitiven (z. B. Mutexe), um kritische Abschnitte zu erstellen und zu verhindern, dass von mehreren Threads gleichzeitig auf Code zugegriffen wird.<br/>                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[How To: Check for Driver Support](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[Rendering](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





