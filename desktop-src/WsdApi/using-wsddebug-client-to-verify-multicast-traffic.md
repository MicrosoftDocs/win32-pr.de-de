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
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a><span data-ttu-id="4a299-103">Überprüfen von Multicast Datenverkehr mithilfe des WSD-Debugclients</span><span class="sxs-lookup"><span data-stu-id="4a299-103">Using WSD Debug Client to Verify Multicast Traffic</span></span>

<span data-ttu-id="4a299-104">Wenn der generische Host und der Client einander im Netzwerk sehen können, der tatsächliche Host und Client jedoch nicht, ist es wahrscheinlich, dass das Problem in den Nachrichten liegt, die zwischen den Endpunkten über das Netzwerk gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a299-104">If the generic host and client can see each other on the network but the actual host and client cannot, it is likely that the problem is in the messages sent between the endpoints over the network.</span></span> <span data-ttu-id="4a299-105">Weitere Informationen zum generischen Host und Client finden Sie unter [Verwenden eines generischen Hosts und Clients für die UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="4a299-105">For more information about the generic host and client, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span> <span data-ttu-id="4a299-106">Da es schwierig sein kann, vollständige Netzwerk Ablauf Verfolgungen zu erfassen, zu filtern und zu lesen, kann das WSD-debugclienttool verwendet werden, um die Multicast Seiten WS-Discovery Nachrichten zu drucken.</span><span class="sxs-lookup"><span data-stu-id="4a299-106">Because full network traces can be difficult to collect, filter, and read, the WSD Debug Client tool can be used to print the multicast sides of WS-Discovery messages.</span></span>

<span data-ttu-id="4a299-107">Der WSD-Debugclient im Multicast Modus kann nur die Hälfte der Nachrichten untersuchen, da der Client keine Unicastnachrichten drucken kann.</span><span class="sxs-lookup"><span data-stu-id="4a299-107">The WSD Debug Client in multicast mode can only inspect half of the messages, since the client cannot print unicast messages.</span></span> <span data-ttu-id="4a299-108">Wenn der Unicastdatenverkehr von Interesse ist, überprüfen Sie die Untersuchung von Netzwerk Ablauf Verfolgungen [für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md)direkt.</span><span class="sxs-lookup"><span data-stu-id="4a299-108">If unicast traffic is of interest, skip directly to [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="4a299-109">Diese Prozedur zeigt eine Methode, die den gesamten Multicast Datenverkehr im Netzwerk anzeigt.</span><span class="sxs-lookup"><span data-stu-id="4a299-109">This procedure shows a method that will display all multicast traffic on the network.</span></span> <span data-ttu-id="4a299-110">Weitere Informationen zum Anzeigen von Multicast Datenverkehr zum und vom Gerät finden Sie unten im Abschnitt [Filtern von WSD-Debug-Client Ergebnissen](#filtering-wsd-debug-client-results) .</span><span class="sxs-lookup"><span data-stu-id="4a299-110">To display only multicast traffic to and from the device, see the [Filtering WSD Debug Client Results](#filtering-wsd-debug-client-results) section below.</span></span>

<span data-ttu-id="4a299-111">**So verwenden Sie den WSD-Debugclient zum Überprüfen von Multicast Datenverkehr**</span><span class="sxs-lookup"><span data-stu-id="4a299-111">**To use the WSD Debug Client to verify multicast traffic**</span></span>

1.  <span data-ttu-id="4a299-112">Konfigurieren Sie den Host und den Client für die Netzwerk übergreifende Ausführung (d. h., stellen Sie sicher, dass der Host und der Client auf unterschiedlichen Computern ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="4a299-112">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="4a299-113">Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **wsddebug \_client.exe/Mode Multicast**</span><span class="sxs-lookup"><span data-stu-id="4a299-113">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
3.  <span data-ttu-id="4a299-114">Reproduzieren Sie den Fehler Durchstarten des Hosts und Clients oder durch Drücken von F5 im Netzwerk-Explorer.</span><span class="sxs-lookup"><span data-stu-id="4a299-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
4.  <span data-ttu-id="4a299-115">Überprüfen Sie, ob die Nachrichten Multicast sind.</span><span class="sxs-lookup"><span data-stu-id="4a299-115">Verify that messages are being multicast.</span></span>

<span data-ttu-id="4a299-116">Wenn die erforderlichen Meldungen in der WSD-debugclientausgabe angezeigt werden, kann es vorkommen, dass der Anwendungsfehler im Multicast Nachrichten Inhalt oder im vorhanden sein oder Inhalt der entsprechenden unicastantwortnachrichten vorliegt.</span><span class="sxs-lookup"><span data-stu-id="4a299-116">If the required messages are displayed in the WSD Debug Client output, then the application failure may be in the multicast message content, or in the existence or content of the corresponding unicast response messages.</span></span> <span data-ttu-id="4a299-117">Führen Sie die Problembehandlung mit den Anweisungen unter Überprüfen von Netzwerk Ablauf Verfolgungen [für UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md)fort</span><span class="sxs-lookup"><span data-stu-id="4a299-117">Continue troubleshooting by following the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="4a299-118">Wenn die erforderlichen Meldungen in der WSD-debugclientausgabe angezeigt werden, ist es wahrscheinlich, dass die Quelle des Anwendungs Problems erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="4a299-118">If the required messages are displayed in the WSD Debug Client output, then it is likely that the source of the application problem has been identified.</span></span> <span data-ttu-id="4a299-119">Es ist wahrscheinlich, dass der Multicast-Datenverkehr nicht im Netzwerk übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="4a299-119">It is likely that the multicast traffic is not being transmitted on the network.</span></span> <span data-ttu-id="4a299-120">Dieser Fehler kann auftreten, wenn die Anwendung Multicast Adapter nicht ordnungsgemäß aufzählt.</span><span class="sxs-lookup"><span data-stu-id="4a299-120">This failure can happen when the application does not enumerate multicast adapters correctly.</span></span> <span data-ttu-id="4a299-121">Anwendungen müssen Multicast Datenverkehr explizit über alle Netzwerkschnittstellen senden. Andernfalls können Pakete nicht für die Loopback Schnittstelle oder für andere Schnittstellen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="4a299-121">Applications must explicitly send multicast traffic over all network interfaces; otherwise, packets may not be generated for the loopback interface or for other interfaces.</span></span> <span data-ttu-id="4a299-122">Um sicherzustellen, dass die Pakete nicht im Netzwerk angezeigt werden, befolgen Sie die Anweisungen unter Überprüfen von Netzwerk Ablauf Verfolgungen [für UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) und suchen nach Beweisen für fehlende Multicast Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4a299-122">To verify that the packets are not appearing on the network, follow the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and look for evidence of missing multicast messages.</span></span>

## <a name="verifying-that-messages-are-being-multicast"></a><span data-ttu-id="4a299-123">Überprüfen, ob Nachrichten Multicast sind</span><span class="sxs-lookup"><span data-stu-id="4a299-123">Verifying that messages are being multicast</span></span>

<span data-ttu-id="4a299-124">Überprüfen Sie [immer, ob](probe-message.md) die Testnachrichten Multicast sind.</span><span class="sxs-lookup"><span data-stu-id="4a299-124">Always verify that [Probe](probe-message.md) messages are being multicast.</span></span> <span data-ttu-id="4a299-125">Stellen Sie optional sicher, dass die Meldungen " [Hello](hello-message.md) " und " [Resolve](resolve-message.md) " Multicast sind.</span><span class="sxs-lookup"><span data-stu-id="4a299-125">Optionally, verify that [Hello](hello-message.md) and [Resolve](resolve-message.md) messages are being multicast.</span></span> <span data-ttu-id="4a299-126">Beachten Sie, dass nicht alle Anwendungen Auflösungs Meldungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a299-126">Note that not all applications use Resolve messages.</span></span> <span data-ttu-id="4a299-127">Weitere Informationen zu Nachrichten Mustern, die von Clients und Hosts verwendet werden, finden Sie unter Ermittlungs [-und Metadatenaustausch-Nachrichten Muster](discovery-and-metadata-exchange-message-patterns.md) und ersten Schritten [mit der WSDAPI-Problem](getting-started-with-wsdapi-troubleshooting.md)Behandlung.</span><span class="sxs-lookup"><span data-stu-id="4a299-127">For more information about message patterns used by clients and hosts, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and [Getting Started with WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span></span>

<span data-ttu-id="4a299-128">Nachrichten müssen ausgelöst werden, damit Sie wie in Schritt 3 oben beschrieben gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4a299-128">Messages must be triggered in order to be sent as described in step 3 above.</span></span> <span data-ttu-id="4a299-129">Der WSD-Debugclient zeigt die unformatierte SOAP-Nachricht als Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="4a299-129">The WSD Debug Client displays the raw SOAP message as output.</span></span> <span data-ttu-id="4a299-130">Da alle Nachrichten, die vom WSD-Debugclient im Multicast Modus gedruckt werden, über einen Multicast-Socket empfangen werden, wird die Zieladresse der Nachricht nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a299-130">Because all messages printed by WSD Debug Client in multicast mode are received over a multicast socket, the message destination address is not displayed.</span></span>

<span data-ttu-id="4a299-131">Die folgende Beispielausgabe eines WSD-Debugclients zeigt eine Testnachricht an.</span><span class="sxs-lookup"><span data-stu-id="4a299-131">The following sample WSD Debug Client output shows a Probe message.</span></span> <span data-ttu-id="4a299-132">Das <wsa: Action>-Element identifiziert die Nachricht als Testnachricht.</span><span class="sxs-lookup"><span data-stu-id="4a299-132">The <wsa:Action> element identifies the message as a Probe message.</span></span> <span data-ttu-id="4a299-133">Überprüfen Sie das Feld <wsa: Action>, um sicherzustellen, dass die empfangene Nachricht eine Testnachricht war.</span><span class="sxs-lookup"><span data-stu-id="4a299-133">Inspect the <wsa:Action> field to verify that the received message was a Probe message.</span></span>

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

<span data-ttu-id="4a299-134">Die folgende Beispielausgabe eines WSD-Debugclients zeigt eine Hello-Meldung an.</span><span class="sxs-lookup"><span data-stu-id="4a299-134">The following sample WSD Debug Client output shows a Hello message.</span></span> <span data-ttu-id="4a299-135">Das <wsa: Action>-Element identifiziert die Nachricht als Hello-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4a299-135">The <wsa:Action> element identifies the message as a Hello message.</span></span>

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

## <a name="filtering-wsd-debug-client-results"></a><span data-ttu-id="4a299-136">Filtern der WSD-Debug-Client Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="4a299-136">Filtering WSD Debug Client Results</span></span>

<span data-ttu-id="4a299-137">Das Filtern der WSD-Debug-Client Ergebnisse kann helfen, den Vorfall Datenverkehr im Zusammenhang mit dem Gerät</span><span class="sxs-lookup"><span data-stu-id="4a299-137">Filtering the WSD Debug Client results can help identify incident traffic involving the device.</span></span> <span data-ttu-id="4a299-138">Filter sind nur in lärmenden Netzwerken notwendig.</span><span class="sxs-lookup"><span data-stu-id="4a299-138">Filtering is only necessary on noisy networks.</span></span>

<span data-ttu-id="4a299-139">Es gibt zwei Möglichkeiten, Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="4a299-139">There are two ways to filter results.</span></span> <span data-ttu-id="4a299-140">Die zu filternden IP-Adressen können explizit identifiziert werden, wenn der WSD-Debugclient gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4a299-140">The IP addresses to filter can be explicitly identified when starting the WSD Debug Client.</span></span> <span data-ttu-id="4a299-141">Alternativ können die IP-Adressen nach dem Start des Clients angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a299-141">Alternatively, the IP addresses can be specified after the client has started.</span></span> <span data-ttu-id="4a299-142">In diesem Abschnitt werden beide Methoden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a299-142">This section describes both methods.</span></span>

<span data-ttu-id="4a299-143">**So geben Sie IP-Adressen zum Filtern beim Starten des WSD-Debugclients an**</span><span class="sxs-lookup"><span data-stu-id="4a299-143">**To specify IP addresses to filter when starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="4a299-144">Konfigurieren Sie den Host und den Client für die Netzwerk übergreifende Ausführung (d. h., stellen Sie sicher, dass der Host und der Client auf unterschiedlichen Computern ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="4a299-144">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="4a299-145">Erfassen Sie die IP-Adressen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="4a299-145">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="4a299-146">Wenn das Gerät über mehrere Adressen verfügt (z. b. sowohl IPv4-als auch IPv6-Adressen), müssen alle Adressen gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="4a299-146">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="4a299-147">Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: \**wsddebug \_client.exe/Mode Multicast/IP Add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="4a299-147">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast /ip add** *<device IP>*</span></span>

<span data-ttu-id="4a299-148">*<device IP>* ist eine IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="4a299-148">*<device IP>* is an IP address.</span></span> <span data-ttu-id="4a299-149">In der folgenden Liste werden einige Beispiel Formate für diese IP-Adresse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a299-149">The following list shows some sample formats for this IP address.</span></span>

-   <span data-ttu-id="4a299-150">192.168.0.1</span><span class="sxs-lookup"><span data-stu-id="4a299-150">192.168.0.1</span></span>
-   <span data-ttu-id="4a299-151">:: 1</span><span class="sxs-lookup"><span data-stu-id="4a299-151">::1</span></span>
-   <span data-ttu-id="4a299-152">mydevice.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4a299-152">mydevice.contoso.com</span></span>

<span data-ttu-id="4a299-153">Der WSD-Debugclient löst die von der Eingabeaufforderung angegebenen Hostnamen automatisch auf.</span><span class="sxs-lookup"><span data-stu-id="4a299-153">The WSD Debug Client automatically resolves hostnames supplied at the command prompt.</span></span>

<span data-ttu-id="4a299-154">**So filtern Sie Ergebnisse nach dem Starten des WSD-Debugclients**</span><span class="sxs-lookup"><span data-stu-id="4a299-154">**To filter results after starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="4a299-155">Konfigurieren Sie den Host und den Client für die Netzwerk übergreifende Ausführung (d. h., stellen Sie sicher, dass der Host und der Client auf unterschiedlichen Computern ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="4a299-155">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="4a299-156">Erfassen Sie die IP-Adressen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="4a299-156">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="4a299-157">Wenn das Gerät über mehrere Adressen verfügt (z. b. sowohl IPv4-als auch IPv6-Adressen), müssen alle Adressen gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="4a299-157">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="4a299-158">Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **wsddebug \_client.exe/Mode Multicast**</span><span class="sxs-lookup"><span data-stu-id="4a299-158">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
4.  <span data-ttu-id="4a299-159">Führen Sie an der WSD-Debug-Client Eingabeaufforderung den folgenden Befehl aus: \**IP-Add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="4a299-159">At the WSD Debug Client command prompt, run the following command: **ip add** *<device IP>*</span></span>
5.  <span data-ttu-id="4a299-160">Wiederholen Sie Schritt 4, bis alle Geräte-IP-Adressen hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="4a299-160">Repeat step 4 until all device IP addresses have been added.</span></span>

<span data-ttu-id="4a299-161">Im folgenden Verfahren wird davon ausgegangen, dass der WSD-Debugclient gestartet wurde und nach der IP-Adresse gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="4a299-161">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="4a299-162">**So überprüfen Sie, ob die richtigen IP-Adressen gefiltert werden**</span><span class="sxs-lookup"><span data-stu-id="4a299-162">**To verify that the correct IP addresses are being filtered**</span></span>

-   <span data-ttu-id="4a299-163">Führen Sie an der WSD-Debug-Client Eingabeaufforderung den folgenden Befehl aus: **IP-Print**</span><span class="sxs-lookup"><span data-stu-id="4a299-163">At the WSD Debug Client command prompt, run the following command: **ip print**</span></span>

    <span data-ttu-id="4a299-164">Die Liste der zu filternden IP-Adressen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a299-164">The list of IP addresses being filtered appears.</span></span>

<span data-ttu-id="4a299-165">Im folgenden Verfahren wird davon ausgegangen, dass der WSD-Debugclient gestartet wurde und nach der IP-Adresse gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="4a299-165">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="4a299-166">**So deaktivieren Sie das Filtern**</span><span class="sxs-lookup"><span data-stu-id="4a299-166">**To disable filtering**</span></span>

-   <span data-ttu-id="4a299-167">Führen Sie an der WSD-Debug-Client Eingabeaufforderung den folgenden Befehl aus: **IP Clear** .</span><span class="sxs-lookup"><span data-stu-id="4a299-167">At the WSD Debug Client command prompt, run the following command: **ip clear**</span></span>

    <span data-ttu-id="4a299-168">Der gesamte Multicast Datenverkehr wird nun in der Debugausgabe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a299-168">All multicast traffic will now be shown in the debug output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a299-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a299-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a299-170">WSDAPI-Diagnose Prozeduren</span><span class="sxs-lookup"><span data-stu-id="4a299-170">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="4a299-171">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="4a299-171">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



