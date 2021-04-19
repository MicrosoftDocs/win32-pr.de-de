---
description: 'Microsoft Internet Explorer unterstützt die Verwendung von IPv6 zum Verbinden und Zugreifen auf IPv6-fähige Sites (z. b. Webserver und FTP-Server), wenn die folgenden Bedingungen erfüllt sind: auf dem Host Computer, auf dem Internet Explorer ausgeführt wird, muss IPv6 installiert und aktiviert sein. Beim Herstellen einer Verbindung mit einem Host, der sich außerhalb des lokalen Subnetzes befindet, muss der Schnittstelle, die die Konnektivität bereitstellt, eine Routing fähige IPv6-Adresse zugewiesen werden. Beim Herstellen einer Verbindung mit der IPv6-Loopback Adresse (:: 1) oder mit einem Link-Local-Ziel ist keine Routing fähige IPv6-Adresse erforderlich. Wenn die angeforderte URL einen Namen (z. b. www.contoso.com) enthält, muss die Domain Name System (DNS)-Abfrage für diesen Namen mindestens eine IPv6-Adresse zurückgeben. Wenn die angeforderte URL z. b. eine IPv6-Adresse (z. b.) enthält, muss die IPv6-Adresse in eckige Klammern (https:// \[ :: 1) eingeschlossen werden \] . Bereichs-IDs, die manchmal als Zonen Indizes bezeichnet werden, werden als Teil der IPv6-Adresse unterstützt. Die Bereichs-ID wird verwendet, um zu bestimmen, welche Netzwerkschnittstelle beim Senden der Anforderung auf Computern mit mehreren Netzwerkschnittstellen verwendet werden soll. Die Bereichs-ID wird mit dem Zeichen "%" nach der IPv6-Hauptadresse angegeben (z. b. FE80:: 1% 11). Allerdings muss das Zeichen "%" in der mit Internet Explorer verwendeten URL mit Escapezeichen versehen werden. Beispielsweise würde die Bereichs-ID 11 für eine Verbindungs lokale Adresse als https:// \[ FE80:: 1% 2511 angegeben werden, \] Wenn Internet Explorer verwendet wird. Diese Möglichkeit der Verwendung von IPv6-Adressen in einer URL wird in Internet Explorer 7 und höher unterstützt.'
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: Verwenden von Internet Explorer für den Zugriff auf IPv6-Websites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d11e7b207de132441d2152a4e0593b20bc00d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369762"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>Verwenden von Internet Explorer für den Zugriff auf IPv6-Websites

Microsoft Internet Explorer unterstützt die Verwendung von IPv6 zum Verbinden und Zugreifen auf IPv6-fähige Sites (z. b. Webserver und FTP-Server), wenn die folgenden Bedingungen erfüllt sind:

-   Auf dem Host Computer, auf dem Internet Explorer ausgeführt wird, muss IPv6 installiert und aktiviert sein.
    -   Beim Herstellen einer Verbindung mit einem Host, der sich außerhalb des lokalen Subnetzes befindet, muss der Schnittstelle, die die Konnektivität bereitstellt, eine Routing fähige IPv6-Adresse zugewiesen werden.
    -   Beim Herstellen einer Verbindung mit der IPv6-Loopback Adresse (:: 1) oder mit einem Link-Local-Ziel ist keine Routing fähige IPv6-Adresse erforderlich.
-   Wenn die angeforderte URL einen Namen (z. b. www.contoso.com) enthält, muss die Domain Name System (DNS)-Abfrage für diesen Namen mindestens eine IPv6-Adresse zurückgeben.
-   Wenn die angeforderte URL z. b. eine IPv6-Adresse (z. b.) enthält, muss die IPv6-Adresse in eckige Klammern (https:// \[ :: 1) eingeschlossen werden \] . Bereichs-IDs, die manchmal als Zonen Indizes bezeichnet werden, werden als Teil der IPv6-Adresse unterstützt. Die Bereichs-ID wird verwendet, um zu bestimmen, welche Netzwerkschnittstelle beim Senden der Anforderung auf Computern mit mehreren Netzwerkschnittstellen verwendet werden soll. Die Bereichs-ID wird mit dem Zeichen "%" nach der IPv6-Hauptadresse angegeben (z. b. FE80:: 1% 11). Allerdings muss das Zeichen "%" in der mit Internet Explorer verwendeten URL mit Escapezeichen versehen werden. Beispielsweise würde die Bereichs-ID 11 für eine Verbindungs lokale Adresse als https:// \[ FE80:: 1% 2511 angegeben werden, \] Wenn Internet Explorer verwendet wird. Diese Möglichkeit der Verwendung von IPv6-Adressen in einer URL wird in Internet Explorer 7 und höher unterstützt.

> [!Note]  
> Wenn Internet Explorer für die Verwendung eines Proxy Servers konfiguriert ist, muss dem Proxy Server eine IPv6-Adresse zugewiesen sein, und der Proxy Server muss IPv6-Adressen als Proxy bereitstellen. Der Proxy Server wird zum Herstellen einer Verbindung mit einem externen Host mithilfe von IPv6 verwendet. Der Proxy Server würde normalerweise für die IPv6-Loopback Adresse und IPv6-Link-Local-Adressen umgangen werden.

 

 

 



