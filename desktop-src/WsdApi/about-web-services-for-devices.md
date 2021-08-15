---
description: Web Service on Devices API (WSDAPI) ist eine Implementierung des Geräteprofils für Webdienste (DPWS) für Windows Vista und Windows Server 2008.
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: Informationen zu Webdiensten auf Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7facef3bfed004a834e151db0c58c83a1576e515ed89fa0d690813bc4c18bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552513"
---
# <a name="about-web-services-on-devices"></a>Informationen zu Webdiensten auf Geräten

Die Web Service on Devices-API (WSDAPI) ist eine Implementierung des Geräteprofils für [Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) für Windows Vista und Windows Server 2008. Das DPWS schränkt Webdienstspezifikationen ein, damit Clients Geräte leicht erkennen können. Sobald ein Gerät gefunden wurde, kann ein Client eine Beschreibung der auf diesem Gerät gehosteten Dienste abrufen und diese Dienste verwenden.

## <a name="devices-and-services"></a>Geräte und Dienste

*Geräte* sind Komponenten, in der Regel Hardware, die an das Netzwerk angeschlossen sind. Beispiele hierfür sind Drucker, Webkameras und Videosysteme.

Geräte können null oder mehr Dienste *enthalten.* Ein Videogerät kann beispielsweise Dienste enthalten, die Ein- und Ausschalten, Wiedergabesteuerung, Medienauswerfen und Videostreaming unterstützen. Die Wiedergabesteuerung unterstützt möglicherweise Aktionen wie Wiedergabe, Pause, Zurücksenden und schnelles Vorwärts.

## <a name="discovering-and-manipulating-a-device"></a>Entdecken und Bearbeiten eines Geräts

WSDAPI erweitert das lokale Plug & Play, indem einem Client ermöglicht wird, ein Remotegerät und die zugehörigen Dienste über ein Netzwerk zu finden und darauf zu zugreifen. Er unterstützt ermittlungsbasiertes, one-way- und two-way-Control-Messaging sowie Ereignisse.

![Diagramm, das zeigt, wie WSDAPI es einem Client ermöglicht, ein Remotegerät zu finden und darauf zu zugreifen.](images/overview01.png)

DPWS-Geräte kündigen ihre Präsenz an und machen Dienste (sofern verfügbar) mit einer eindeutigen Adresse und einem standardisierten Satz von XML-Nachrichten verfügbar. DPWS-Clients können den Ermittlungsprozess verwenden, um das Gerät zu finden, seine Dienste aufzählen und eine Verbindung mit diesen Diensten herstellen, um bestimmte Aktionen durchzuführen.

Ein WSDAPI-Client fragt zuerst das Gerät nach vollständigen Beschreibungen seiner Dienste ab, einschließlich der Diensttypen (z. B. druckerdiensttyp oder Scannerdiensttyp). Der Client steuert dann das Gerät durch Aufrufen von Befehlen, die durch einen Diensttyp definiert sind (z. B. durch Aufrufen von **CreatePrintJob** auf einem Gerät mit einem Druckerdiensttyp). Optional kann der Client auch Zustandsänderungen in jedem Dienst überwachen, indem er Ereignisse akribiert, die während der Befehlsausführung auftreten.

![Diagramm, das zeigt, wie ein WSDAPI-Client ein Gerät abfragt und mit ihm interagiert.](images/netdevice01.png)

Weitere Informationen zu Messagingmustern für Geräte finden Sie unter [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).

## <a name="logical-and-physical-addressing"></a>Logische und physische Adressierung

Die logische Adressierung wird verwendet, um Geräte unabhängig von ihren physischen Adressen eindeutig zu identifizieren. WS-Discovery bietet einen Mechanismus zum Auflösen logischer Adressen in physische Adressen, sodass Client-zu-Gerät-Messaging stattfinden kann. Ein Beispiel hierfür ist NAS (Network Attached Storage), den Sie mit sich führen. Wenn Sie über einen Laptop und ein NAS verfügen, sollte Ihr Laptop erkennen können, dass es sich um dasselbe Gerät handelt, unabhängig von der physischen Adresse (IP-Adresse), die der NAS erhält, wenn Sie zwischen Subnetzen wechseln. Hierzu muss das Gerät über eine Identität verfügen, die unabhängig von der ip-Adresse ist, die es erhält. Da herkömmliche Mechanismen wie DNS in einem normalen Roamingszenario nicht verfügbar sind, stellen WS-Addressing und WS-Discovery logische Adressierung und Auflösung als Ad-hoc-Alternative bereit.

Wenn ein Gerät hergestellt wird, erhält es einen global eindeutigen Bezeichner, der als UUID-URI dargestellt wird. Dieser Bezeichner ändert sich für das Gerät nie. Wenn das Gerät eingeschaltet ist, gibt es seine logische Adresse immer über eine WS-Discovery [Hello-Nachricht](hello-message.md) an und akzeptiert Anforderungen zum Konvertieren dieser Adresse in eine physische Adresse (in der Regel HTTP) über WS-Discovery [Resolve-](resolve-message.md) oder [Probe-Nachrichten.](probe-message.md) Nachdem eine gültige physische Adresse (IP-Adresse) erhalten wurde, erfolgt das Messaging über diese Adresse, und WS-Discovery wird nur verwendet, wenn sich die Adresse ändert, der Zustand des Geräts geändert wird und die Clients benachrichtigt werden müssen oder das Gerät offline geschaltet wird.

## <a name="building-applications"></a>Erstellen von Anwendungen

WSDAPI stellt einen generischen DPWS-SOAP-Stapel zur Verwendung durch Client- und Dienstanwendungen zur Verfügung. Der Codegenerator für Webdienste auf Geräten (Web [Services on Devices Code Generator,](web-services-for-devices-code-generator.md) WsdCodeGen.exe) kann verwendet werden, um eine Dienstbeschreibung (WSDL) in Proxy- und Stubcode zu konvertieren, den Anwendungen direkt aufrufen können. Dieser generierte Code transformiert Funktionsaufrufe und Parameter automatisch in SOAP-Nachrichten und XML-Felder und ruft dann in WSDAPI auf, um Anforderungen an das Remotegerät oder den Remoteclient ausausgaben zu können.

Die Funktionsermittlung kann beim Erstellen von WSDAPI-Anwendungen verwendet werden, um von PnP zurückgegebene Funktionsinstanzen zu erstellen und zu aktivieren. Diese Funktionsinstanzen enthalten Daten, die verwendet werden können, um mehr Informationen über die PnP-APIs zu erhalten, wenn mehr als nur eine einfache Ermittlung erforderlich ist. Weitere Informationen finden Sie unter [Funktionsermittlung](/previous-versions/windows/desktop/fundisc/fd-portal) und [PnP-X.](/previous-versions/windows/desktop/fundisc/pnp-x)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlung und Metadaten Exchange Nachrichtenmustern](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[WSDAPI-Spezifikationskonformität](wsdapi-specification-compliance.md)
</dt> <dt>

[Übersicht über die WSDAPI-Schnittstellen](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 
