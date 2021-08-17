---
title: Vorgänge für Kachelpools
description: In diesem Abschnitt werden Vorgänge aufgeführt, die Sie für Kachelpools ausführen können.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c72e15ebe9a8fd2f6725451268d3d03fb7b181442907248d0db44860560aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098322"
---
# <a name="operations-available-on-tile-pools"></a>Vorgänge für Kachelpools

In diesem Abschnitt werden Vorgänge aufgeführt, die Sie für Kachelpools ausführen können.

-   Die Lebensdauer von Kachelpools funktioniert wie jede andere Direct3D-Ressource, die durch Verweiszählung unterstützt wird, einschließlich in diesem Fall der Nachverfolgung von Zuordnungen von gekachelten Ressourcen. Wenn die Anwendung nicht mehr auf einen Kachelpool verweist und alle Kachelzuordnungen zum Arbeitsspeicher nicht mehr vorhanden sind und gpu-Zugriffe (Graphics Processing Unit) abgeschlossen sind, gibt das Betriebssystem die Zuordnung des Kachelpools frei.
-   APIs, die sich auf die Freigabe und Synchronisierung von Oberflächen beziehen, funktionieren für Kachelpools (aber nicht direkt für gekachelte Ressourcen). Ähnlich wie beim Verhalten für angebotene Kachelpools werden Direct3D-Befehle, die auf kachelte Ressourcen zugreifen, die auf einen Kachelpool verweisen, gelöscht, wenn der Kachelpool freigegeben wurde und derzeit von einem anderen Gerät und Prozess erworben wird.
-   [**ID3D11DeviceContext2::ResizeTilePool-Vorgang**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**IDXGIDevice2::OfferResources-**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) und [**ReclaimResources-Vorgänge:**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) Diese APIs zum vorübergehenden Abrufen von Arbeitsspeicher für das System werden für den gesamten Kachelpool ausgeführt (und sind für einzelne gekachelte Ressourcen nicht verfügbar). Wenn eine gekachelte Ressource auf eine Kachel in einem angebotenen Kachelpool verweist, verhält sich die gekachelte Ressource so, als ob sie angeboten wird (z. B. löscht die Laufzeit Befehle, die darauf verweisen).

Daten können nicht direkt in den und aus dem Kachelpoolspeicher kopiert werden. Der Zugriff auf den Arbeitsspeicher erfolgt immer über gekachelte Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von gekachelten Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

 