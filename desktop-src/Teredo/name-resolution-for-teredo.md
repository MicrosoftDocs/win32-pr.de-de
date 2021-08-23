---
title: Namensauflösung für Teredo
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: Weitere Informationen finden Sie unter Namensauflösung für Teredo.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d9c41685977ef5a4ae3e94996a8d1a59db5f9812e2ed8efe758878a9055c28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001688"
---
# <a name="name-resolution-for-teredo"></a>Namensauflösung für Teredo

Die Teredo-Schnittstelle verwendet derzeit die folgenden Protokolle für die Namensauflösung:

## <a name="domain-name-system"></a>Domain Name System (DNS)

Die Domain Name System (DNS) ist derzeit die bekannteste Technologie zur Namensauflösung im Internet. Die meisten Webserver registrieren URL-Adressen bei DNS-Servern. Die Adressen eines Heimnetzwerks sind jedoch nicht bei DNS-Servern registriert, da die meisten Heimbenutzer IP-Adressen über DHCP (Dynamic Host Configuration Protocol) von ihrem Internetdienstanbieter abrufen. DHCP-Leases haben eine relativ kurze Dauer und dauern zwischen 48 und 72 Stunden, bis ein Name in der gesamten DNS-Cloud verteilt wird. Daher hat sich DNS als ineffektive Methode zum Abrufen der öffentlichen IP-Adresse eines Heimbenutzers erwiesen. Eine Teredo-Adresse enthält die öffentliche IPv4-Adresse und erbt daher mindestens die gleiche Flüchtigkeit der IPv4-Adressen. Daher sind Teredo-Adressen derzeit nicht im DNS registriert.

## <a name="peer-name-resolution-protocol"></a>Peer Name Resolution-Protokoll

Das Peer Name Resolution Protocol (PNRP) ist eine verteilte DNS-Technologie, die IP-Adressen auf Tausenden von Benutzercomputern speichert, die Teil einer PNRP-Cloud sind. Mithilfe von Windows Vista kann jeder Heimbenutzer Mitglied einer PNRP-Cloud werden und seine Teredo IPv6-Adresse im PNRP-Netzwerk ankündigen. Im Gegensatz zu Adressen, die DNS-Servern zur Verfügung gestellt werden, dauert die Propagieren von Adressen im PNRP-Netzwerk häufig weniger als eine Minute. Da sich Teredo-Adressen häufig ändern können (die vom ISP bereitgestellte externe IPv4-Adresse kann sich ändern, oder der vom Internetgatewaygerät des Benutzers verwendete externe Port kann sich ändern), hat sich PNRP als effektiver Mechanismus für Privatbenutzer erwiesen. PNRP-Namen, Adressen, die auf ".pnrp.net" enden, basieren auf eindeutigen Systemeigenschaften, die sich nicht ändern. Daher ist ein PNRP-Name eine zuverlässige Möglichkeit, eine Verbindung mit einem Heimbenutzer herzustellen. Die [**WSAConnectByName-API**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) kann verwendet werden, um ip-Adressen mithilfe der PNRP-Technologie (DNS-Namen, die mit ".pnrp.net" enden) abzurufen und eine Verbindung mit anderen Hosts herzustellen.

 

 
