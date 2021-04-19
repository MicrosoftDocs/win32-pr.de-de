---
description: Wenn sich der generische Host und der Client im Netzwerk sehen können, der tatsächliche Host und der Client jedoch nicht, liegt das Problem wahrscheinlich in den Nachrichten, die zwischen den Endpunkten über das Netzwerk gesendet werden.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Verwenden des WSD-Debugclients zum Überprüfen des Multicastdatenverkehrs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a814ac97512ef4b0691c22d3238d151372023a7
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380664"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a>Verwenden des WSD-Debugclients zum Überprüfen des Multicastdatenverkehrs

Wenn sich der generische Host und der Client im Netzwerk sehen können, der tatsächliche Host und der Client jedoch nicht, liegt das Problem wahrscheinlich in den Nachrichten, die zwischen den Endpunkten über das Netzwerk gesendet werden. Weitere Informationen zum generischen Host und Client finden Sie unter [Verwenden eines generischen Hosts und Clients für die UDP-WS-Ermittlung.](using-a-generic-host-and-client-for-udp-ws-discovery.md) Da vollständige Netzwerkablaufverfolgungen schwierig zu erfassen, zu filtern und zu lesen sind, kann das WSD-Debugclienttool zum Drucken der Multicastseiten WS-Discovery Nachrichten verwendet werden.

Der WSD-Debugclient im Multicastmodus kann nur die Hälfte der Nachrichten überprüfen, da der Client keine Unicastnachrichten drucken kann. Wenn Unicastdatenverkehr von Interesse ist, fahren Sie direkt mit [Inspecting Network Traces for UDP WS-Discovery (Untersuchen von Netzwerkablaufverfolgungen für die UDP-WS-Ermittlung)](inspecting-network-traces-for-udp-ws-discovery.md)über.

Dieses Verfahren zeigt eine Methode, die den gesamten Multicastdatenverkehr im Netzwerk anzeigt. Informationen zum Anzeigen von Multicastdatenverkehr zum und vom Gerät finden Sie weiter unten im Abschnitt Filtern von [WSD-Debugclientergebnissen.](#filtering-wsd-debug-client-results)

**So verwenden Sie den WSD-Debugclient zum Überprüfen des Multicastdatenverkehrs**

1.  Konfigurieren Sie den Host und den Client so, dass sie über das Netzwerk ausgeführt werden .(Stellen Sie also sicher, dass der Host und der Client auf verschiedenen Computern ausgeführt werden.)
2.  Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **WSDDebug \_client.exe /mode multicast**
3.  Reproduzieren Sie den Fehler, indem Sie host und client starten oder F5 im Netzwerk-Explorer drücken.
4.  Überprüfen Sie, ob Nachrichten multicastiert werden.

Wenn die erforderlichen Nachrichten in der Ausgabe des WSD-Debugclients angezeigt werden, kann sich der Anwendungsfehler im Inhalt der Multicastnachricht oder im Vorhandensein oder Inhalt der entsprechenden Unicastantwortnachrichten befinden. Fahren Sie mit der Problembehandlung fort, indem Sie die Anweisungen unter [Überprüfen von Netzwerkablaufverfolgungen für die UDP-WS-Ermittlung](inspecting-network-traces-for-udp-ws-discovery.md)befolgen.

Wenn die erforderlichen Meldungen in der Ausgabe des WSD-Debugclients angezeigt werden, ist es wahrscheinlich, dass die Quelle des Anwendungsproblems identifiziert wurde. Es ist wahrscheinlich, dass der Multicastdatenverkehr nicht im Netzwerk übertragen wird. Dieser Fehler kann passieren, wenn die Anwendung Multicastadapter nicht ordnungsgemäß aufzählt. Anwendungen müssen explizit Multicastdatenverkehr über alle Netzwerkschnittstellen senden. Andernfalls werden pakete möglicherweise nicht für die Loopbackschnittstelle oder für andere Schnittstellen generiert. Um sicherzustellen, dass die Pakete nicht im Netzwerk angezeigt werden, befolgen Sie die Anweisungen unter Überprüfen von Netzwerkverfolgungen für [die UDP-WS-Ermittlung,](inspecting-network-traces-for-udp-ws-discovery.md) und suchen Sie nach Beweisen für fehlende Multicastnachrichten.

## <a name="verifying-that-messages-are-being-multicast"></a>Überprüfen, ob Nachrichten Multicast verwenden

Vergewissern Sie sich [immer, dass](probe-message.md) Testnachrichten multicastt werden. Überprüfen Sie optional, ob [Hello-](hello-message.md) und [Resolve-Nachrichten](resolve-message.md) multicast sind. Beachten Sie, dass nicht alle Anwendungen Nachrichten auflösen verwenden. Weitere Informationen zu Nachrichtenmustern, die von Clients und Hosts verwendet werden, finden Sie unter Discovery [and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and Erste Schritte with [WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).

Nachrichten müssen ausgelöst werden, um wie in Schritt 3 oben beschrieben gesendet zu werden. Der WSD-Debugclient zeigt die unformatierte SOAP-Nachricht als Ausgabe an. Da alle vom WSD-Debugclient im Multicastmodus gedruckten Nachrichten über einen Multicastsocket empfangen werden, wird die Nachrichtenzieladresse nicht angezeigt.

Die folgende Beispielausgabe des WSD-Debugclients zeigt eine Testmeldung. Das \<wsa:Action> -Element identifiziert die Nachricht als Testnachricht. Überprüfen Sie das \<wsa:Action> Feld, um sicherzustellen, dass die empfangene Nachricht eine Testnachricht war.

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

Die folgende Beispielausgabe des WSD-Debugclients zeigt eine Hello-Meldung. Das \<wsa:Action> -Element identifiziert die Nachricht als Hello-Nachricht.

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a>Filtern von WSD-Debugclientergebnissen

Durch Filtern der Ergebnisse des WSD-Debugclients können Incidentdatenverkehr im Zusammenhang mit dem Gerät identifiziert werden. Filterung ist nur in lauten Netzwerken erforderlich.

Es gibt zwei Möglichkeiten, Ergebnisse zu filtern. Die zu filternden IP-Adressen können beim Starten des WSD-Debugclients explizit identifiziert werden. Alternativ können die IP-Adressen angegeben werden, nachdem der Client gestartet wurde. In diesem Abschnitt werden beide Methoden beschrieben.

**So geben Sie ip-Adressen an, die beim Starten des WSD-Debugclients gefiltert werden sollen**

1.  Konfigurieren Sie den Host und den Client so, dass sie über das Netzwerk ausgeführt werden .(Stellen Sie also sicher, dass der Host und der Client auf verschiedenen Computern ausgeführt werden.)
2.  Erfassen Sie die IP-Adressen des Geräts. Wenn das Gerät über mehrere Adressen verfügt (z. B. sowohl IPv4- als auch IPv6-Adressen), müssen alle Adressen gesammelt werden.
3.  Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **WSDDebug \_client.exe /mode multicast /ip add***<device IP>*

*<device IP>* ist eine IP-Adresse. Die folgende Liste enthält einige Beispielformate für diese IP-Adresse.

-   192.168.0.1
-   ::1
-   mydevice.contoso.com

Der WSD-Debugclient löst automatisch hostnames auf, die an der Eingabeaufforderung angegeben werden.

**So filtern Sie ergebnisse nach dem Starten des WSD-Debugclients**

1.  Konfigurieren Sie den Host und den Client so, dass sie über das Netzwerk ausgeführt werden .(Stellen Sie also sicher, dass der Host und der Client auf verschiedenen Computern ausgeführt werden.)
2.  Erfassen Sie die IP-Adressen des Geräts. Wenn das Gerät über mehrere Adressen verfügt (z. B. sowohl IPv4- als auch IPv6-Adressen), müssen alle Adressen gesammelt werden.
3.  Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **WSDDebug \_client.exe /mode multicast**
4.  Führen Sie an der Eingabeaufforderung des WSD-Debugclients den folgenden Befehl aus: **ip add***<device IP>*
5.  Wiederholen Sie Schritt 4, bis alle IP-Adressen des Geräts hinzugefügt wurden.

Beim folgenden Verfahren wird davon ausgegangen, dass der WSD-Debugclient gestartet wurde und eine Filterung nach IP-Adresse erfolgt.

**So überprüfen Sie, ob die richtigen IP-Adressen gefiltert werden**

-   Führen Sie an der Eingabeaufforderung des WSD-Debugclients den folgenden Befehl aus: **ip print**

    Die Liste der ip-Adressen, die gefiltert werden, wird angezeigt.

Beim folgenden Verfahren wird davon ausgegangen, dass der WSD-Debugclient gestartet wurde und eine Filterung nach IP-Adresse erfolgt.

**So deaktivieren Sie die Filterung**

-   Führen Sie an der Eingabeaufforderung des WSD-Debugclients den folgenden Befehl aus: **ip clear**

    Der ganze Multicastdatenverkehr wird nun in der Debugausgabe angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI – Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



