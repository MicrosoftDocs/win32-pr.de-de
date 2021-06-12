---
title: Verwalten von DNS-Servern
description: Erfahren Sie mehr über das Verwalten von DNS-Servern. Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS ab schließt.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010773"
---
# <a name="managing-dns-servers"></a>Verwalten von DNS-Servern

Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS ab schließt. DNS-Server enthalten Dateien, die als *Zonendateien* bezeichnet werden, die es ihnen ermöglichen, Namen in IP-Adressen aufzulösen (oder umgekehrt). Bei der Abfrage antwortet ein DNS-Server auf eine von drei Arten:

-   Der Server gibt die angeforderten Informationen zur Namensauflösung oder IP-Auflösung zurück.
-   Der Server gibt einen Zeiger auf einen anderen DNS-Server zurück, der die Anforderung ausführen kann.
-   Der Server gibt an, dass er nicht über die angeforderten Informationen verfügt.

DNS-Server können während der Vorbereitung der Rückgabe der angeforderten Auflösungsinformationen andere DNS-Server abfragen. Darüber hinaus führen DNS-Server jedoch nur die in der vorherigen Liste erwähnten Vorgänge aus.

Es gibt drei Hauptarten von DNS-Servern: primäre Server, sekundäre Server und Cacheserver. Weitere [Informationen zu diesen DNS-Servern](dns-servers.md) finden Sie unter DNS-Server.

## <a name="administration-steps"></a>Verwaltungsschritte

Der DNS-WMI-Anbieter ermöglicht die Verwaltung von DNS-Servern vom Server selbst oder von Remotehosts. Die allgemeinen Schritte, die zum Verwalten eines DNS-Servers mithilfe des DNS-WMI-Anbieters erforderlich sind, sind:

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
-   [Anzeigen von DNS-Servereigenschaftstypen](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Ändern von DNS-Servereigenschaften](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




