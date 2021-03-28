---
title: Objekt Erstellung mit Multithreading
description: Verwenden Sie die ID3D11Device-Schnittstelle zum Erstellen von Ressourcen und Objekten, und verwenden Sie Verknüpfung id3d11devicecontext aus zum Rendern.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947739"
---
# <a name="object-creation-with-multithreading"></a>Objekt Erstellung mit Multithreading

Verwenden Sie die [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstelle zum Erstellen von Ressourcen und Objekten, und verwenden Sie [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) zum [Rendern](overviews-direct3d-11-render-multi-thread-render.md).

Im folgenden finden Sie einige Beispiele für das Erstellen von Ressourcen:

-   [Vorgehensweise: Erstellen eines Scheitelpunkt Puffers](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [Vorgehensweise: Erstellen eines Index Puffers](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [Vorgehensweise: Erstellen eines konstanten Puffers](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [Gewusst wie: Initialisieren einer Textur aus einer Datei](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a>Überlegungen zum Multithreading

Der Umfang der Parallelität beim Erstellen und Rendern von Ressourcen, die Ihre Anwendung erreichen kann, hängt von der durch den Treiber implementierten Multithreadunterstützung ab. Wenn der Treiber gleichzeitige Erstellung unterstützt, sollte die Anwendung weitaus weniger Parallelitäts Probleme aufweisen. Wenn der Treiber die gleichzeitige Objekt Erstellung jedoch nicht unterstützt, ist der Umfang der Parallelität äußerst eingeschränkt. Um zu verstehen, wie viele Unterstützung in einem Treiber verfügbar ist, Fragen Sie den Treiber nach dem Wert des **driverconcurrenterstellungsmembers** der [**D3D11 \_ Feature \_ Data \_ Threading**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) -Struktur ab. Weitere Informationen zum Überprüfen der Treiberunterstützung für Multithreading finden Sie unter Gewusst [wie: Überprüfen der Treiberunterstützung](overviews-direct3d-11-render-multi-thread-support.md).

Gleichzeitige Vorgänge führen nicht zwangsläufig zu einer besseren Leistung. Beispielsweise wird das Erstellen und Laden einer Textur in der Regel durch die Speicherbandbreite begrenzt. Der Versuch, mehrere Texturen zu erstellen und zu laden, ist möglicherweise nicht schneller als eine Textur gleichzeitig, auch wenn dadurch mehrere CPU-Kerne im Leerlauf bleiben. Wenn Sie jedoch mehrere Shader mithilfe mehrerer Threads erstellen, kann dies die Leistung erhöhen, da dieser Vorgang weniger von Systemressourcen wie z. b. der Speicherbandbreite abhängt.

Wenn die Treiber-und Grafikhardware Multithreading unterstützt, können Sie die neu erstellten Ressourcen in der Regel effizienter initialisieren, indem Sie einen Zeiger auf die Anfangsdaten im *pinitialdata* -Parameter übergeben (z. b. in einem Aufrufen der [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) -Methode).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




