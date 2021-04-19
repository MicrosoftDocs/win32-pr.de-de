---
title: Teredo-Komponenten
ms.assetid: 95d83030-b1de-4f09-b9d0-f443d9672ca1
description: 'Weitere Informationen zu: Teredo-Komponenten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b4de66f38d5eb64b8321b6bb89e78fbb763e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343249"
---
# <a name="teredo-components"></a>Teredo-Komponenten

Die [Teredo](about-teredo.md) -Infrastruktur besteht aus den folgenden Komponenten:

## <a name="teredo-clients"></a>Teredo-Clients

Bei einem Teredo-Client handelt es sich um einen IPv6/IPv4-Knoten, der eine Teredo-Tunnelingschnittstelle unterstützt, über die Pakete auf andere Teredo-Clients oder Knoten im IPv6-Internet (über ein Teredo-Relay) getunniert werden. Ein Teredo-Client kommuniziert mit einem Teredo-Server, um ein Adress Präfix zu erhalten, von dem eine Teredo-basierte IPv6-Adresse konfiguriert oder verwendet wird, um die Kommunikation mit anderen Teredo-Clients oder-Hosts im IPv6-Internet zu vereinfachen.

Windows XP mit Service Pack 1 (SP1) mit dem Advanced Networking Pack, Windows XP mit Service Pack 2 (SP2), Windows Server 2003 mit Service Pack 1 (SP1), Windows Server 2003 mit Service Pack 2 (SP2), Windows Vista und Windows Server 2008 enthalten den Teredo-Client.

## <a name="teredo-servers"></a>Teredo-Server

Bei einem Teredo-Server handelt es sich um einen IPv6/IPv4-Knoten, der mit dem IPv4-Internet und dem IPv6-Internet verbunden ist und eine Teredo-Tunnelingschnittstelle unterstützt, über die Pakete empfangen werden. Die allgemeine Rolle des Teredo-Servers besteht darin, die Adress Konfiguration von Teredo-Clients zu unterstützen und die anfängliche Kommunikation zwischen Teredo-Clients und anderen Teredo-Clients oder zwischen Teredo-Clients und reinen IPv6-Hosts zu vereinfachen. Der Teredo-Server lauscht an UDP-Port 3544 für Teredo-Datenverkehr.

Im Gegensatz zum-Client ist der Teredo-Server nicht in Microsoft-Betriebsplattformen enthalten. Um die Kommunikation zwischen Windows-basierten Teredo-Client Computern zu vereinfachen, hat Microsoft Teredo-Server im IPv4-Internet bereitgestellt.

## <a name="teredo-relays"></a>Teredo-Relays

Ein Teredo-Relay ist ein IPv6/IPv4-Router, der Pakete zwischen Teredo-Clients im IPv4-Internet (mit einer Teredo-Tunnelingschnittstelle) und reinen IPv6-Hosts weiterleiten kann. In einigen Fällen interagiert das Teredo-Relay mit einem Teredo-Server, um die anfängliche Kommunikation zwischen Teredo-Clients und reinen IPv6-Hosts zu vereinfachen. Das Teredo-Relay lauscht an UDP-Port 3544 für Teredo-Datenverkehr.

Ebenso wie der Teredo-Server beinhalten Microsoft-Betriebsplattformen keine Teredo-Relayfunktionen. Microsoft plant derzeit nicht die Bereitstellung von Teredo-Relays im IPv4-Internet. Teredo-Relays sind nicht erforderlich, um mit Teredo-Host spezifischen Relays zu kommunizieren.

## <a name="teredo-host-specific-relays"></a>Teredo-Host-Specific Relays

Die Kommunikation zwischen Teredo-Clients und IPv6-Hosts, die mit einer globalen Adresse konfiguriert sind, muss über ein Teredo-Relay durchlaufen werden. Dies ist für reine IPv6-Hosts erforderlich, die mit dem IPv6-Internet verbunden sind. Wenn der IPv6-Host jedoch IPv6 und IPv4-fähig ist und sowohl mit dem IPv4-Internet als auch mit dem IPv6-Internet verbunden ist, muss die Kommunikation zwischen dem Teredo-Client und dem IPv6-Host über das IPv4-Internet erfolgen, anstatt das IPv6-Internet zu durchlaufen und ein Teredo-Relay durchlaufen zu müssen.

Ein Host spezifisches Teredo-Relay ist ein IPv6/IPv4-Knoten, der über eine Schnittstelle und Konnektivität mit dem IPv4-Internet und dem IPv6-Internet verfügt und direkt mit Teredo-Clients über das IPv4-Internet kommunizieren kann, ohne dass ein zwischenteredo-Relay erforderlich ist. Die Konnektivität mit dem IPv4-Internet kann über eine öffentliche IPv4-Adresse oder über eine private IPv4-Adresse und eine benachbarte NAT erfolgen. Die Konnektivität mit dem IPv6-Internet kann über eine direkte Verbindung mit dem IPv6-Internet oder über eine IPv6-Übergangstechnologie wie IPv6-zu-IPv4 erfolgen, bei der IPv6-Pakete über das IPv4-Internet hinweg getunniert werden. Das Host spezifische Teredo-Relay lauscht an UDP-Port 3544 für Teredo-Datenverkehr.

Windows XP mit SP1 mit dem Advanced Networking Pack, Windows XP mit SP2, Windows Server 2003 mit SP1, Windows Server 2003 mit SP2, Windows Vista und Windows Server 2008 enthalten die Host spezifische Teredo-Relayfunktion, die automatisch aktiviert wird, wenn dem Computer eine globale Adresse zugewiesen ist. Eine globale Adresse wird in einer empfangenen Routerankündigungs Nachricht von einem systemeigenen IPv6-Router, einem ISATAP-Router oder einem IPv6-zu-IPv4-Router zugewiesen. Wenn der Computer nicht über eine globale Adresse verfügt, ist die Teredo-Client Funktion aktiviert.

Das Host spezifische Teredo-Relay ermöglicht Teredo-Clients die effiziente Kommunikation mit IPv6-zu-IPv4-Hosts, IPv6-Hosts mit einem nicht-IPv6-zu-IPv4-globalen Präfix oder ISATAP-Hosts oder 6over4-Hosts in Organisationen, die ein globales Präfix für Ihre Adressen verwenden, sofern beide Hosts eine Version von Windows verwenden, die Teredo unterstützt

 

 




