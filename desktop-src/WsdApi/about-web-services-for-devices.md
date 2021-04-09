---
description: Die Web Service on Devices-API (WSDAPI) ist eine Implementierung des Geräte Profils für Webdienste (DPWS) für Windows Vista und Windows Server 2008.
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: Informationen zu Webdiensten auf Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca7f7dc97dabd3dde7af12f3cece992b4f0ef6d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "103869400"
---
# <a name="about-web-services-on-devices"></a>Informationen zu Webdiensten auf Geräten

Die Web Service on Devices-API (WSDAPI) ist eine Implementierung des [Geräte Profils für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) für Windows Vista und Windows Server 2008. Die DPWS schränkt Webdienst Spezifikationen ein, damit Clients problemlos Geräte ermitteln können. Nachdem ein Gerät erkannt wurde, kann ein Client eine Beschreibung der auf diesem Gerät gehosteten Dienste abrufen und diese Dienste verwenden.

## <a name="devices-and-services"></a>Geräte und Dienste

*Geräte* sind Komponenten, normalerweise Hardware, die mit dem Netzwerk verbunden sind. Beispiele hierfür sind Drucker, Webkameras und Videosysteme.

Geräte können NULL oder mehr *Dienste* enthalten. Ein Videogerät kann z. b. Dienste enthalten, die das Einschalten und deaktivieren, das Abspielen von Steuerelementen, das Steuern von Medien und das Video Streaming unterstützen. Die Wiedergabe Steuerung unterstützt möglicherweise Aktionen wie "Wiedergabe", "anhalten", "Zurückspulen" und "schneller

## <a name="discovering-and-manipulating-a-device"></a>Entdecken und Bearbeiten eines Geräts

WSDAPI erweitert das lokale Plug & Play Modell, indem es einem Client ermöglicht, ein Remote Gerät und seine zugeordneten Dienste über ein Netzwerk zu ermitteln und darauf zuzugreifen. Es unterstützt Ermittlung, unidirektionales und bidirektionales Steuerungs Messaging und Ereignisse.

![Diagramm, das zeigt, wie WSDAPI einem Client das ermitteln und Zugreifen auf ein Remote Gerät ermöglicht.](images/overview01.png)

DPWS-Geräte kündigen ihre Anwesenheits-und Bereitstellungs Dienste (sofern vorhanden) mit einer eindeutigen Adresse und einem standardisierten Satz von XML-Nachrichten an. DPWS-Clients können den Ermittlungsprozess zum Suchen des Geräts, zum Auflisten der zugehörigen Dienste und zum Herstellen einer Verbindung mit diesen Diensten verwenden, um bestimmte Aktionen auszuführen.

Ein WSDAPI-Client fragt zuerst das Gerät nach umfassenden Beschreibungen seiner Dienste ab, einschließlich der Dienst Typen (z. b. eines Drucker Dienst Typs oder eines Scanner-Dienst Typs). Der Client steuert dann das Gerät durch Aufrufen von Befehlen, die von einem Diensttyp definiert werden (z. b. durch Aufrufen von **createprintjob** auf einem Gerät mit einem druckerdiensttyp). Optional kann der Client auch Zustandsänderungen in jedem Dienst überwachen, indem er Ereignisse abonniert, die während der Befehlsausführung auftreten.

![Diagramm, das zeigt, wie ein WSDAPI-Client ein Gerät abfragt und mit ihm interagiert.](images/netdevice01.png)

Weitere Informationen zu Geräte Messaging Mustern finden Sie unter Ermittlungs [-und Metadatenaustausch-Nachrichten Muster](discovery-and-metadata-exchange-message-patterns.md).

## <a name="logical-and-physical-addressing"></a>Logische und physische Adressierung

Mithilfe der logischen Adressierung werden Geräte unabhängig von ihren physischen Adressen eindeutig identifiziert. WS-Discovery bietet einen Mechanismus, um logische Adressen in physische Adressen aufzulösen, sodass Client-zu-Gerät-Messaging erfolgen kann. Ein Beispiel hierfür ist Network Attached Storage (NAS), den Sie mit Ihnen ausführen. Wenn Sie einen Laptop und NAS haben, sollte Ihr Laptop erkennen können, dass es sich um das gleiche Gerät handelt, unabhängig von der physischen Adresse (IP-Adresse), die der NAS beim Wechsel zwischen Subnetzen erhält. Um dies zu erreichen, muss das Gerät über eine Identität verfügen, die unabhängig von der abbenötigten IP-Adresse ist. Da herkömmliche Mechanismen wie DNS nicht in einem normalen Roamingszenario verfügbar sind, bieten WS-Addressing und WS-Discovery die logische Adressierung und Lösung als eine Ad-hoc-Alternative.

Wenn ein Gerät hergestellt wird, erhält es eine Globally Unique Identifier, die als UUID-URI dargestellt wird. Dieser Bezeichner ändert sich nie für das Gerät. Wenn das Gerät eingeschaltet ist, kündigt es stets seine logische Adresse über eine WS-Discovery [Hello](hello-message.md) -Nachricht an und akzeptiert Anforderungen, die in eine physische Adresse (i. d. h. http) über WS-Discovery [Auflösen](resolve-message.md) [oder über](probe-message.md) prüfen von Nachrichten konvertiert werden. Sobald eine gültige physische Adresse (IP-Adresse) abgerufen wurde, erfolgt das gesamte Messaging über diese Adresse. WS-Discovery wird nur verwendet, wenn sich die Adresse ändert, der Zustand des Geräts geändert wird und die Clients benachrichtigt werden müssen oder wenn das Gerät offline geschaltet wird.

## <a name="building-applications"></a>Erstellen von Anwendungen

WSDAPI bietet einen generischen DPWS-SOAP-Stapel für die Verwendung durch Client-und Dienst Anwendungen. Der [Code-Generator für die Webdienste auf Geräten](web-services-for-devices-code-generator.md) (WsdCodeGen.exe) kann verwendet werden, um eine Dienst Beschreibung (WSDL) in Proxy-und Stub-Code zu konvertieren, der von Anwendungen direkt aufgerufen werden kann. Dieser generierte Code transformiert automatisch Funktionsaufrufe und Parameter in SOAP-Nachrichten und XML-Felder und ruft dann WSDAPI auf, um Anforderungen an das Remote Gerät oder den Client auszugeben.

Die Funktions Ermittlung kann beim Erstellen von WSDAPI-Anwendungen zum Erstellen und Aktivieren von Funktions Instanzen verwendet werden, die von PNP zurückgegeben werden. Diese Funktions Instanzen enthalten Daten, die verwendet werden können, um weitere Informationen über die PNP-APIs zu erhalten, wenn mehr als nur eine einfache Ermittlung erforderlich ist. Weitere Informationen finden Sie unter [Funktions](/previous-versions/windows/desktop/fundisc/fd-portal) Ermittlung und [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs-und Metadatenaustausch-Nachrichten Muster](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[WSDAPI-Spezifikation Konformität](wsdapi-specification-compliance.md)
</dt> <dt>

[Übersicht über die WSDAPI-Schnittstellen](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 
