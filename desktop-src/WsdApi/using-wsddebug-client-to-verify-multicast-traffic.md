---
description: Wenn der generische Host und der Client einander im Netzwerk sehen können, der tatsächliche Host und Client jedoch nicht, ist es wahrscheinlich, dass das Problem in den Nachrichten liegt, die zwischen den Endpunkten über das Netzwerk gesendet werden.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Überprüfen von Multicast Datenverkehr mithilfe des WSD-Debugclients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f03e06baefc40bad843a5193b2cec604383251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357786"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a>Überprüfen von Multicast Datenverkehr mithilfe des WSD-Debugclients

Wenn der generische Host und der Client einander im Netzwerk sehen können, der tatsächliche Host und Client jedoch nicht, ist es wahrscheinlich, dass das Problem in den Nachrichten liegt, die zwischen den Endpunkten über das Netzwerk gesendet werden. Weitere Informationen zum generischen Host und Client finden Sie unter [Verwenden eines generischen Hosts und Clients für die UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md). Da es schwierig sein kann, vollständige Netzwerk Ablauf Verfolgungen zu erfassen, zu filtern und zu lesen, kann das WSD-debugclienttool verwendet werden, um die Multicast Seiten WS-Discovery Nachrichten zu drucken.

Der WSD-Debugclient im Multicast Modus kann nur die Hälfte der Nachrichten untersuchen, da der Client keine Unicastnachrichten drucken kann. Wenn der Unicastdatenverkehr von Interesse ist, überprüfen Sie die Untersuchung von Netzwerk Ablauf Verfolgungen [für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md)direkt.

Diese Prozedur zeigt eine Methode, die den gesamten Multicast Datenverkehr im Netzwerk anzeigt. Weitere Informationen zum Anzeigen von Multicast Datenverkehr zum und vom Gerät finden Sie unten im Abschnitt [Filtern von WSD-Debug-Client Ergebnissen](#filtering-wsd-debug-client-results) .

**So verwenden Sie den WSD-Debugclient zum Überprüfen von Multicast Datenverkehr**

1.  Konfigurieren Sie den Host und den Client für die Netzwerk übergreifende Ausführung (d. h., stellen Sie sicher, dass der Host und der Client auf unterschiedlichen Computern ausgeführt werden).
2.  Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **wsddebug \_client.exe/Mode Multicast**
3.  Reproduzieren Sie den Fehler Durchstarten des Hosts und Clients oder durch Drücken von F5 im Netzwerk-Explorer.
4.  Überprüfen Sie, ob die Nachrichten Multicast sind.

Wenn die erforderlichen Meldungen in der WSD-debugclientausgabe angezeigt werden, kann es vorkommen, dass der Anwendungsfehler im Multicast Nachrichten Inhalt oder im vorhanden sein oder Inhalt der entsprechenden unicastantwortnachrichten vorliegt. Führen Sie die Problembehandlung mit den Anweisungen unter Überprüfen von Netzwerk Ablauf Verfolgungen [für UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md)fort

Wenn die erforderlichen Meldungen in der WSD-debugclientausgabe angezeigt werden, ist es wahrscheinlich, dass die Quelle des Anwendungs Problems erkannt wurde. Es ist wahrscheinlich, dass der Multicast-Datenverkehr nicht im Netzwerk übertragen wird. Dieser Fehler kann auftreten, wenn die Anwendung Multicast Adapter nicht ordnungsgemäß aufzählt. Anwendungen müssen Multicast Datenverkehr explizit über alle Netzwerkschnittstellen senden. Andernfalls können Pakete nicht für die Loopback Schnittstelle oder für andere Schnittstellen generiert werden. Um sicherzustellen, dass die Pakete nicht im Netzwerk angezeigt werden, befolgen Sie die Anweisungen unter Überprüfen von Netzwerk Ablauf Verfolgungen [für UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) und suchen nach Beweisen für fehlende Multicast Nachrichten.

## <a name="verifying-that-messages-are-being-multicast"></a>Überprüfen, ob Nachrichten Multicast sind

Überprüfen Sie [immer, ob](probe-message.md) die Testnachrichten Multicast sind. Stellen Sie optional sicher, dass die Meldungen " [Hello](hello-message.md) " und " [Resolve](resolve-message.md) " Multicast sind. Beachten Sie, dass nicht alle Anwendungen Auflösungs Meldungen verwenden. Weitere Informationen zu Nachrichten Mustern, die von Clients und Hosts verwendet werden, finden Sie unter Ermittlungs [-und Metadatenaustausch-Nachrichten Muster](discovery-and-metadata-exchange-message-patterns.md) und ersten Schritten [mit der WSDAPI-Problem](getting-started-with-wsdapi-troubleshooting.md)Behandlung.

Nachrichten müssen ausgelöst werden, damit Sie wie in Schritt 3 oben beschrieben gesendet werden können. Der WSD-Debugclient zeigt die unformatierte SOAP-Nachricht als Ausgabe an. Da alle Nachrichten, die vom WSD-Debugclient im Multicast Modus gedruckt werden, über einen Multicast-Socket empfangen werden, wird die Zieladresse der Nachricht nicht angezeigt.

Die folgende Beispielausgabe eines WSD-Debugclients zeigt eine Testnachricht an. Das <wsa: Action>-Element identifiziert die Nachricht als Testnachricht. Überprüfen Sie das Feld <wsa: Action>, um sicherzustellen, dass die empfangene Nachricht eine Testnachricht war.

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

Die folgende Beispielausgabe eines WSD-Debugclients zeigt eine Hello-Meldung an. Das <wsa: Action>-Element identifiziert die Nachricht als Hello-Nachricht.

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

## <a name="filtering-wsd-debug-client-results"></a>Filtern der WSD-Debug-Client Ergebnisse

Das Filtern der WSD-Debug-Client Ergebnisse kann helfen, den Vorfall Datenverkehr im Zusammenhang mit dem Gerät Filter sind nur in lärmenden Netzwerken notwendig.

Es gibt zwei Möglichkeiten, Ergebnisse zu filtern. Die zu filternden IP-Adressen können explizit identifiziert werden, wenn der WSD-Debugclient gestartet wird. Alternativ können die IP-Adressen nach dem Start des Clients angegeben werden. In diesem Abschnitt werden beide Methoden beschrieben.

**So geben Sie IP-Adressen zum Filtern beim Starten des WSD-Debugclients an**

1.  Konfigurieren Sie den Host und den Client für die Netzwerk übergreifende Ausführung (d. h., stellen Sie sicher, dass der Host und der Client auf unterschiedlichen Computern ausgeführt werden).
2.  Erfassen Sie die IP-Adressen des Geräts. Wenn das Gerät über mehrere Adressen verfügt (z. b. sowohl IPv4-als auch IPv6-Adressen), müssen alle Adressen gesammelt werden.
3.  Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **wsddebug \_client.exe/Mode Multicast/IP Add***<device IP>*

*<device IP>* ist eine IP-Adresse. In der folgenden Liste werden einige Beispiel Formate für diese IP-Adresse angezeigt.

-   192.168.0.1
-   :: 1
-   mydevice.contoso.com

Der WSD-Debugclient löst die von der Eingabeaufforderung angegebenen Hostnamen automatisch auf.

**So filtern Sie Ergebnisse nach dem Starten des WSD-Debugclients**

1.  Konfigurieren Sie den Host und den Client für die Netzwerk übergreifende Ausführung (d. h., stellen Sie sicher, dass der Host und der Client auf unterschiedlichen Computern ausgeführt werden).
2.  Erfassen Sie die IP-Adressen des Geräts. Wenn das Gerät über mehrere Adressen verfügt (z. b. sowohl IPv4-als auch IPv6-Adressen), müssen alle Adressen gesammelt werden.
3.  Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **wsddebug \_client.exe/Mode Multicast**
4.  Führen Sie an der WSD-Debug-Client Eingabeaufforderung den folgenden Befehl aus: **IP-Add***<device IP>*
5.  Wiederholen Sie Schritt 4, bis alle Geräte-IP-Adressen hinzugefügt wurden.

Im folgenden Verfahren wird davon ausgegangen, dass der WSD-Debugclient gestartet wurde und nach der IP-Adresse gefiltert wird.

**So überprüfen Sie, ob die richtigen IP-Adressen gefiltert werden**

-   Führen Sie an der WSD-Debug-Client Eingabeaufforderung den folgenden Befehl aus: **IP-Print**

    Die Liste der zu filternden IP-Adressen wird angezeigt.

Im folgenden Verfahren wird davon ausgegangen, dass der WSD-Debugclient gestartet wurde und nach der IP-Adresse gefiltert wird.

**So deaktivieren Sie das Filtern**

-   Führen Sie an der WSD-Debug-Client Eingabeaufforderung den folgenden Befehl aus: **IP Clear** .

    Der gesamte Multicast Datenverkehr wird nun in der Debugausgabe angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



