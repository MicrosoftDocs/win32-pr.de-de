---
title: Suchen nach Geräten
description: Die UPnP-Architektur ist eine dynamische Netzwerkarchitektur, mit der Geräte jederzeit beitreten und das Netzwerk verlassen können.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037427"
---
# <a name="finding-devices"></a>Suchen nach Geräten

Die UPnP-Architektur ist eine dynamische Netzwerkarchitektur, mit der Geräte jederzeit beitreten und das Netzwerk verlassen können. Aufgrund dieser dynamischen Architektur können Anwendungen nicht darauf basieren, dass bestimmte UPnP-basierte Geräte zu einem bestimmten Zeitpunkt verfügbar sind. Aus diesem Grund durchsuchen Anwendungen (oder Steuerungs Punkte) das Netzwerk, um Geräte zu finden, die den angegebenen Kriterien am ehesten entsprechen. Anwendungen warten auch auf Geräte Ankündigungs Meldungen, die darauf hinweisen, dass dem Netzwerk neue Geräte hinzugefügt wurden.

Im folgenden finden Sie gültige Suchkriterien für UPnP-basierte Geräte:

-   Gerätetyp
-   Dienstart
-   Eindeutiger Gerätename (UDN)
-   Alle Stamm Geräte

Der Gerätetyp und die Diensttyp Suche werden normalerweise verwendet, um eine Klasse von Geräten mit allgemeinen Merkmalen zu suchen. Die udn-Suche wird verwendet, um ein bestimmtes Gerät zu finden.

Um nach Geräten zu suchen, muss eine Anwendung zuerst das Device Finder-Objekt instanziieren. Dieses Objekt macht die [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) -Schnittstelle verfügbar. die zugehörigen Methoden führen die zuvor beschriebenen Suchvorgänge aus.

In den folgenden Abschnitten wird das Auffinden von Geräten beschrieben:

-   [Erstellen des Geräte Suchgeräts](creating-the-device-finder.md)
-   [Asynchrone Suche](asynchronous-searching.md)
-   [Synchrone Suche](synchronous-searching.md)
-   [Von synchronen suchen zurückgegebene Geräte Sammlungen](device-collections-returned-by-synchronous-searches.md)

 

 




