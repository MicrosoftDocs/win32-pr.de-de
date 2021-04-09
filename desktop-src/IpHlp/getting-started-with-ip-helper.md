---
description: Im folgenden finden Sie eine Schritt-für-Schritt-Anleitung für den Einstieg in die Programmierung mit der IP-Hilfsanwendung (Application Programming Interface, API). Es wurde entwickelt, um ein Verständnis für die grundlegenden IP-Hilfsobjekte und Datenstrukturen und deren Zusammenarbeit zu bieten.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Einführung in das IP-Hilfsprogramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869068"
---
# <a name="getting-started-with-ip-helper"></a>Einführung in das IP-Hilfsprogramm

Im folgenden finden Sie eine Schritt-für-Schritt-Anleitung für den Einstieg in die Programmierung mit der IP-Hilfsanwendung (Application Programming Interface, API). Es wurde entwickelt, um ein Verständnis für die grundlegenden IP-Hilfsobjekte und Datenstrukturen und deren Zusammenarbeit zu bieten.

Die Anwendung, die zur Veranschaulichung verwendet wird, ist eine sehr einfache IP-Hilfsanwendung. Erweiterte Codebeispiele sind in den im Microsoft Windows Software Development Kit (SDK) enthaltenen Beispielen enthalten.

Der erste Schritt ist für die meisten IP-Hilfsanwendungen identisch.

-   [Erstellen einer grundlegenden IP-Hilfsanwendung](creating-a-basic-ip-helper-application.md)

In den folgenden Abschnitten werden die verbleibenden Schritte zum Erstellen dieser grundlegenden IP-Hilfsanwendung beschrieben.

-   [Abrufen von Informationen mithilfe von getnetworkpara Metern](retrieving-information-using-getnetworkparams.md)
-   [Verwalten von Netzwerkadaptern mithilfe von getadaptersinfo](managing-network-adapters-using-getadaptersinfo.md)
-   [Verwalten von Schnittstellen mithilfe von getinterfacetten Info](managing-interfaces-using-getinterfaceinfo.md)
-   [Verwalten von IP-Adressen mit getipaddrtable](managing-ip-addresses-using-getipaddrtable.md)
-   [Verwalten von DHCP-Leases mithilfe von ipreleaseaddress und iprenewaddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [Verwalten von IP-Adressen mit addipaddress und deleteipaddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [Abrufen von Informationen mithilfe von GetIpStatistics](retrieving-information-using-getipstatistics.md)
-   [Abrufen von Informationen mithilfe von GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Der gesamte Quellcode für dieses grundlegende IP-Hilfsobjekt.

-   [Vollständiger IP-hilfsanwendungs-Quellcode](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a>Erweiterte IP-hilfsprogrammbeispiele

Im Microsoft Windows Software Development Kit (SDK) sind mehrere erweiterte IP-hilfsprogrammbeispiele enthalten. In der Standardeinstellung wird der Quellcode des IP-Hilfsskripts von der Windows SDK für Windows 7 im folgenden Verzeichnis installiert:

*C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Beispiele \\ netds \\ iphelp*

Die erweiterten unten aufgeführten Beispiele befinden sich in den folgenden Verzeichnissen:

-   Enablerouter

    Dieses Verzeichnis enthält ein Beispiel, das veranschaulicht, wie die IP-Hilfsfunktionen [**enablerouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) und [**unenablerouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) verwendet werden, um die IPv4-Weiterleitung auf dem lokalen Computer zu aktivieren und zu deaktivieren.

-   iparamep

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die IP-Hilfsfunktionen verwendet werden, um Einträge in der IPv4-ARP-Tabelle auf dem lokalen Computer anzuzeigen und zu bearbeiten.

-   ipchange

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie IP-Hilfsobjekte verwendet werden, um eine IP-Adresse für einen bestimmten Netzwerkadapter auf dem Computerprogramm gesteuert zu ändern. Dieses Programm veranschaulicht auch, wie vorhandene IP-Konfigurationsinformationen für den Netzwerkadapter abgerufen werden.

-   IPConfig

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie Sie die IPv4-Konfigurationsinformationen Programm gesteuert abrufen, ähnlich wie das IPCONFIG.EXE Hilfsprogramm. Es zeigt, wie die Funktionen [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) und [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) verwendet werden. Beachten Sie, dass die **getadaptersinfo** -Funktion nur IPv4-Informationen abruft.

-   Iprenew

    Dieses Verzeichnis enthält ein Beispielprogramm, das die programmgesteuerte Freigabe und Erneuerung von IPv4-Adressen veranschaulicht, die über DHCP abgerufen wurden. Außerdem wird in diesem Programm veranschaulicht, wie vorhandene Konfigurationsinformationen für den Netzwerkadapter abgerufen werden.

-   Iproute

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die IP-Hilfsfunktionen verwendet werden, um die IPv4-Routing Tabelle zu bearbeiten.

-   ipstat

    Dieses Verzeichnis enthält ein Beispielprogramm, das veranschaulicht, wie die IP-Hilfsfunktionen verwendet werden, um IPv4-Verbindungen für ein Protokoll anzuzeigen. Standardmäßig werden Statistiken für IP, ICMP, TCP und UDP angezeigt.

-   NetInfo

    Dieses Verzeichnis enthält ein Beispielprogramm, das die Verwendung der neuen IP-Hilfsobjekte veranschaulicht, die unter Windows Vista und höher eingeführt wurden, um Adress-und Schnittstellen Informationen für IPv4 und IPv6 anzuzeigen bzw. zu ändern.

 

 



