---
description: Listet die Diagnoseverfahren auf, die bei der Problembehandlung von WSDAPI-Anwendungen verwendet werden
ms.assetid: befe4234-8d3a-4fc5-9a7d-faca94964af6
title: Problembehandlung bei anderen WSDAPI-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a421f26237cc14d07a43e00faeb6d8bf49aa02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354560"
---
# <a name="troubleshooting-other-wsdapi-applications"></a>Problembehandlung bei anderen WSDAPI-Anwendungen

Anwendungen können WSDAPI-Schnittstellen und-Funktionen direkt zum Durchführen von Ermittlungs-und metadatenaustauschen von Geräten abrufen. Die von diesen Anwendungen verwendeten Nachrichten Muster variieren.

Das Ziel dieses Handbuch zur Problembehandlung besteht darin, dass WSDAPI-Anwendungsentwickler einen Geräte Proxy erfolgreich implementieren können. Dieses Handbuch soll nicht bei der Problembehandlung für alle Aspekte von WSDAPI helfen. Wenn der Geräte Proxy erfolgreich erstellt wurde und der Client und der Host sich im Netzwerk gegenseitig sehen können, kann dieses Handbuch die Probleme der Anwendung nicht beheben. Befolgen Sie die Anweisungen unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md) -Ablauf Verfolgung, und wenden Sie sich an den Microsoft Support, um weitere Unterstützung zu erhalten.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxy"></a>Problembehandlung bei Clients, die wsdcreatedeviceproxy aufrufen

Anwendungen rufen [**wsdkreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) auf, um eine Instanz der [**iwsddeviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) -Schnittstelle zu erstellen und zu initialisieren. Mit diesem Geräte Proxy Objekt können Dienste auf einem Gerät und Exchange-Metadaten angekündigt werden.

Eine Anwendung, die [**wsdcreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) aufrufen, verwendet immer die folgenden Meldungen.

-   [Get](get--metadata-exchange--http-request-and-message.md)
-   [GetResponse](getresponse--metadata-exchange--message.md)

Eine Anwendung, die [**wsdcreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) aufrufen, verwendet manchmal die folgenden Meldungen.

-   [Beheben](resolve-message.md)
-   [Resolvematches](resolvematches-message.md)

[Auflösungs](resolve-message.md) -und [resolvematches](resolvematches-message.md) -Nachrichten werden generiert, wenn eine logische Geräteadresse (d. h. eine Geräteadresse der Form "urn: uuid: {GUID}") an *pszdeviceid* übergeben wird. Diese Nachrichten werden nicht generiert, wenn eine physische Geräteadresse an *pszdeviceid* übergeben wird. Wenn Auflösungs-und resolvematches-Nachrichten verwendet werden, werden Sie vor den [Get](get--metadata-exchange--http-request-and-message.md) -und [GetResponse](getresponse--metadata-exchange--message.md) -Nachrichten gesendet.

Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit einer Anwendung zu identifizieren, die [**wsdcreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) mit einer physischen Geräteadresse anruft.

1.  Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).
2.  [Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)

Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit einer Anwendung zu identifizieren, die [**wsdcreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) mit einer logischen Geräteadresse anruft.

1.  Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).
2.  [Verwenden Sie einen generischen Host und Client für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Überprüfen Sie Multicast Datenverkehr mithilfe des WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Überprüfen Sie die Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)

Vergewissern Sie sich, dass die Nachrichten [Auflösen](resolve-message.md) und [resolvematches](resolvematches-message.md) generiert werden und die Datenverkehrs Anforderungen erfüllen. Es ist nicht erforderlich, in der WSD-debugclientausgabe oder in den Netzwerk Ablauf [Verfolgungen nach Test-oder](probe-message.md) [Probe Matches](probematches-message.md) -Meldungen zu suchen.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxyadvanced"></a>Problembehandlung bei Clients, die wsdcreatedeviceproxyadvanced aufrufen

Anwendungen rufen [**wsdkreatedeviceproxyadvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) auf, um eine Instanz der [**iwsddeviceproxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) -Schnittstelle zu erstellen und zu initialisieren. Anders als bei [**wsdkreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)verfügt **wsdkreatedeviceproxyadvanced** über einen *pdeviceaddress* -Parameter, der zum Definieren der Transport Adresse des Geräts verwendet wird. Wenn diese Transport Adresse angegeben wird, ist die Auflösung logischer Adressen nicht erforderlich, und die Nachrichten von [Resolve](resolve-message.md) und [resolvematches](resolvematches-message.md) werden nicht generiert.

Wenn *pdeviceaddress* auf **null** festgelegt ist und *pszdeviceid* eine logische Adresse ist, dann ist die Adress Auflösung erforderlich, und [Auflösungs-und](resolve-message.md) [resolvematches](resolvematches-message.md) -Meldungen werden generiert.

Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit einer Anwendung zu identifizieren, die [**wsdcreatedeviceproxyadvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) mit einem _pdeviceaddress_ -Parameter ungleich **null** aufrufen. Diese Prozeduren können auch verwendet werden, wenn *pdeviceaddress* **null** und *pszdeviceid* eine physische Adresse ist.

1.  Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).
2.  [Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)

Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit einer Anwendung zu identifizieren, die [**wsdcreatedeviceproxyadvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) aufrufen, wobei *pdeviceaddress* auf **null** festgelegt ist und *pszdeviceid* auf eine logische Adresse festgelegt ist.

1.  Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).
2.  [Verwenden Sie einen generischen Host und Client für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Überprüfen Sie Multicast Datenverkehr mithilfe des WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Überprüfen Sie die Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)

Vergewissern Sie sich, dass die Nachrichten [Auflösen](resolve-message.md) und [resolvematches](resolvematches-message.md) generiert werden und die Datenverkehrs Anforderungen erfüllen. Es ist nicht erforderlich, in der WSD-debugclientausgabe oder in den Netzwerk Ablauf [Verfolgungen nach Test-oder](probe-message.md) [Probe Matches](probematches-message.md) -Meldungen zu suchen.

## <a name="troubleshooting-clients-using-the-iwsdiscoveryprovider-interface"></a>Problembehandlung bei Clients mit der iwsdiscoveryprovider-Schnittstelle

Anwendungen, die die [**iwsdiscoveryprovider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) -Schnittstelle aufrufen, führen keinen Metadatenaustausch durch. Diese Schnittstelle wird nur für die Ermittlung verwendet. Die Nachrichten Muster und Problem Behandlungs Prozeduren unterscheiden sich für jede Methode, die in der **iwsdiscoveryprovider** -Schnittstelle aufgerufen wird

Wenn eine Anwendung [**iwsdiscoveryprovider:: searchbytype**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype)aufruft, wird eine [Testnachricht generiert](probe-message.md) . Die Testnachricht wird von UDP-Multicast an Port 3702 gesendet. Eine [Probe Matches](probematches-message.md) -Meldung wird als Antwort generiert. Die Probe Matches-Nachricht wird von UDP Unicast gesendet und stammt von Port 3702.

Wenn eine Anwendung [**iwsdiscoveryprovider:: searchbyid**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid)aufruft, wird eine [Resolve](resolve-message.md) -Nachricht generiert. Eine Auflösungs Meldung wird von UDP-Multicast an Port 3702 gesendet. Eine [resolvematches](resolvematches-message.md) -Nachricht wird als Antwort generiert. Die resolvematches werden von UDP Unicast gesendet und stammen von Port 3702.

Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit einer Anwendung zu identifizieren, die [**iwsdiscoveryprovider:: searchbytype**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) oder [**iwsdiscoveryprovider:: searchbyid**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid)aufrufen. Überprüfen Sie, ob die von der aufgerufenen API generierten Nachrichten die Datenverkehrs Anforderungen erfüllen.

1.  Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).
2.  [Verwenden Sie einen generischen Host und Client für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Überprüfen Sie Multicast Datenverkehr mithilfe des WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Überprüfen Sie die Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).

Wenn eine Anwendung [**iwsdiscoveryprovider:: searchbyaddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress)aufruft, handelt es sich um eine gesteuerte Ermittlungs Anwendung. Weitere Informationen zur Problembehandlung finden [Sie unter Problembehandlung bei Anwendungen mithilfe der gesteuerten](troubleshooting-applications-using-directed-discovery.md)Ermittlung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



