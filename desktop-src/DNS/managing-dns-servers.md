---
title: Verwalten von DNS-Servern
description: Erfahren Sie mehr über das Verwalten von DNS-Servern. Ein DNS-Server ist ein Computer, der den Vorgang der Namensauflösung in DNS abschließt.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccce0b6c4a292e2fe46ec8584a601deee9267d2c5f1bfdeebaefa05db630f437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433380"
---
# <a name="managing-dns-servers"></a>Verwalten von DNS-Servern

Ein DNS-Server ist ein Computer, der den Vorgang der Namensauflösung in DNS abschließt. DNS-Server enthalten Dateien, sogenannte *Zonendateien,* die es ihnen ermöglichen, Namen in IP-Adressen aufzulösen (oder umgekehrt). Bei der Abfrage antwortet ein DNS-Server auf eine von drei Arten:

-   Der Server gibt die angeforderten Namensauflösungs- oder IP-Auflösungsinformationen zurück.
-   Der Server gibt einen Zeiger auf einen anderen DNS-Server zurück, der die Anforderung bedienen kann.
-   Der Server gibt an, dass er nicht über die angeforderten Informationen verfügt.

DNS-Server können während der Vorbereitung auf die Rückgabe der angeforderten Auflösungsinformationen andere DNS-Server abfragen. Darüber hinaus führen DNS-Server jedoch keine anderen Vorgänge aus als die in der vorherigen Liste erwähnten.

Es gibt drei Hauptarten von DNS-Servern: primäre Server, sekundäre Server und Cacheserver. Weitere Informationen zu diesen [DNS-Servern](dns-servers.md) finden Sie unter DNS-Server.

## <a name="administration-steps"></a>Verwaltungsschritte

Der DNS-WMI-Anbieter ermöglicht die Verwaltung von DNS-Servern vom Server selbst oder von Remotehosts. Die allgemeinen Schritte, die zum Verwalten eines DNS-Servers mit dem DNS-WMI-Anbieter erforderlich sind, sind:

-   Herstellen einer Verbindung mit dem DNS-WMI-Anbieter
-   Abrufen einer Serverinstanz
-   Auflisten oder Ändern einer Servereigenschaft oder Verwenden einer Methode

Um zu veranschaulichen, wie diese Verwaltungsschritte implementiert werden, werden Beispiele bereitgestellt. Die folgenden Aufgaben sind mit den zugehörigen Skriptbeispielen verknüpft.

-   [Beenden eines DNS-Servers](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Starten eines DNS-Servers](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Neustarten eines DNS-Servers](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Hinzufügen einer IP-Adresse](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Entfernen einer IP-Adresse](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Auflisten von DNS-Servereigenschaften](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Anzeigen von DNS-Servereigenschaftentypen](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Ändern von DNS-Servereigenschaften](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




