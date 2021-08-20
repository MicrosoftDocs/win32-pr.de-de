---
title: Multicast-Gruppen-Manager-Client
description: Ein Client ist eine Entität, die eine MGM-Funktion aufruft, z. B. ein Routingprotokoll oder eine administrative Anwendung.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2fceda28404e20be5d2c3192b672b1d4e20cb1f95f238f8b561a989c564f6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790423"
---
# <a name="multicast-group-manager-client"></a>Multicast-Gruppen-Manager-Client

Ein Client ist eine Entität, die eine MGM-Funktion aufruft, z. B. ein Routingprotokoll oder eine administrative Anwendung.

Die MGM-API wird hauptsächlich von Multicastroutingprotokollen verwendet. Entwickler von Multicastroutingprotokollen verwenden die MGM-API für folgende Zwecke:

-   Verwalten der Gruppenmitgliedschaft
-   Steuern des Schnittstellenbesitzes
-   Empfangen von Benachrichtigungen vom Multicastgruppen-Manager zu Anforderungen anderer Multicastroutingprotokolle für Multicastdaten

Bestimmte Verwaltungsanwendungen, die Multicastweiterleitungseinträge (MFEs) überwachen müssen, können dies tun, ohne die Gruppenmitgliedschaft hinzuzufügen oder zu entfernen. Entwickler administrativer Anwendungen verwenden bestimmte MGM-Funktionen, um Informationen in MFEs zu überprüfen.

> [!Note]  
> Multicastroutingprotokolle greifen auch auf MFEs zu.

 

Ein MFE leitet Informationen weiter, die der Multicastgruppen-Manager basierend auf der Gruppenmitgliedschaft erstellt. Die MFEs, die vom Multicastgruppen-Manager abgerufen werden, können statistische Informationen bereitstellen. Eine Verwaltungsanwendung kann diese Informationen dann verwenden, um die entsprechenden Aktionen zu bestimmen. Beispielsweise kann eine Verwaltungsanwendung Aktionen ausführen, die auf der Paketmenge auf einer bestimmten Schnittstelle basieren.

 

 




