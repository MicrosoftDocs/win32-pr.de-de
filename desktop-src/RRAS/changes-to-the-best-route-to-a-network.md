---
title: Änderungen an der besten Route zu einem Netzwerk
description: Eine Änderung eines der folgenden Werte für die beste Route zu einem bestimmten Zielnetzwerk bewirkt, dass der Routingtabellen-Manager eine Benachrichtigungsnachricht generiert, die an jeden registrierten Client und an die Weiterleitungen gesendet wird.
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fe96a0b339325c2290c346ba581d5b892db24d1cd972f7a83a0b2ec525eeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030360"
---
# <a name="changes-to-the-best-route-to-a-network"></a>Änderungen an der besten Route zu einem Netzwerk

**Windows Server 2003:** Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Neue Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.

Eine Änderung eines der folgenden Werte für die beste Route zu einem bestimmten Zielnetzwerk bewirkt, dass der Routingtabellen-Manager eine Benachrichtigungsmeldung generiert, die an jeden registrierten Client und an die Weiterleitungen gesendet wird:

-   Protokollbezeichner
-   Schnittstellenindex
-   Adresse des Routers des nächsten Hops
-   Protokollfamilienspezifische Daten, die Routenmetriken enthalten

Eine Änderung der Protokoll-ID, des Schnittstellenindexes oder der Routeradresse des nächsten Hops tritt auf, wenn ein neuer Eintrag mit besserer Route hinzugefügt wird oder wenn der aktuelle Eintrag mit der besten Route gelöscht oder veraltert wird und eine andere Route als neue beste Route verlassen wird.

 

 




