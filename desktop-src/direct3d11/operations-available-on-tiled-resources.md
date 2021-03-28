---
title: Auf gekachelten Ressourcen verfügbare Vorgänge
description: In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für gekachelte Ressourcen ausführen können.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037386"
---
# <a name="operations-available-on-tiled-resources"></a>Auf gekachelten Ressourcen verfügbare Vorgänge

In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für gekachelte Ressourcen ausführen können.

-   void [**ID3D11DeviceContext2:: updatetilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) und [**ID3D11DeviceContext2:: copytilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) -Vorgänge: Diese Vorgangs Punkt-Kachel Positionen in einer gekachelten Ressource an Positionen in Kachel Pools oder auf NULL oder auf beides. Diese Vorgänge können eine Zusammenhang lose Teilmenge der Kachel Zeiger aktualisieren.
-   Copy \* ()-und Update \* ()-Vorgänge: alle APIs, die Daten in eine und aus einer Standard Pool Oberfläche (z. b. [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) und [**ID3D11DeviceContext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) kopieren können, funktionieren für gekachelte Ressourcen. Beim Lesen von nicht zugeordneten Kacheln wird 0 erzeugt und Schreibvorgänge in nicht zugeordnete Kacheln werden gelöscht.
-   [**ID3D11DeviceContext2:: copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) und [**ID3D11DeviceContext2:: updatetiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) -Vorgänge: diese Vorgänge sind zum Kopieren von Kacheln mit 64 KB-Granularität in und aus einer gekachelten Ressource und einer Puffer Ressource in einem kanonischen Speicher Layout vorhanden. Der Anzeigetreiber und die Hardware führen alle Arbeitsspeicher, die für die gekachelte Ressource erforderlich sind.
-   Direct3D Pipeline Bindungen und Ansichts Erstellungen/-Bindungen, die für nicht-Kachel Ressourcen funktionieren, funktionieren auch für gekachelte Ressourcen.

Kachel Steuerelemente sind in sofortigen oder verzögerten Kontexten verfügbar (genau wie Aktualisierungen typischer Ressourcen), und bei der Ausführung wirkt sich dies auf nachfolgende Zugriffe auf die Kacheln aus (nicht zuvor übermittelte Vorgänge).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Kachel Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

 




