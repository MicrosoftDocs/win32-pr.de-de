---
description: Im Folgenden finden Sie eine Schritt-für-Schritt-Anleitung für die ersten Schritte beim Programmieren mithilfe der API (Application Programming Interface, Anwendungsprogrammierschnittstelle) des IP-Hilfsprogramms. Es soll ein Verständnis der grundlegenden IP-Hilfsfunktionen und Datenstrukturen sowie deren Zusammenarbeit bieten.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Erste Schritte mit DEM IP-Hilfsfeld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134ca2df12a7d2d2cbd2d0a64f1da07c8aeecd4980fea791bfc19ca018cd87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014158"
---
# <a name="getting-started-with-ip-helper"></a>Erste Schritte mit DEM IP-Hilfsfeld

Im Folgenden finden Sie eine Schritt-für-Schritt-Anleitung für die ersten Schritte beim Programmieren mithilfe der API (Application Programming Interface, Anwendungsprogrammierschnittstelle) des IP-Hilfsprogramms. Es soll ein Verständnis der grundlegenden IP-Hilfsfunktionen und Datenstrukturen sowie deren Zusammenarbeit bieten.

Die Anwendung, die zur Veranschaulichung verwendet wird, ist eine sehr einfache IP-Hilfsanwendung. Erweiterte Codebeispiele sind in den Beispielen enthalten, die im Microsoft Windows Software Development Kit (SDK) enthalten sind.

Der erste Schritt ist für die meisten IP-Hilfsanwendungen identisch.

-   [Erstellen einer einfachen IP-Hilfsanwendung](creating-a-basic-ip-helper-application.md)

In den folgenden Abschnitten werden die verbleibenden Schritte zum Erstellen dieser grundlegenden IP-Hilfsanwendung beschrieben.

-   [Abrufen von Informationen mit GetNetworkParams](retrieving-information-using-getnetworkparams.md)
-   [Verwalten von Netzwerkadaptern mit GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)
-   [Verwalten von Schnittstellen mit GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)
-   [Verwalten von IP-Adressen mit GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)
-   [Verwalten von DHCP-Leases mit ipReleaseAddress und IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [Verwalten von IP-Adressen mit addIPAddress und DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [Abrufen von Informationen mit getIpStatistics](retrieving-information-using-getipstatistics.md)
-   [Abrufen von Informationen mit GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Der vollständige Quellcode für dieses einfache IP-Hilfsbeispiel.

-   [Vollständiger Quellcode der IP-Hilfsanwendung](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a>Erweiterte IP-Hilfsbeispiele

Im Microsoft Windows Software Development Kit (SDK) sind mehrere erweiterte IP-Hilfsprogramme enthalten. Standardmäßig wird der Quellcode des IP-Hilfsdienstbeispiels vom Windows SDK installiert, das für Windows 7 im folgenden Verzeichnis veröffentlicht wurde:

*C: \\ Programme \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples \\ NetDs \\ IPHelp*

Die weiter unten aufgeführten erweiterten Beispiele befinden sich in den folgenden Verzeichnissen:

-   EnableRouter

    Dieses Verzeichnis enthält ein Beispiel, das veranschaulicht, wie die [**IP-Hilfsfunktionen EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) und [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) verwendet werden, um die IPv4-Weiterleitung auf dem lokalen Computer zu aktivieren und zu deaktivieren.

-   iparp

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die IP-Hilfsfunktionen verwendet werden, um Einträge in der IPv4-ARP-Tabelle auf dem lokalen Computer anzuzeigen und zu bearbeiten.

-   ipchange

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie Ip-Hilfsfunktionen verwendet werden, um eine IP-Adresse für einen bestimmten Netzwerkadapter auf Ihrem Computer programmgesteuert zu ändern. Dieses Programm veranschaulicht auch, wie Sie ip-Konfigurationsinformationen für vorhandene Netzwerkadapter abrufen.

-   IPConfig

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie IPv4-Konfigurationsinformationen programmgesteuert abgerufen werden, ähnlich wie IPCONFIG.EXE Hilfsprogramm. Es wird veranschaulicht, wie die [**Funktionen GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) und [**GetAdaptersInfo verwendet**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) werden. Beachten Sie, dass **die GetAdaptersInfo-Funktion** nur IPv4-Informationen abruft.

-   IPRenew

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie IPv4-Adressen, die über DHCP erhalten wurden, programmgesteuert veröffentlicht und erneuert werden. Dieses Programm veranschaulicht auch, wie Sie vorhandene Konfigurationsinformationen für Netzwerkadapter abrufen.

-   Iproute

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die IP-Hilfsfunktionen verwendet werden, um die IPv4-Routingtabelle zu bearbeiten.

-   ipstat

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die IP-Hilfsfunktionen verwendet werden, um IPv4-Verbindungen für ein Protokoll zu zeigen. Standardmäßig werden Statistiken für IP, ICMP, TCP und UDP angezeigt.

-   Netinfo

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die neuen IP-Hilfsprogramm-APIs, die unter Windows Vista und höher eingeführt wurden, zum Anzeigen/Ändern von Adress- und Schnittstelleninformationen für IPv4 und IPv6 verwendet werden.

 

 



