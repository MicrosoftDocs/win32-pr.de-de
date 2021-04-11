---
title: Server seitige NAP-Architektur
description: Server seitige NAP-Architektur
ms.assetid: b05c52d5-1f90-41d4-a540-d20e70e54bcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dac585d3c455a1a40f2037b71c0e33cd2bd4847
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101295"
---
# <a name="nap-server-side-architecture"></a>Server seitige NAP-Architektur

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die serverseitige NAP-Plattformarchitektur verwendet Computer, auf denen Windows Server 2008 ausgeführt wird. Die folgende Abbildung zeigt die Architektur der serverseitigen Unterstützung für die NAP-Plattform, bestehend aus Windows-basierten NAP-Erzwingungs Punkten und einem NAP-Integritäts Richtlinien Server.

![Architektur der serverseitigen Unterstützung für die NAP-Plattform](images/nap-server-side-arch.png)

Ein Windows-basierter NAP-Erzwingungs Punkt verfügt über eine Ebene von NAP-Erzwingungs Server-Komponenten. Jede NAP es ist für einen anderen Typ von Netzwerk Zugriff oder-Kommunikation definiert. Beispielsweise gibt es eine NAP es für RAS-VPN-Verbindungen und eine NAP es für die DHCP-Konfiguration. Der NAP es wird in der Regel mit einem bestimmten Typ von NAP-fähiertem Client abgeglichen. Beispielsweise ist die DHCP-NAP es für die Verwendung mit einem DHCP-basierten NAP-Erzwingungs Client (EC) konzipiert. Softwarehersteller von Drittanbietern oder Microsoft können zusätzliche NAP-Zugriffsmöglichkeiten für die NAP-Plattform bereitstellen. Ein NAP es ruft das System Statement of Health (SSOH) aus dem entsprechenden NAP EC ab und sendet es an einen NAP-Integritäts Richtlinien Server als Anbieter spezifisches VSA (Remote Authentication Dial-in User Service)-Attribut (VSA) der [RADIUS-Access-Request Nachricht](https://www.ietf.org/rfc/rfc2865.txt?number=2865) .

Wie in der Abbildung der serverseitigen Architektur gezeigt, verfügt der NAP-Integritäts Richtlinien Server über die folgenden Komponenten:

-   Netzwerk Richtlinien Server-Dienst (NPS)

    Empfängt die RADIUS-Access-Request Nachricht, extrahiert das SSOH und übergibt es an die NAP-Verwaltungs Server Komponente. Der NPS-Dienst wird mit Windows Server 2008 bereitgestellt.

-   NAP-Verwaltungs Server

    Ermöglicht die Kommunikation zwischen dem NPS-Dienst und den System Integritätsprüfungen (SHVs). Die NAP-Verwaltungs Server Komponente wird mit der NAP-Plattform bereitgestellt.

-   Eine Schicht von SHV-Komponenten

    Jeder SHV ist für einen oder mehrere Typen von Systemintegritäts Informationen definiert und kann mit einem SHA verglichen werden. Beispielsweise könnte ein SHV für ein Antivirenprogramm vorhanden sein. Ein SHV kann mit einem oder mehreren Integritäts Anforderungs Servern abgeglichen werden. Beispielsweise wird ein SHV zum Überprüfen von Antivirensignaturen mit dem Server abgeglichen, der die neueste Signatur Datei enthält. SHVs müssen nicht über einen entsprechenden Integritäts Anforderungs Server verfügen. Ein SHV kann nur NAP-fähige Clients anweisen, lokale Systemeinstellungen zu überprüfen, um sicherzustellen, dass eine Host basierte Firewall aktiviert ist. Windows Server 2008 enthält die Windows-Sicherheitsintegritätsprüfung (WSHV). Zusätzliche SHVs werden von Softwareherstellern von Drittanbietern oder von Microsoft als Add-ons für die NAP-Plattform bereitgestellt.

-   SHV-API

    Bietet eine Reihe von Funktionsaufrufen, mit denen sich SHVs bei der NAP-Verwaltungs Serverkomponente registrieren, SoHs (Receive Statement of Health) von der NAP-Verwaltungs Serverkomponente und Send Statement of Health-Antworten (sostd) an die NAP-Verwaltungs Serverkomponente senden können. Die SHV-API wird mit der NAP-Plattform bereitgestellt. Sehen Sie sich die folgenden NAP-Schnittstellen an: [**inapsystemhealthvalidator**](inapsystemhealthvalidator.md) und [**inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md).

Wie bereits erwähnt, besteht die gängigste Konfiguration für die serverseitige NAP-Infrastruktur aus NAP-Erzwingungs Punkten, die den Netzwerk Zugriff oder die Kommunikation mit einem bestimmten Typ bereitstellen, und separate NPS-Integritäts Richtlinien Server, die die System Integritätsprüfung Der NPS-Dienst kann als NAP-Integritäts Richtlinien Server auf einzelnen Windows-basierten NAP-Erzwingungs Punkten installiert werden. Allerdings muss in dieser Konfiguration jeder NAP-Erzwingungs Punkt separat mit Netzwerk Zugriffs-und Integritäts Richtlinien konfiguriert werden. Die empfohlene Konfiguration ist die Verwendung separater NAP-Integritäts Richtlinien Server.

Die gesamte NAP-Architektur besteht aus den folgenden Komponenten:

-   Die drei NAP-Client Komponenten (eine SHA-Schicht, der NAP-Agent und eine NAP EC Ebene).
-   Die vier serverseitigen NAP-Komponenten (eine SHV-Schicht, der NAP-Verwaltungs Server, der NPS-Dienst und eine NAP es Schicht auf Windows-basierten NAP-Erzwingungs Punkten).
-   Der Integritäts Anforderungs Server, bei dem es sich um Computer handelt, die aktuelle System Integritäts Anforderungen für NAP-Integritäts Richtlinien Server erfüllen können
-   Wiederherstellungs Server, bei denen es sich um Computer mit Integritäts Update Ressourcen handelt, auf die NAP-Clients zugreifen können, um ihren nicht kompatiblen Zustand zu beheben.

In der folgenden Abbildung sind die Beziehungen zwischen den Komponenten der NAP-Plattform dargestellt.

![Beziehungen zwischen den Komponenten der NAP-Plattform](images/nap-components.png)

Beachten Sie, dass die folgenden Komponenten Sätze übereinstimmen:

-   NAP-ECS und NAP ESs sind in der Regel mit Übereinstimmungen.

    Beispielsweise wird die DHCP-NAP EC auf dem NAP-Client mit der DHCP-NAP es auf dem DHCP-Server verglichen.

-   SHA-und Wiederherstellungs Server können abgeglichen werden.

    Beispielsweise wird ein Antivirus-SHA auf dem Client mit einem Wiederherstellungs Server für Antivirensignaturen abgeglichen.

-   SHVs und Integritäts Anforderungs Server können abgeglichen werden.

    Beispielsweise kann ein Antivirus-SHV auf dem NAP-Integritäts Richtlinien Server mit einem antivirenintegritäts-Anforderungs Server abgeglichen werden.

Softwarehersteller von Drittanbietern können die NAP-Plattform wie folgt erweitern:

-   Erstellen Sie eine neue Methode, mit der die Integrität eines NAP-Clients ausgewertet wird.

    Softwarehersteller von Drittanbietern müssen einen SHA für den NAP-Client, einen SHV für den NAP-Integritäts Richtlinien Server und ggf. Integritäts Anforderungen und Wiederherstellungs Server erstellen. Wenn die Integritäts-oder Wiederherstellungs Server bereits vorhanden sind, z. b. ein Antivirensignatur-Verteilungs Server, müssen nur die entsprechenden SHA-und SHV-Komponenten erstellt werden. In einigen Fällen werden keine Integritäts Anforderungen oder Wartungs Server benötigt.

-   Erstellen Sie eine neue Methode zum Erzwingen von Integritäts Anforderungen für den Netzwerk Zugriff oder die Kommunikation.

    Softwarehersteller von Drittanbietern müssen eine NAP EC auf dem NAP-Client erstellen. Wenn die Erzwingungs Methode einen Windows-basierten Dienst verwendet, müssen Softwarehersteller von Drittanbietern einen entsprechenden NAP es erstellen, der mit einem NAP-Integritäts Richtlinien Server über das RADIUS-Protokoll kommuniziert, oder indem Sie den auf dem NAP-Erzwingungs Punkt installierten NPS-Dienst als RADIUS-Proxy verwenden.

In den folgenden Abschnitten werden die Komponenten der serverseitigen NAP-Architektur ausführlich beschrieben.

## <a name="nap-enforcement-server"></a>NAP-Durchsetzungs Server

Ein NAP-Erzwingungs Server ermöglicht ein gewisses Maß an Netzwerk Zugriff oder-Kommunikation, kann den Integritäts Status eines NAP-Clients zur Evaluierung an den Netzwerk Integritäts Richtlinien Server übergeben und kann basierend auf der Antwort die Erzwingung des eingeschränkten Netzwerk Zugriffs bereitstellen.

Die in Windows Server 2008 enthaltene NAP-ESs ist wie folgt:

-   Eine IPSec-NAP es für die durch IPSec geschützte Kommunikation.

    Bei der IPSec-geschützten Kommunikation übergibt die Integritäts Registrierungsstelle (Health Registration Authority, HRA), ein Computer mit Windows Server 2008 und Internetinformationsdienste (IIS), der Integritäts Zertifikate von einer Zertifizierungsstelle (Certification Authority, ca) für kompatible Computer erhält, die Integritäts Statusinformationen des NAP-Clients an den NAP-Integritäts Richtlinien Server.

-   Ein DHCP-NAP es für die Konfiguration der DHCP-basierten IP-Adresse.

    Der DHCP-NAP es ist die Funktionalität des DHCP-Server Dienstanbieter, der branchenübliche DHCP-Nachrichten für die Kommunikation mit dem DHCP-NAP EC auf einem NAP-Client verwendet Die DHCP-Erzwingung für eingeschränkten Netzwerk Zugriff erfolgt über DHCP-Optionen.

-   Ein Terminaldienstegateway (Terminaldienstegateway) NAP es für Server-basierte Verbindungen mit Terminal Dienste-Gateway

Für RAS-VPN-und 802.1 x-authentifizierte Verbindungen werden von den Funktionen im NPS-Dienst PEAP-TLV-Nachrichten zwischen NAP-Clients und dem NAP-Integritäts Richtlinien Server verwendet. Die VPN-Erzwingung erfolgt mithilfe von IP-Paket Filtern, die auf die VPN-Verbindung angewendet werden. die 802.1 x-Erzwingung erfolgt auf dem 802.1 x-Netzwerk Zugriffsgerät durch Anwenden von IP-Paket Filtern auf die Verbindung oder durch Zuweisen der Verbindung zu einer VLAN-ID, die dem eingeschränkten Netzwerk entspricht.

## <a name="nap-administration-server"></a>NAP-Verwaltungs Server

Die NAP-Verwaltungs Server Komponente bietet die folgenden Dienste:

-   Ruft die ssohs aus der NAP es über den NPS-Dienst ab.
-   Verteilt die SoHs in den ssohs an die entsprechenden System Integritätsprüfungen (SHV).
-   Sammelt sostd von den SHVs und übergibt sie zur Auswertung an den NPS-Dienst.

## <a name="nps-service"></a>NPS-Dienst

RADIUS ist ein weit verbreitetes Protokoll, das die zentralisierte Authentifizierung, Autorisierung und die Kontoführung für den Netzwerk Zugriff ermöglicht, der in den Anforderungen für Kommentare (RFCs) 2865 und 2866 beschrieben wird. Der ursprünglich für den DFÜ-Remote Zugriff entwickelte RADIUS wird jetzt von drahtlos Zugriffs Punkten unterstützt, indem Ethernet-Switches, VPN-Server, DSL-Zugriffs Server (Digital Subscriber Line) und andere Netzwerk Zugriffs Server authentifiziert werden.

NPS ist die Implementierung eines RADIUS-Servers und-Proxys in Windows Server 2008. NPS ersetzt den Internet Authentifizierungsdienst (IAS) in Windows Server 2003. Für die NAP-Plattform umfasst der NPS-Dienst die NAP-Administrator Server Komponente, Unterstützung für die SHV-API und installierbare SHVs sowie Optionen zum Konfigurieren von Integritäts Richtlinien.

Der NPS-Dienst erstellt basierend auf den SoHRs aus den SHVs und den konfigurierten Integritäts Richtlinien eine System Statement of Health Response (SSoHR), die angibt, ob der NAP-Client kompatibel oder nicht kompatibel ist und den Satz von SoHRs aus den SHVs enthält.

## <a name="system-health-validator-shv"></a>System Integritätsprüfung (SHV)

Ein SHV empfängt einen SoH vom NAP-Verwaltungs Server und vergleicht die System Integritäts Statusinformationen mit dem erforderlichen System Integritäts Zustand. Wenn das SoH beispielsweise aus einem antivirenverzeichnis besteht und die Versionsnummer der letzten Viren Signatur Datei enthält, kann der entsprechende Antivirus-SHV beim Antivirus Health-Anforderungs Server nach der aktuellen Versionsnummer suchen, um das SoH des NAP-Clients zu überprüfen.

Der SHV gibt eine Sohr an den NAP-Verwaltungs Server zurück. Der Sohr kann Informationen darüber enthalten, wie der entsprechende SHA auf dem NAP-Client die aktuellen System Integritäts Anforderungen erfüllen kann. Beispielsweise könnte der vom Antivirus-SHV gesendete SoH den Antivirus-SHA auf dem NAP-Client anweisen, die neueste Version der Antivirensignaturdatei von einem bestimmten Antivirensignatur Server anhand des Namens oder der IP-Adresse anzufordern.

 

 




