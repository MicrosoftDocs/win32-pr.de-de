---
title: Vorgänge für Kachelpools
description: In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für Kachel Pools ausführen können.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209252"
---
# <a name="operations-available-on-tile-pools"></a>Vorgänge für Kachelpools

In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für Kachel Pools ausführen können.

-   Die Lebensdauer von Kachel Pools funktioniert wie jede andere Direct3D-Ressource, die durch die Verweis Zählung unterstützt wird, einschließlich der Nachverfolgung von Zuordnungen aus gekachelten Ressourcen. Wenn die Anwendung nicht mehr auf einen Kachel Pool verweist und alle Kachel Zuordnungen zum Arbeitsspeicher verschwunden sind und der GPU-Zugriff (Graphics Processing Unit) abgeschlossen ist, hebt das Betriebssystem die Zuordnung des Kachel Pools auf.
-   APIs, die sich auf die Freigabe und Synchronisierung von Oberflächen beziehen, funktionieren für Kachel Pools (aber nicht direkt auf Kacheln). Ähnlich wie das Verhalten für angebotene Kachel Pools werden Direct3D-Befehle, die auf gekachelte Ressourcen zugreifen, die auf einen Kachel Pool zeigen, gelöscht, wenn der Kachel Pool freigegeben wurde und zurzeit von einem anderen Gerät und Prozess abgerufen wird.
-   [**ID3D11DeviceContext2:: resizetilepool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) -Vorgang
-   [**IDXGIDevice2:: offerresources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) -und [**reclaimresources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) -Vorgänge: Diese APIs für die vorübergehende Bereitstellen von Speicher für das System arbeiten für den gesamten Kachel Pool (und sind für einzelne gekachelte Ressourcen nicht verfügbar). Wenn eine gekachelte Ressource auf eine Kachel in einem angebotenen Kachel Pool zeigt, verhält sich die Kachel Ressource so, als ob Sie angeboten wird (z. b. wenn die Laufzeit Befehle löscht, die auf diese Kachel verweisen).

Daten können nicht direkt in den und aus dem Arbeitsspeicher des Kachel Pools kopiert werden. Der Zugriff auf den Arbeitsspeicher erfolgt immer über gekachelte Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Kachel Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

 