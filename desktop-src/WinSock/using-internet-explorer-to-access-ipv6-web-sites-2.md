---
description: "Microsoft Internet Explorer unterstützt die Verwendung von IPv6 für die Verbindung und den Zugriff auf IPv6-fähige Websites (z. B. Webserver und FTP-Server), wenn die folgenden Umstände erfüllt sind: Auf dem Hostcomputer, auf dem Internet Explorer ausgeführt wird, muss IPv6 installiert und aktiviert sein. Beim Herstellen einer Verbindung mit einem Host, der sich außerhalb des lokalen Subnetzes befindet, muss der Schnittstelle, die die Konnektivität bereitstellt, eine routingfähige IPv6-Adresse zugewiesen sein. Beim Herstellen einer Verbindung mit der IPv6-Loopbackadresse (::1) oder einem lokalen Linkziel ist keine routingfähige IPv6-Adresse erforderlich. Wenn die angeforderte URL einen Namen enthält (z. B. www.contoso.com), muss die DNS-Abfrage (Domain Name System) für diesen Namen mindestens eine IPv6-Adresse zurückgeben. Wenn die angeforderte URL eine IPv6-Adresse enthält (z.B. ::1), muss die IPv6-Adresse in eckige Klammern (https:// \\[ ::1) eingeschlossen \\] werden. Bereichs-IDs, auch als Zonenindizes bezeichnet, werden als Teil der IPv6-Adresse unterstützt. Die Bereichs-ID wird verwendet, um zu bestimmen, welche Netzwerkschnittstelle beim Senden der Anforderung auf Computern mit mehreren Netzwerkschnittstellen verwendet werden soll. Die Bereichs-ID wird mithilfe des Zeichens '%' nach der IPv6-Hauptadresse angegeben (z.B. fe80::1%11). Das '%'-Zeichen muss jedoch in der mit Internet Explorer verwendeten URL mit Escapezeichen verbunden werden. Beispielsweise würde die Bereichs-ID 11 für eine lokale Linkadresse als https:// \\[ fe80::1%2511 angegeben, \\] wenn Internet Explorer verwendet wird. Diese Möglichkeit, IPv6-Adressen in einer URL zu verwenden, wird ab Internet Explorer 7 unterstützt."
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: Verwenden von Internet Explorer für den Zugriff auf IPv6-Websites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48a9f18e80e0e163ad6fe4ccda0aaef43826edd4becb28e294aad5eca7085c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559271"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>Verwenden von Internet Explorer für den Zugriff auf IPv6-Websites

Microsoft Internet Explorer unterstützt die Verwendung von IPv6 für verbindungen und den Zugriff auf IPv6-fähige Websites (z. B. Webserver und FTP-Server), wenn die folgenden Umstände erfüllt sind:

-   Auf dem Hostcomputer, auf dem Internet Explorer ausgeführt wird, muss IPv6 installiert und aktiviert sein.
    -   Beim Herstellen einer Verbindung mit einem Host, der sich außerhalb des lokalen Subnetzes befindet, muss der Schnittstelle, die die Konnektivität bereitstellt, eine routingfähige IPv6-Adresse zugewiesen sein.
    -   Beim Herstellen einer Verbindung mit der IPv6-Loopbackadresse (::1) oder einem lokalen Linkziel ist keine routingfähige IPv6-Adresse erforderlich.
-   Wenn die angeforderte URL einen Namen enthält (z. B. www.contoso.com), muss die DNS-Abfrage (Domain Name System) für diesen Namen mindestens eine IPv6-Adresse zurückgeben.
-   Wenn die angeforderte URL eine IPv6-Adresse enthält (z.B. ::1), muss die IPv6-Adresse von eckigen Klammern (https:// \[ ::1) umgeben \] sein. Bereichs-IDs, auch als Zonenindizes bezeichnet, werden als Teil der IPv6-Adresse unterstützt. Die Bereichs-ID wird verwendet, um zu bestimmen, welche Netzwerkschnittstelle beim Senden der Anforderung auf Computern mit mehreren Netzwerkschnittstellen verwendet werden soll. Die Bereichs-ID wird mithilfe des Zeichens '%' nach der IPv6-Hauptadresse angegeben (z.B. fe80::1%11). Das '%'-Zeichen muss jedoch in der mit Internet Explorer verwendeten URL mit Escapezeichen verbunden werden. Beispielsweise würde die Bereichs-ID 11 für eine lokale Linkadresse als https:// \[ fe80::1%2511 angegeben, \] wenn Internet Explorer verwendet wird. Diese Möglichkeit, IPv6-Adressen in einer URL zu verwenden, wird ab Internet Explorer 7 unterstützt.

> [!Note]  
> Wenn Internet Explorer für die Verwendung eines Proxyservers konfiguriert ist, muss dem Proxyserver eine IPv6-Adresse zugewiesen sein, und der Proxyserver muss IPv6-Adressen proxyfähig sein. Der Proxyserver wird verwendet, um mithilfe von IPv6 eine Verbindung mit einem externen Host herzustellen. Der Proxyserver wird normalerweise für die IPv6-Loopbackadresse und die lokalen IPv6-Linkadressen umgangen.

 

 

 



