---
title: Änderungen an der besten Route zu einem Netzwerk
description: Eine Änderung in einem der folgenden Werte für die beste Route zu einem bestimmten Zielnetzwerk bewirkt, dass der Routing Tabellen-Manager eine Benachrichtigungs Meldung generiert, die an jeden registrierten Client und an die Weiterleitungen gesendet wird.
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339428"
---
# <a name="changes-to-the-best-route-to-a-network"></a>Änderungen an der besten Route zu einem Netzwerk

**Windows Server 2003:** Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Neue Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.

Eine Änderung in den folgenden Werten für die beste Route zu einem bestimmten Zielnetzwerk bewirkt, dass der Routing Tabellen-Manager eine Benachrichtigungs Meldung generiert, die an jeden registrierten Client und an die Weiterleitungen gesendet wird:

-   Protokoll Bezeichner
-   Schnittstellen Index
-   Adresse des Routers für den nächsten Hop
-   Protokoll Familien spezifische Daten, die Routingmetriken enthalten

Eine Änderung an der Protokoll Kennung, dem Schnittstellen Index oder der Routeradresse für den nächsten Hop tritt auf, wenn ein neuer, besserer Routen Eintrag hinzugefügt wird oder wenn der aktuelle beste Routen Eintrag gelöscht oder entfernt wird und eine andere Route als neue beste Route verlässt.

 

 




