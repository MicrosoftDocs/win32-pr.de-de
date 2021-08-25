---
title: Suchen von Geräten
description: Die UPnP-Architektur ist eine dynamische Netzwerkarchitektur, mit der Geräte jederzeit eingebunden und das Netzwerk verlassen können.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5626f7d941d9e3fa73b6d3d46ef9f51ef256ee8371e7594c312d225bba865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867590"
---
# <a name="finding-devices"></a>Suchen von Geräten

Die UPnP-Architektur ist eine dynamische Netzwerkarchitektur, mit der Geräte jederzeit eingebunden und das Netzwerk verlassen können. Aufgrund dieser dynamischen Architektur können Sich Anwendungen nicht darauf verlassen, dass bestimmte UPnP-basierte Geräte zu einem bestimmten Zeitpunkt verfügbar sind. Aus diesem Grund durchsuchen Anwendungen (oder Kontrollpunkte) das Netzwerk, um Geräte zu finden, die den angegebenen Kriterien am besten entsprechen. Anwendungen warten auch auf Geräteankündigungsmeldungen, die darauf hinweisen, dass dem Netzwerk neue Geräte hinzugefügt wurden.

Es folgen gültige Suchkriterien für UPnP-basierte Geräte:

-   Gerätetyp
-   Dienstart
-   Eindeutiger Gerätename (UDN)
-   Alle Stammgeräte

Die Suche nach Gerätetyp und Diensttyp wird in der Regel verwendet, um eine Klasse von Geräten mit gemeinsamen Merkmalen zu finden. Die UDN-Suche wird verwendet, um ein bestimmtes Gerät zu finden.

Um nach Geräten zu suchen, muss eine Anwendung zuerst das Device Finder-Objekt instanziieren. Dieses Objekt macht die [**IUPnPDeviceExpo-Schnittstelle**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) verfügbar. die Methoden führen die zuvor beschriebenen Suchvorgänge aus.

In den folgenden Abschnitten wird beschrieben, wie Geräte gesucht werden:

-   [Erstellen der Gerätesuche](creating-the-device-finder.md)
-   [Asynchrone Suche](asynchronous-searching.md)
-   [Synchrone Suche](synchronous-searching.md)
-   [Von synchronen Suchvorgängen zurückgegebene Gerätesammlungen](device-collections-returned-by-synchronous-searches.md)

 

 




