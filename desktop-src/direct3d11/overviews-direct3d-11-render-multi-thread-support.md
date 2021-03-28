---
title: Überprüfen der Treiberunterstützung
description: In diesem Thema wird erläutert, wie Sie bestimmen können, ob Multithreading-Funktionen (einschließlich Ressourcen Erstellung und Befehlslisten) für die Hardwarebeschleunigung unterstützt werden.
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae42bbb3eedb76d049479839d497a79db81b5697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992775"
---
# <a name="how-to-check-for-driver-support"></a>Vorgehensweise: Überprüfen der Treiberunterstützung

In diesem Thema wird erläutert, wie Sie bestimmen können, ob Multithreading-Funktionen (einschließlich [Ressourcen Erstellung](overviews-direct3d-11-render-multi-thread-intro.md) und [Befehlslisten](overviews-direct3d-11-render-multi-thread-command-list.md)) für die Hardwarebeschleunigung unterstützt werden.

Es wird empfohlen, dass Anwendungen auf die Unterstützung von Grafikhardware von Multithreading überprüfen. Wenn die Treiber-und Grafikhardware keine Multithread-Objekt Erstellung unterstützt, kann die Leistung auf folgende Weise eingeschränkt werden:

-   Das Erstellen mehrerer Objekte (auch unterschiedlicher Typen) kann gleichzeitig eingeschränkt sein.
-   Das Erstellen eines Objekts, während Grafikbefehle mithilfe eines [unmittelbaren Kontexts](overviews-direct3d-11-render-multi-thread-render.md) gerendert werden, ist möglicherweise eingeschränkt. Wenn z. b. das Multithreading von der Hardware nicht unterstützt wird, sollte eine Anwendung ein Objekt, das für die Erstellung sehr lange Zeit benötigt, nicht in einem Hintergrund Thread erstellen. Ein Erstellungs Vorgang, der sehr lange dauert, kann das sofortige Kontext Rendering blockieren und das Risiko einer visuellen Frame Rate erhöhen.

Die Laufzeit unterstützt das Multithreading und Befehlslisten unabhängig von der Unterstützung von Treibern und Hardware. Wenn keine Treiber-und Hardwareunterstützung für Multithreads oder Befehlslisten vorhanden ist, wird die Funktionalität von der Laufzeit emuliert. Weitere Informationen zum Multithreading finden Sie unter [Einführung in Multithreading in Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).

**So überprüfen Sie die Treiberunterstützung für Multithreading:**

1.  Initialisieren Sie ein [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstellen Objekt. Das Multithreading ist standardmäßig aktiviert.
2.  Wenden Sie sich an [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Übergeben *Sie den* D3D11- **featurethreading \_ \_** -Wert an den Featureparameter, übergeben Sie die [**D3D11 \_ Feature \_ Data \_ Threading**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) -Struktur an den *pfeaturesupportdata* -Parameter, und übergeben Sie die Größe der **\_ \_ Daten \_ Thread** Struktur der D3D11-Funktion an den Parameter " *featuresupportdatasize* ".
3.  Wenn die [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) -Methode erfolgreich ist, wird die [**D3D11 \_ Feature \_ Data \_ Threading**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) -Struktur, die Sie im vorherigen Schritt übermittelt haben, mit Informationen zur Multithreading-Unterstützung initialisiert.
    -   Wenn " **driverconcurrentcreate** " den Wert " **true**" hat, kann ein Treiber mehr als eine Ressource gleichzeitig (gleichzeitig) in verschiedenen Threads erstellen.

        Wenn **drivercommandlists** den Wert **true** hat, unterstützt der Treiber Befehlslisten. Das heißt, dass renderingbefehle, die von einem unmittelbaren Kontext ausgegeben werden, gleichzeitig mit der Objekt Erstellung in separaten Threads mit geringem Risiko einer Frame Rate Stutter erfolgen können.

    -   Wenn " **driverconcurrentcreation** " den Wert " **false**" hat, unterstützt ein Treiber keine gleichzeitige Erstellung. Dies bedeutet, dass die Menge der möglichen Parallelität äußerst eingeschränkt ist. Von der Grafikhardware können keine Objekte verschiedener Typen in verschiedenen Threads simuliert werden. Darüber hinaus kann die Grafikhardware keinen unmittelbaren Kontext verwenden, um renderbefehle auszugeben, während die Grafikhardware versucht, eine Ressource in einem anderen Thread zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




