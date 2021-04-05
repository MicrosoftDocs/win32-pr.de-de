---
title: DNS-Server
description: Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS abschließt.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- DNS-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712240"
---
# <a name="dns-servers"></a>DNS-Server

Ein *DNS-Server* ist ein Computer, der den Prozess der Namensauflösung in DNS abschließt. DNS-Server enthalten [*Zonendateien*](z-gly.md) , mit deren Hilfe Sie Namen in IP-Adressen und IP-Adressen in Namen auflösen können. Wenn eine Abfrage erfolgt, antwortet ein DNS-Server auf eine von drei Arten:

-   Der Server gibt die angeforderte Namensauflösung oder IP-Auflösungs Daten zurück.
-   Der Server gibt einen Zeiger auf einen anderen DNS-Server zurück, der die Anforderung bedienen kann.
-   Der Server gibt an, dass er nicht über die angeforderten Daten verfügt.

DNS-Server können während der Vorbereitung der Rückgabe der angeforderten Auflösungs Daten möglicherweise andere DNS-Server Abfragen, aber darüber hinaus führen DNS-Server keine anderen Vorgänge aus.

Es gibt drei Hauptarten von DNS-Servern – primäre Server, sekundäre Server und Cache Server.

## <a name="primary-server"></a>Primärer Server

Der *primäre Server* ist der autorisierende Server für die Zone. Alle administrativen Aufgaben, die der Zone zugeordnet sind (z. b. das Erstellen von Unterdomänen innerhalb der Zone oder andere ähnliche administrative Aufgaben), müssen auf dem primären Server ausgeführt werden. Außerdem müssen alle Änderungen, die der Zone oder Änderungen oder Erweiterungen in den Zonendateien zugeordnet sind, auf dem primären Server vorgenommen werden. Für eine beliebige Zone gibt es einen primären Server, außer wenn Sie Active Directory-Dienste und den Microsoft DNS-Server integrieren.

## <a name="secondary-servers"></a>Sekundäre Server

*Sekundäre Server* sind Sicherungs-DNS-Server. Sekundäre Server erhalten alle Ihre Zonendateien aus den Zonendateien des primären Servers in einer Zonen Übertragung. Für eine beliebige Zone können mehrere sekundäre Server vorhanden sein – so viele, wie Sie für den [*Lastenausgleich*](l-gly.md), die [*Fehlertoleranz*](f-gly.md)und die Verringerung des Datenverkehrs erforderlich sind. Außerdem kann es sich bei einem DNS-Server um einen sekundären Server für mehrere Zonen handeln.

Zusätzlich zu primären und sekundären DNS-Servern können zusätzliche DNS-Server Rollen verwendet werden, wenn solche Server für eine DNS-Infrastruktur geeignet sind. Diese zusätzlichen Server sind [*Caching-Server*](f-gly.md)und-Weiterleitungen.

## <a name="caching-servers"></a>Zwischenspeichern von Servern

Zwischen speichernde [*Server*](c-gly.md), die auch als nur für das Caching bezeichnete Server bezeichnet werden, werden wie Ihr Name vorgeschlagen. Sie stellen nur den Cache-Query-Dienst für DNS-Antworten bereit. Anstatt Zonendateien wie andere sekundäre Server zu verwalten, führen zwischen Speicherungs-DNS-Server Abfragen aus, speichern die Antworten zwischen und geben die Ergebnisse an den Abfrage Client zurück. Der Hauptunterschied zwischen Cache Servern und anderen sekundären Servern besteht darin, dass andere sekundäre Server Zonendateien verwalten (und ggf. Zonenübertragungen durchführen, um den Netzwerk Datenverkehr zu erzeugen), nicht zwischen Speicherungs Servern.

 

 




