---
title: DNS-Server
description: Erfahren Sie mehr über DNS-Server. Ein DNS-Server ist ein Computer, der den Prozess der Namensauflösung in DNS ab schließt.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- DNS-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe2415c50cdd2472b20e8f14123afa2aa919d26
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011253"
---
# <a name="dns-servers"></a>DNS-Server

Ein *DNS-Server* ist ein Computer, der den Prozess der Namensauflösung in DNS ab schließt. DNS-Server enthalten [*Zonendateien,*](z-gly.md) die es ihnen ermöglichen, Namen in IP-Adressen und IP-Adressen in Namen aufzulösen. Bei der Abfrage antwortet ein DNS-Server auf eine von drei Arten:

-   Der Server gibt die angeforderten Namensauflösungs- oder IP-Auflösungsdaten zurück.
-   Der Server gibt einen Zeiger auf einen anderen DNS-Server zurück, der die Anforderung ausführen kann.
-   Der Server gibt an, dass er nicht über die angeforderten Daten verfügt.

DNS-Server können während der Vorbereitung der Rückgabe der angeforderten Auflösungsdaten andere DNS-Server abfragen. Darüber hinaus führen DNS-Server jedoch keine anderen Vorgänge aus.

Es gibt drei Hauptarten von DNS-Servern: primäre Server, sekundäre Server und Cacheserver.

## <a name="primary-server"></a>Primärer Server

Der *primäre Server* ist der autoritative Server für die Zone. Alle administrativen Aufgaben, die der Zone zugeordnet sind (z. B. das Erstellen von Unterdomänen innerhalb der Zone oder andere ähnliche administrative Aufgaben), müssen auf dem primären Server ausgeführt werden. Darüber hinaus müssen alle Änderungen, die der Zone zugeordnet sind, oder Änderungen oder Ergänzungen von RRs in den Zonendateien auf dem primären Server vorgenommen werden. Für jede bestimmte Zone gibt es einen primären Server, außer wenn Sie Active Directory-Dienste und Microsoft DNS-Server integrieren.

## <a name="secondary-servers"></a>Sekundäre Server

*Sekundäre Server* sind DNS-Sicherungsserver. Sekundäre Server empfangen alle ihre Zonendateien aus den Zonendateien des primären Servers in einer Zonenübertragung. Für jede Zone können mehrere sekundäre Server vorhanden [](l-gly.md)sein– so viele wie nötig, um Lastenausgleich, [*Fehlertoleranz*](f-gly.md)und Datenverkehrsreduzierung zu ermöglichen. Darüber hinaus kann jeder DNS-Server ein sekundärer Server für mehrere Zonen sein.

Zusätzlich zu primären und sekundären DNS-Servern können zusätzliche DNS-Serverrollen verwendet werden, wenn solche Server für eine DNS-Infrastruktur geeignet sind. Bei diesen zusätzlichen Servern handelt es sich um [*Zwischenspeicherungsserver und -forwarder.*](f-gly.md)

## <a name="caching-servers"></a>Zwischenspeichern von Servern

[*Zwischenspeichern von*](c-gly.md)Servern, die auch als Server mit ausschließlicher Zwischenspeicherung bekannt sind, wird wie von ihrem Namen vorgeschlagen ausgeführt. Sie stellen nur zwischengespeicherte Abfragedienste für DNS-Antworten zur Verfügung. Anstatt Zonendateien wie andere sekundäre Server zu verwalten, führen dns-Server Zwischenspeicherungsabfragen aus, speichern die Antworten zwischen und geben die Ergebnisse an den abfragenden Client zurück. Der Hauptunterschied zwischen Zwischenspeicherungsservern und anderen sekundären Servern besteht in der Beibehaltung von Zonendateien durch andere sekundäre Server (und gegebenenfalls der Erstellung von Zonenübertragungen, wodurch der Übertragung zugeordneter Netzwerkdatenverkehr generiert wird). Dies gilt nicht für Cacheserver.

 

 




