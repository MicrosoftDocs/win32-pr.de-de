---
title: Implementieren eines gehosteten Geräts
description: Der Geräte Host mit der UPnP-Technologie implementiert die zentralen UPnP-Protokolle Ermittlung, Beschreibung, Steuerung und Ereignis Ereignisse.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713577"
---
# <a name="implementing-a-hosted-device"></a>Implementieren eines gehosteten Geräts

Der Geräte Host mit der UPnP-Technologie implementiert die zentralen UPnP-Protokolle: Ermittlung, Beschreibung, Steuerung und Ereignisse. Der Entwickler, der ein gehosteter Gerät implementiert, muss nur Folgendes bereitstellen:

-   Eine Beschreibung des Geräts und seiner Dienste.
-   Eine Implementierung der Funktionalität des Geräts.

Beispielsweise muss der Entwickler eines uhrgeräts UPnP-basierte Geräte-und Dienst Beschreibungen für das Gerät und eine Implementierung der Clock-Funktionen bereitstellen (z. b. die Zeit, die Festlegung der Zeit und die Reaktion auf Abfragen für die aktuelle Zeit). Geräte Host:

-   Kündigt das Gerät gemäß dem UPnP Discovery-Protokoll an.
-   Reagiert auf Abfragen für die Beschreibung des Geräts.
-   Leitet Steuerungsanforderungen an den Teil des Geräte Codes weiter, der die Clock-Funktionen implementiert.
-   Verwaltet Ereignis Abonnements für Dienste.
-   Sendet Ereignis Benachrichtigungen an Abonnenten, wenn sich der Dienststatus ändert.

 

 




