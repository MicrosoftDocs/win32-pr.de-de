---
title: Multicast-Gruppen-Manager-Client
description: Ein Client ist eine Entität, die eine MGM-Funktion aufruft, z. b. ein Routing Protokoll oder eine administrative Anwendung.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714064"
---
# <a name="multicast-group-manager-client"></a>Multicast-Gruppen-Manager-Client

Ein Client ist eine Entität, die eine MGM-Funktion aufruft, z. b. ein Routing Protokoll oder eine administrative Anwendung.

Die MGM-API wird hauptsächlich von Multicast Routing Protokollen verwendet. Entwickler von Multicast Routing Protokollen verwenden die MGM-API für Folgendes:

-   Beibehalten der Gruppenmitgliedschaft
-   Steuerungs Schnittstellen Besitz
-   Empfangen von Benachrichtigungen vom Multicast-Gruppen-Manager bezüglich anderer Multicast Routing Protokolle Anforderungen für Multicast Daten

Bestimmte administrative Anwendungen, die MFEs (Multicast-Weiterleitungs Einträge) überwachen müssen, können dies ohne hinzufügen oder Entfernen von Gruppenmitgliedschaften tun. Entwickler von Administratoren verwenden bestimmte MGM-Funktionen zum Überprüfen von Informationen in MFEs.

> [!Note]  
> Multicast Routing Protokolle greifen auch auf MFEs zu.

 

Ein MFE leitet Informationen weiter, die vom Multicast-Gruppen-Manager basierend auf der Gruppenmitgliedschaft erstellt werden. Die vom Multicast-Gruppen-Manager abgerufenen MFEs können statistische Informationen bereitstellen. Eine administrative Anwendung kann diese Informationen dann verwenden, um die entsprechenden Aktionen zu bestimmen. Beispielsweise kann eine administrative Anwendung Aktionen ausführen, die auf der Menge der Pakete auf einer bestimmten Schnittstelle basieren.

 

 




