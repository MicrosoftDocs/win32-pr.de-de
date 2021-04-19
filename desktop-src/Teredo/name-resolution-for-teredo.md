---
title: Namensauflösung für Teredo
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 'Weitere Informationen finden Sie hier: Namensauflösung für Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700b5d40fda0546c29bd7c47ee773977c374784c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362921"
---
# <a name="name-resolution-for-teredo"></a>Namensauflösung für Teredo

Die Teredo-Schnittstelle verwendet derzeit die folgenden Protokolle für die Namensauflösung:

## <a name="domain-name-system"></a>Domain Name System (DNS)

Der Domain Name System (DNS) ist derzeit die wichtigste Technologie zur Namensauflösung im Internet. Die meisten Webserver registrieren URL-Adressen bei DNS-Servern. Allerdings werden die Adressen eines Heimnetzwerks nicht bei DNS-Servern registriert, da die meisten Heimanwender IP-Adressen über das Dynamic Host Configuration-Protokoll (DHCP) von Ihrem Internet Dienstanbieter erhalten. DHCP-Leases haben einen relativ kurzen Zeitraum und können zwischen 48 und 72 Stunden dauern, um einen Namen in der gesamten DNS-Cloud weiterzugeben. Das Ergebnis ist, dass DNS eine ineffektive Methode zum Abrufen der öffentlichen IP-Adresse eines heimbenutzers ist. Eine Teredo-Adresse enthält die öffentliche IPv4-Adresse und erbt daher mindestens die gleiche Volatilität der IPv4-Adressen. Daher sind Teredo-Adressen derzeit nicht in DNS registriert.

## <a name="peer-name-resolution-protocol"></a>Peer Name Resolution-Protokoll

Bei dem Peer Name Resolution Protocol (PNRP) handelt es sich um eine verteilte DNS-Technologie, die IP-Adressen auf Tausenden von Benutzer Computern speichert, die Teil einer PNRP-Cloud sind. Bei Verwendung von Windows Vista kann jeder Heimanwender ein Mitglied einer PNRP-Cloud werden und seine Teredo-IPv6-Adresse im PNRP-Netzwerk ankündigen. Im Gegensatz zu Adressen, die für DNS-Server gelten, nehmen Adressen im PNRP-Netzwerk häufig weniger als eine Minute für die Weitergabe an. Da sich Teredo-Adressen häufig ändern können (externe IPv4-Adressen, die vom Internetdienstanbieter bereitgestellt werden, können sich ändern, oder der vom Internet Gateway-Gerät des Benutzers verwendete externe Port kann sich ändern), hat sich PNRP als effektiver Mechanismus für Privat Benutzer erwiesen. PNRP-Namen, Adressen, die auf ". PNRP.net" enden, basieren auf eindeutigen Systemeigenschaften, die sich nicht ändern. Daher ist ein PNRP-Name eine zuverlässige Möglichkeit zum Herstellen einer Verbindung mit einem Heimbenutzer. Die [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) -API kann verwendet werden, um die IP-Adresse mithilfe der PNRP-Technologie (DNS-Namen, die mit ". PNRP.net" enden) zu erhalten und eine Verbindung mit anderen Hosts herzustellen.

 

 
