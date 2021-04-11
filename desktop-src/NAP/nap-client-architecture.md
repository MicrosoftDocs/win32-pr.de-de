---
title: NAP-Client Architektur
description: Ein NAP-Client ist ein Computer, auf dem Windows XP mit Service Pack 3 (SP3), Windows Vista oder Windows Server 2008 mit der NAP-Plattform ausgeführt wird.
ms.assetid: 163c33c9-b18b-49f9-a2a1-fd90a1dc0826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15862eaa6ae4f4c1f79c53cf9d540aedec295e8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310991"
---
# <a name="nap-client-architecture"></a>NAP-Client Architektur

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Ein NAP-Client ist ein Computer, auf dem Windows XP mit Service Pack 3 (SP3), Windows Vista oder Windows Server 2008 mit der NAP-Plattform ausgeführt wird.

Diese Abbildung zeigt die Architektur der NAP-Plattform auf einem NAP-Client.

![Architektur der NAP-Plattform auf einem NAP-Client](images/nap-client-side-arch.png)

Die NAP-Client Architektur besteht aus den folgenden Elementen:

-   Eine Schicht von Erzwingungs Client-Komponenten (EC)

    Jede NAP EC ist für einen anderen Typ von Netzwerk Zugriff definiert. Beispielsweise gibt es eine NAP EC für die DHCP-Konfiguration und eine NAP EC für RAS-VPN-Verbindungen. Der NAP EC kann mit einem bestimmten Typ von NAP-Erzwingungs Punkt abgeglichen werden. Beispielsweise ist die DHCP-NAP EC für die Verwendung mit einem DHCP-basierten NAP-Erzwingungs Punkt konzipiert. Einige NAP-ECS werden mit der NAP-Plattform und Drittanbieter-Softwareanbietern bereitgestellt, oder Microsoft kann andere bereitstellen.

-   Eine Ebene der Systemintegritäts-Agent-Komponenten (SHA)

    Eine SHA-Komponente verwaltet und meldet ein oder mehrere Elemente der Systemintegrität. Beispielsweise kann ein SHA für Antivirensignaturen und ein SHA für Betriebssystemupdates vorhanden sein. Ein SHA kann mit einem Wiederherstellungs Server abgeglichen werden. dabei handelt es sich um einen Computer, der Integritäts Update Ressourcen enthält, auf die NAP-Clients zugreifen können, um ihren nicht kompatiblen Zustand zu beheben. Beispielsweise wird ein SHA zum Überprüfen von Antivirensignaturen mit dem Server abgeglichen, der die neueste Antivirus-Signatur Datei enthält. SHAs müssen nicht über einen entsprechenden Wiederherstellungs Server verfügen. Beispielsweise kann ein SHA nur lokale Systemeinstellungen überprüfen, um sicherzustellen, dass eine Host basierte Firewall aktiviert ist. Windows Vista und Windows XP Service Pack 3 enthalten die Windows-Sicherheitsintegritäts-Agent (WSHA), mit der die Einstellungen der Windows-Security Center überwacht werden. Softwarehersteller von Drittanbietern oder Microsoft können zusätzliche SHAs für die NAP-Plattform bereitstellen.

-   NAP-Agent

    Verwaltet die aktuellen Integritäts Zustandsinformationen des NAP-Clients und ermöglicht die Kommunikation zwischen der NAP EC-und SHA-Schicht. Der NAP-Agent wird mit der NAP-Plattform bereitgestellt.

-   Systemintegritäts-Agent-API

    Bietet eine Reihe von Funktionen, mit denen SHAs beim NAP-Agent registriert werden kann, um den Integritäts Status des Systems anzugeben, auf Abfragen des System Integritäts Status vom NAP-Agent zu Antworten und den NAP-Agent zum Übergeben von Systemintegritäts-Wiederherstellungs Informationen an einen SHA zu übergeben. Die SHA-API ermöglicht es Anbietern, zusätzliche SHAs zu erstellen und zu installieren. Die SHA-API wird mit der NAP-Plattform bereitgestellt. Sehen Sie sich die folgenden NAP-Schnittstellen an: [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md), [**inapsystemhealthagentcallback**](inapsystemhealthagentcallback.md)und [**inapsystemhealthagentrequest**](inapsystemhealthagentrequest.md).

Um den Integritäts Status eines bestimmten SHA anzugeben, erstellt ein SHA ein Statement of Health ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) und übergibt es an den NAP-Agent. Ein SoH kann ein oder mehrere Elemente der Systemintegrität enthalten. Beispielsweise kann das SHA für ein Antivirenprogramm ein SoH erstellen, das den Status der auf dem Computer, der Version und des letzten empfangene antivirensignaturupdates, die den Status der Antivirensoftware enthält. Wenn ein SHA seinen Status aktualisiert, erstellt er einen neuen SoH und übergibt ihn an den NAP-Agent. Um den Gesamt Integritäts Status eines NAP-Clients anzugeben, verwendet der NAP-Agent ein System Statement of Health (SSOH), das Versionsinformationen für den NAP-Client und den Satz von SoHs für die installierten SHAs umfasst.

In den folgenden Abschnitten werden die Komponenten der NAP-Client Architektur ausführlicher beschrieben.

## <a name="nap-enforcement-client"></a>NAP-Durchsetzungs Client

Ein NAP-Erzwingungs Client (EC) fordert eine gewisse Zugriffsebene für ein Netzwerk an und übergibt den Integritäts Status des Computers an einen NAP-Erzwingungs Punkt, der den Netzwerk Zugriff bereitstellt. NAP-Erzwingungs Punkte sind Computer oder Netzwerk Zugriffsgeräte, die NAP verwenden oder mit NAP verwendet werden können, um den Integritäts Status eines NAP-Clients zu evaluieren und eingeschränkten Netzwerk Zugriff oder Kommunikation zu ermöglichen. Wenn die Integrität des Computers nicht kompatibel ist, gibt der NAP EC den eingeschränkten Status des NAP-Clients auf andere Komponenten der NAP-Client Architektur an.

Die NAP-ECS für die NAP-Plattform, die unter Windows XP mit SP3, Windows Vista und Windows Server 2008 bereitgestellt wird, lauten wie folgt:

-   Eine IPSec-NAP EC für die durch IPSec geschützte Kommunikation.
-   Ein EAPHost-NAP EC für 802.1 x-authentifizierte Verbindungen.
-   Ein VPN-NAP EC für RAS-VPN-Verbindungen.
-   Ein DHCP-NAP EC für die Konfiguration der DHCP-basierten IPv4-Adresse.
-   Ein TS-Gateway-NAP EC für Terminaldienstegateway-Verbindungen.

Für Windows XP mit SP3 gibt es separate NAP-ECS für 802.1 x-authentifizierte Kabel-und Drahtlos Verbindungen.

### <a name="ipsec-nap-ec"></a>IPSec-NAP EC

Der IPSec-NAP EC ist eine Komponente, die SSOH vom NAP-Agent abruft und an eine Integritäts Registrierungsstelle (Health Registration Authority, HRA), einen Computer mit Windows Server 2008 und Internetinformationsdienste (IIS) sendet, der Integritäts Zertifikate von einer Zertifizierungsstelle (Certification Authority, ca) für kompatible Computer abruft. Der IPSec-NAP EC wird im NAP-Clientkonfigurations-Snap-in als IPSec-EC der vertrauenden Seite bezeichnet. Der IPSec-NAP EC interagiert auch mit folgendem:

-   Der Zertifikat Speicher zum Speichern des Integritäts Zertifikats.
-   Die IPSec-Komponenten in Windows, um sicherzustellen, dass das Integritäts Zertifikat für die IPSec-geschützte Kommunikation verwendet wird.
-   Die Host basierte Firewall (z. b. die Windows-Firewall), sodass durch die Firewall durch IPSec geschützter Datenverkehr zugelassen wird.

### <a name="eaphost-nap-ec"></a>EAPHost-NAP EC

Der EAPHost-NAP EC ist eine Komponente, die SSOH vom NAP-Agent abruft und Sie als eine Nachricht vom Typ PEAP-Type-Length-Value (TLV) für 802.1 x-authentifizierte Verbindungen sendet. Der EAPHost-NAP EC wird im NAP-Clientkonfigurations-Snap-in als EAP-Quarantäne-EC bezeichnet.

### <a name="vpn-nap-ec"></a>VPN-NAP EC

Der VPN-NAP EC ist die Funktionalität im RAS-Verbindungs-Manager-Dienst, der die SSOH vom NAP-Agent abruft und Sie als PEAP-TLV-Nachricht für RAS-VPN-Verbindungen sendet. Der VPN-NAP EC wird im NAP-Clientkonfigurations-Snap-in als RAS-Quarantäne bezeichnet.

### <a name="dhcp-nap-ec"></a>DHCP-NAP EC

Der DHCP-NAP EC ist die Funktionalität des DHCP-Client diensdienstanbieter, der nach Industriestandard-DHCP-Nachrichten verwendet, um System Integritäts Meldungen und eingeschränkte Informationen Der IPSec-DHCP-EC wird im NAP-Clientkonfigurations-Snap-in als DHCP-Quarantäne-EC bezeichnet. Der DHCP-NAP EC Ruft den SSOH vom NAP-Agent ab. Der DHCP-Client Dienst fragmentiert ggf. das SSOH und setzt jedes Fragment in eine herstellerspezifische DHCP-Option von Microsoft, die in DHCPDISCOVER-, DHCPREQUEST-oder DHCPInform-Nachrichten gesendet wird. Die Nachrichten dhcpablehnen und DHCPRELEASE enthalten nicht den SSOH-Ausdruck.

## <a name="system-health-agent"></a>Systemintegritäts-Agent

Ein Systemintegritäts-Agent (System Health Agent, SHA) führt System Integritäts Updates aus und veröffentlicht seinen Status in Form eines SoH an den NAP-Agent. Der SoH enthält Informationen, die der NAP-Integritäts Richtlinien Server verwenden kann, um zu überprüfen, ob sich der Client Computer im erforderlichen Integritäts Zustand befindet. Ein SHA wird mit einem System Integritäts Prüfungs Punkt (System Health Validator, SHV) auf Serverseite der NAP-Plattformarchitektur abgeglichen. Der entsprechende SHV kann eine SoH-Antwort (SoHR) an den NAP-Client zurückgeben, die von der NAP EC und dem NAP-Agent an den SHA-Agent geleitet wird, um ihn darüber zu informieren, was geschehen soll, wenn sich der SHA nicht in einem erforderlichen Integritäts Zustand befindet. Beispielsweise könnte der von einem Antivirus-SHV gesendete SoH den entsprechenden Antivirus-SHA anweisen, einen Antivirus-Signatur Server abzufragen, um die neueste Version der Antivirus-Signatur Datei abzurufen. Der Sohr kann auch den Namen oder die IP-Adresse des zu Abfrage enden Antivirensignatur Servers einschließen.

Ein SHA kann einen lokal installierten Richtlinien Client verwenden, um die Systemintegritäts-Verwaltungsfunktionen in Verbindung mit einem Richtlinien Server zu unterstützen. Beispielsweise kann ein Software Update-SHA mithilfe der lokal installierten Software Client Software (dem Richtlinien Client) Versions Überprüfung und Installations-und Aktualisierungs Funktionen mit dem Software Update Server (dem Richtlinien Server) ausführen.

## <a name="nap-agent"></a>NAP-Agent

Der NAP-Agent stellt die folgenden Dienste bereit:

-   Sammelt die SoHs von jedem SHA und speichert Sie zwischen. Der SoH-Cache wird immer dann aktualisiert, wenn ein SHA ein neues oder aktualisiertes SoH bereitstellt.
-   Speichert den SSOH und stellt ihn auf Anforderung an den NAP-ECS bereit.
-   Übergibt Benachrichtigungen an SHAs, wenn sich der eingeschränkte Zustand ändert.
-   Behält den eingeschränkten Systemzustand bei und sammelt Statusinformationen von jedem SHA.
-   Übergibt sostd an den entsprechenden SHA.

 

 




