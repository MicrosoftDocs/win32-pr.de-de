---
description: Die Web Services on Devices-API (WSDAPI) wird verwendet, um Client Anwendungen zu entwickeln, die Geräte suchen und darauf zugreifen, sowie um Geräte Hosts und zugehörige Dienste zu entwickeln, die unter Windows Vista und Windows Server 2008 ausgeführt werden.
ms.assetid: 2b23d7d3-3b06-48c8-993e-49c72b139624
title: Übersicht über die WSDAPI-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3e728971741f97707c1dc72effdaf0ca17dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354626"
---
# <a name="overview-of-the-wsdapi-interfaces"></a>Übersicht über die WSDAPI-Schnittstellen

Die Web Services on Devices-API (WSDAPI) wird verwendet, um Client Anwendungen zu entwickeln, die Geräte suchen und darauf zugreifen, sowie um Geräte Hosts und zugehörige Dienste zu entwickeln, die unter Windows Vista und Windows Server 2008 ausgeführt werden. Die [funktionsermittlungs](/previous-versions/windows/desktop/fundisc/fd-portal) -API und das [wsdcodegen](web-services-for-devices-code-generator.md) -Tool sind ergänzende Tools, die für die Client-, Geräte Host-und Dienst Entwicklung verwendet werden können. Die WSDAPI-Schnittstellen können direkt verwendet werden, um erweiterte Funktionen verfügbar zu machen.

## <a name="major-wsdapi-interfaces"></a>Wichtige WSDAPI-Schnittstellen

Die vier wichtigsten WSDAPI-Schnittstellen sind [**iwsdiscoveryprovider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider), [**iwsdiscoverypublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher), [**iwsddeviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)und [**iwsddevicehost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost). Eine Liste aller WSDAPI-Schnittstellen finden Sie unter [Webdienste auf Geräteschnittstellen](web-services-for-devices-interfaces.md).

## <a name="iwsdiscoveryprovider"></a>Iwsdiscoveryprovider

[**Iwsdiscoveryprovider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) wird zur Implementierung WS-Discovery Funktionen auf Clients verwendet.

[**Iwsdiscoveryprovider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) gibt WS-Discovery Test- [und Auflösungs](resolve-message.md) Meldungen [aus und empfängt](probe-message.md) die Nachrichten [Hello](hello-message.md), [Bye](bye-message.md), [Probe Matches](probematches-message.md)und [resolvematches](resolvematches-message.md) . Verwenden Sie die Informationen, die über die **iwsdiscoveryprovider** -Schnittstelle abgerufen werden, wenn Sie eine [**iwsddeviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) -Schnittstelle erstellen, mit der ein bestimmtes DPWS-Gerät beschrieben und gesteuert

Eine [**iwsdiscoveryprovider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) -Schnittstelle ist nicht erforderlich, wenn Sie eine bestimmte DPWS-Geräteadresse vor dem Erstellen eines Geräte Proxys auflösen. Bei Bedarf wird die Geräteadresse von [**wsdkreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) automatisch aufgelöst.

Die [funktionsermittlungs](/previous-versions/windows/desktop/fundisc/fd-portal) -API kann für die generische Geräte-und Dienst Ermittlung verwendet werden, da die API DPWS-Geräte ermitteln kann, und auch Geräte, die andere Protokolle verwenden. Verwenden Sie die Funktions Ermittlung, wenn Sie eine generische Ermittlungs Anwendung schreiben.

## <a name="iwsdiscoverypublisher"></a>Iwsdiscoverypublisher

[**Iwsdiscoverypublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) wird verwendet, um WS-Discovery Funktionen für Ziel Dienste wie z. b. Geräte zu implementieren.

[**Iwsdiscoverypublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) ermöglicht es einer Anwendung, ihre Anwesenheit mithilfe WS-Discovery Hello-und bye-Nachrichten zu veröffentlichen. Diese Schnittstelle ermöglicht einer Anwendung das Empfangen von Test-und Auflösungsanforderungen sowie das Erstellen und Senden von Probe Matches-und resolvematches-Antworten.

Eine [**iwsdiscoverypublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) -Schnittstelle ist nicht erforderlich, wenn das vorhanden sein eines [**iwsddevicehost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) -Objekts einfach veröffentlicht wird. **Iwsddevicehost** verwaltet seine eigene WS-Discovery Anwesenheit.

## <a name="iwsddeviceproxy"></a>Iwsddeviceproxy

Mithilfe von [**iwsddeviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) werden Client seitige WS-Discovery-, WS-MetadataExchange-und Steuerungsfunktionen implementiert. Diese Funktion umfasst optionale Funktionen für sicheres Channel, WS-Ereignis und Anlage.

Die [**iwsddeviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) -Schnittstelle verfügt über die folgenden drei Verwendungsmöglichkeiten.

-   Löst bei Bedarf logische Geräte Adressen auf.
-   Initiiert Metadatenanforderungen an Geräte, um die Typen und Adressen der Dienste aufzuzählen.
-   Stellt eine Quelle für [**iwsdserviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) -Objekte bereit, die verwendet werden können, um Steuerungs Meldungen an bestimmte Dienste auf einem Gerät auszugeben.

Das [**iwsddeviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) -Objekt wird in der Regel erstellt und vollständig in Code verwendet, der von [wsdcodegen](web-services-for-devices-code-generator.md)generiert wurde.

## <a name="iwsddevicehost"></a>Iwsddevicehost

Mithilfe von [**iwsddevicehost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) werden Geräte seitige WS-Discovery-, WS-MetadataExchange-und diensthostingfunktionen implementiert. Gehostete Dienste reagieren möglicherweise auf Steuerungs Meldungen und unterstützen möglicherweise die Funktionen "sicherer Kanal", "WS-Ereignis" und "Anlage".

Die [**iwsddevicehost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) -Schnittstelle verfügt über die folgenden Verwendungsmöglichkeiten.

-   Hostet Dienst Objekte.
-   Gibt an, dass ein Geräte Host im Netzwerk mithilfe von WS-Discovery vorhanden ist.
-   Reagiert auf WS-MetadataExchange Anforderungen und beschreibt die Typen und Speicherorte gehosteter Dienste.
-   Sendet Netzwerk Anforderungen an Dienst Objekte.

Die Funktionen WS-Discovery, WS-MetadataExchange und WS-Eventing-Abonnement Verwaltung werden vollständig innerhalb des Geräte Host Objekts behandelt. Bevor ein Dienst innerhalb eines Geräte Hosts gehostet werden kann, müssen die folgenden Anforderungen erfüllt sein.

-   Der Host muss durch Aufrufen von [**wsdcreatedevicehost**](/windows/desktop/api/WsdHost/nf-wsdhost-wsdcreatedevicehost)erstellt werden.
-   Die dem Dienst zugeordneten Metadaten müssen registriert werden.
-   Der Dienst selbst muss registriert werden.
-   Der Geräte Host muss gestartet werden.

Das [**iwsddevicehost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) -Objekt wird in der Regel im von [wsdcodegen](web-services-for-devices-code-generator.md)generierten Code erstellt und verwendet.

 

 
