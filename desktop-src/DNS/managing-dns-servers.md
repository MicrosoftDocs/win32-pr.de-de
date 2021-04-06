---
title: Verwalten von DNS-Servern
description: Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS abschließt.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712426"
---
# <a name="managing-dns-servers"></a>Verwalten von DNS-Servern

Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS abschließt. DNS-Server enthalten Dateien, so genannte *Zonendateien*, die es Ihnen ermöglichen, Namen in IP-Adressen aufzulösen (oder umgekehrt). Beim Abfragen antwortet ein DNS-Server auf eine von drei Arten:

-   Der Server gibt die angeforderte Namensauflösung oder IP-Auflösungsinformationen zurück.
-   Der Server gibt einen Zeiger auf einen anderen DNS-Server zurück, der die Anforderung bedienen kann.
-   Der Server gibt an, dass er nicht über die angeforderten Informationen verfügt.

DNS-Server können während der Vorbereitung der Rückgabe der angeforderten Auflösungsinformationen möglicherweise andere DNS-Server Abfragen. Darüber hinaus führen DNS-Server keine Vorgänge aus, die nicht in der vorherigen Liste aufgeführt sind.

Es gibt drei Hauptarten von DNS-Servern – primäre Server, sekundäre Server und Cache Server. Weitere Informationen zu diesen DNS-Servern finden Sie unter [DNS-Server](dns-servers.md) .

## <a name="administration-steps"></a>Verwaltungsschritte

Der DNS-WMI-Anbieter ermöglicht die Verwaltung von DNS-Servern vom Server selbst oder von Remote Hosts aus. Die folgenden allgemeinen Schritte zum Verwalten eines DNS-Servers mit dem DNS-WMI-Anbieter sind erforderlich:

-   Herstellen einer Verbindung mit dem DNS-WMI-Anbieter
-   Eine Serverinstanz wird erhalten.
-   Auflisten oder Ändern einer Server Eigenschaft oder Verwenden einer Methode

Um zu veranschaulichen, wie diese Verwaltungsschritte implementiert werden, werden Beispiele bereitgestellt. Die folgenden Aufgaben sind mit den zugehörigen Skript Beispielen verknüpft.

-   [Beenden eines DNS-Servers](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Starten eines DNS-Servers](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Neustarten eines DNS-Servers](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Hinzufügen einer IP-Adresse](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Entfernen einer IP-Adresse](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Auflisten von DNS-Server Eigenschaften](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Anzeigen von DNS-Server Eigenschafts Typen](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Ändern von DNS-Server Eigenschaften](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




