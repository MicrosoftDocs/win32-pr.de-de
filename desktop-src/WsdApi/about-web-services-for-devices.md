---
description: Web Service on Devices API (WSDAPI) ist eine Implementierung des Geräteprofils für Webdienste (Devices Profile for Web Services, DPWS) für Windows Vista und Windows Server 2008.
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

Web Service on Devices API (WSDAPI) ist eine Implementierung des [Geräteprofils für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (Devices Profile for Web Services, DPWS) für Windows Vista und Windows Server 2008. DpWS schränkt Webdienstspezifikationen ein, damit Clients Geräte leicht ermitteln können. Sobald ein Gerät ermittelt wurde, kann ein Client eine Beschreibung der auf diesem Gerät gehosteten Dienste abrufen und diese Dienste verwenden.

## <a name="devices-and-services"></a>Geräte und Dienste

*Geräte* sind Komponenten, in der Regel Hardware, die an das Netzwerk angefügt sind. Beispiele hierfür sind Drucker, Webkameras und Videosysteme.

Geräte können null oder mehr *Dienste* enthalten. Beispielsweise kann ein Videogerät Dienste enthalten, die Ein- und Ausschalten, Wiedergabesteuerung, Medienauswahl und Videostreaming unterstützen. Die Wiedergabesteuerung kann Aktionen wie Wiedergabe, Pause, Zurückspulen und schnelles Vorwärtsschalten unterstützen.

## <a name="discovering-and-manipulating-a-device"></a>Ermitteln und Bearbeiten eines Geräts

WSDAPI erweitert das lokale Plug & Play Modell, indem es einem Client ermöglicht wird, ein Remotegerät und die zugehörigen Dienste über ein Netzwerk zu ermitteln und darauf zuzugreifen. Sie unterstützt die Ermittlung, das ein- und zweiseitige Steuerungsmessaging und das Ereignis.

![Diagramm, das zeigt, wie ein Client mit WSDAPI ein Remotegerät ermitteln und darauf zugreifen kann](images/overview01.png)

DPWS-Geräte kündigen ihre Präsenz an und machen Dienste (falls vorhanden) mit einer eindeutigen Adresse und einem standardisierten Satz von XML-Nachrichten verfügbar. DPWS-Clients können den Ermittlungsprozess verwenden, um das Gerät zu suchen, seine Dienste aufzuzählen und eine Verbindung mit diesen Diensten herzustellen, um bestimmte Aktionen auszuführen.

Ein WSDAPI-Client fragt zuerst das Gerät nach vollständigen Beschreibungen seiner Dienste ab, einschließlich der Diensttypen (z. B. eines Druckerdiensttyps oder eines Scannerdiensttyps). Der Client steuert dann das Gerät, indem er Befehle aufruft, die durch einen Diensttyp definiert sind (z. B. durch Aufrufen von **CreatePrintJob** auf einem Gerät mit einem Druckerdiensttyp). Optional kann der Client auch Zustandsänderungen in jedem Dienst überwachen, indem er Ereignisse abonniert, die während der Befehlsausführung auftreten.

![Diagramm, das zeigt, wie ein WSDAPI-Client ein Gerät abfragt und mit diesem interagiert](images/netdevice01.png)

Weitere Informationen zu Gerätemessagingmustern finden Sie unter [Ermittlung und Metadaten Exchange Nachrichtenmuster.](discovery-and-metadata-exchange-message-patterns.md)

## <a name="logical-and-physical-addressing"></a>Logische und physische Adressierung

Die logische Adressierung wird verwendet, um Geräte unabhängig von ihren physischen Adressen eindeutig zu identifizieren. WS-Discovery bietet einen Mechanismus zum Auflösen logischer Adressen in physische Adressen, sodass Client-zu-Gerät-Messaging erfolgen kann. Ein Beispiel hierfür ist nas (Network Attached Storage), den Sie bei sich tragen. Wenn Sie über einen Laptop und ein NAS verfügen, sollte Ihr Laptop erkennen können, dass es sich um dasselbe Gerät handelt, unabhängig von der physischen Adresse (IP-Adresse), die der NAS beim Verschieben zwischen Subnetzen erhält. Um dies zu erreichen, muss das Gerät über eine Identität verfügen, die von der ip-Adresse unabhängig ist, die es erhält. Da herkömmliche Mechanismen wie DNS in einem normalen Roamingszenario nicht verfügbar sind, bieten WS-Addressing und WS-Discovery eine logische Adressierung und Auflösung als Ad-hoc-Alternative.

Wenn ein Gerät hergestellt wird, erhält es einen global eindeutigen Bezeichner, der als UUID-URI dargestellt wird. Dieser Bezeichner wird für das Gerät nie geändert. Wenn das Gerät eingeschaltet ist, kündigt es seine logische Adresse immer über eine WS-Discovery [Hello-Nachricht](hello-message.md) an und akzeptiert Anforderungen, diese über WS-Discovery [Resolve-](resolve-message.md) oder [Probe-Nachrichten](probe-message.md) in eine physische Adresse (in der Regel HTTP) zu konvertieren. Sobald eine gültige physische Adresse (IP-Adresse) abgerufen wurde, erfolgt das gesamte Messaging über diese Adresse, und WS-Discovery wird nur verwendet, wenn sich die Adresse ändert, sich der Zustand des Geräts ändert und die Clients benachrichtigt werden müssen oder das Gerät offline geschaltet wird.

## <a name="building-applications"></a>Erstellen von Anwendungen

WSDAPI stellt einen generischen DPWS-SOAP-Stapel für die Verwendung durch Client- und Dienstanwendungen bereit. Der [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md) (WsdCodeGen.exe) kann verwendet werden, um eine Dienstbeschreibung (WSDL) in Proxy- und Stubcode zu konvertieren, den Anwendungen direkt aufrufen können. Dieser generierte Code transformiert Funktionsaufrufe und Parameter automatisch in SOAP-Nachrichten und XML-Felder und ruft dann WSDAPI auf, um Anforderungen an das Remotegerät oder den Client auszugeben.

Die Funktionsermittlung kann beim Erstellen von WSDAPI-Anwendungen verwendet werden, um funktionsinstanzen zu erstellen und zu aktivieren, die von PnP zurückgegeben werden. Diese Funktionsinstanzen enthalten Daten, die verwendet werden können, um mehr Informationen über die PnP-APIs abzurufen, wenn mehr als nur eine einfache Ermittlung erforderlich ist. Weitere Informationen finden Sie unter [Funktionsermittlung](/previous-versions/windows/desktop/fundisc/fd-portal) und [PnP-X.](/previous-versions/windows/desktop/fundisc/pnp-x)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs- und Metadaten-Exchange Nachrichtenmuster](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[WSDAPI-Spezifikationskonformität](wsdapi-specification-compliance.md)
</dt> <dt>

[Übersicht über die WSDAPI-Schnittstellen](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 
