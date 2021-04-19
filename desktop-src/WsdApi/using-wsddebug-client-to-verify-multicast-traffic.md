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
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a><span data-ttu-id="e5d33-103">Verwenden des WSD-Debugclients zum Überprüfen des Multicastdatenverkehrs</span><span class="sxs-lookup"><span data-stu-id="e5d33-103">Using WSD Debug Client to Verify Multicast Traffic</span></span>

<span data-ttu-id="e5d33-104">Wenn sich der generische Host und der Client im Netzwerk sehen können, der tatsächliche Host und der Client jedoch nicht, liegt das Problem wahrscheinlich in den Nachrichten, die zwischen den Endpunkten über das Netzwerk gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-104">If the generic host and client can see each other on the network but the actual host and client cannot, it is likely that the problem is in the messages sent between the endpoints over the network.</span></span> <span data-ttu-id="e5d33-105">Weitere Informationen zum generischen Host und Client finden Sie unter [Verwenden eines generischen Hosts und Clients für die UDP-WS-Ermittlung.](using-a-generic-host-and-client-for-udp-ws-discovery.md)</span><span class="sxs-lookup"><span data-stu-id="e5d33-105">For more information about the generic host and client, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span> <span data-ttu-id="e5d33-106">Da vollständige Netzwerkablaufverfolgungen schwierig zu erfassen, zu filtern und zu lesen sind, kann das WSD-Debugclienttool zum Drucken der Multicastseiten WS-Discovery Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-106">Because full network traces can be difficult to collect, filter, and read, the WSD Debug Client tool can be used to print the multicast sides of WS-Discovery messages.</span></span>

<span data-ttu-id="e5d33-107">Der WSD-Debugclient im Multicastmodus kann nur die Hälfte der Nachrichten überprüfen, da der Client keine Unicastnachrichten drucken kann.</span><span class="sxs-lookup"><span data-stu-id="e5d33-107">The WSD Debug Client in multicast mode can only inspect half of the messages, since the client cannot print unicast messages.</span></span> <span data-ttu-id="e5d33-108">Wenn Unicastdatenverkehr von Interesse ist, fahren Sie direkt mit [Inspecting Network Traces for UDP WS-Discovery (Untersuchen von Netzwerkablaufverfolgungen für die UDP-WS-Ermittlung)](inspecting-network-traces-for-udp-ws-discovery.md)über.</span><span class="sxs-lookup"><span data-stu-id="e5d33-108">If unicast traffic is of interest, skip directly to [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="e5d33-109">Dieses Verfahren zeigt eine Methode, die den gesamten Multicastdatenverkehr im Netzwerk anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e5d33-109">This procedure shows a method that will display all multicast traffic on the network.</span></span> <span data-ttu-id="e5d33-110">Informationen zum Anzeigen von Multicastdatenverkehr zum und vom Gerät finden Sie weiter unten im Abschnitt Filtern von [WSD-Debugclientergebnissen.](#filtering-wsd-debug-client-results)</span><span class="sxs-lookup"><span data-stu-id="e5d33-110">To display only multicast traffic to and from the device, see the [Filtering WSD Debug Client Results](#filtering-wsd-debug-client-results) section below.</span></span>

<span data-ttu-id="e5d33-111">**So verwenden Sie den WSD-Debugclient zum Überprüfen des Multicastdatenverkehrs**</span><span class="sxs-lookup"><span data-stu-id="e5d33-111">**To use the WSD Debug Client to verify multicast traffic**</span></span>

1.  <span data-ttu-id="e5d33-112">Konfigurieren Sie den Host und den Client so, dass sie über das Netzwerk ausgeführt werden .(Stellen Sie also sicher, dass der Host und der Client auf verschiedenen Computern ausgeführt werden.)</span><span class="sxs-lookup"><span data-stu-id="e5d33-112">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="e5d33-113">Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **WSDDebug \_client.exe /mode multicast**</span><span class="sxs-lookup"><span data-stu-id="e5d33-113">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
3.  <span data-ttu-id="e5d33-114">Reproduzieren Sie den Fehler, indem Sie host und client starten oder F5 im Netzwerk-Explorer drücken.</span><span class="sxs-lookup"><span data-stu-id="e5d33-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
4.  <span data-ttu-id="e5d33-115">Überprüfen Sie, ob Nachrichten multicastiert werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-115">Verify that messages are being multicast.</span></span>

<span data-ttu-id="e5d33-116">Wenn die erforderlichen Nachrichten in der Ausgabe des WSD-Debugclients angezeigt werden, kann sich der Anwendungsfehler im Inhalt der Multicastnachricht oder im Vorhandensein oder Inhalt der entsprechenden Unicastantwortnachrichten befinden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-116">If the required messages are displayed in the WSD Debug Client output, then the application failure may be in the multicast message content, or in the existence or content of the corresponding unicast response messages.</span></span> <span data-ttu-id="e5d33-117">Fahren Sie mit der Problembehandlung fort, indem Sie die Anweisungen unter [Überprüfen von Netzwerkablaufverfolgungen für die UDP-WS-Ermittlung](inspecting-network-traces-for-udp-ws-discovery.md)befolgen.</span><span class="sxs-lookup"><span data-stu-id="e5d33-117">Continue troubleshooting by following the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="e5d33-118">Wenn die erforderlichen Meldungen in der Ausgabe des WSD-Debugclients angezeigt werden, ist es wahrscheinlich, dass die Quelle des Anwendungsproblems identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="e5d33-118">If the required messages are displayed in the WSD Debug Client output, then it is likely that the source of the application problem has been identified.</span></span> <span data-ttu-id="e5d33-119">Es ist wahrscheinlich, dass der Multicastdatenverkehr nicht im Netzwerk übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="e5d33-119">It is likely that the multicast traffic is not being transmitted on the network.</span></span> <span data-ttu-id="e5d33-120">Dieser Fehler kann passieren, wenn die Anwendung Multicastadapter nicht ordnungsgemäß aufzählt.</span><span class="sxs-lookup"><span data-stu-id="e5d33-120">This failure can happen when the application does not enumerate multicast adapters correctly.</span></span> <span data-ttu-id="e5d33-121">Anwendungen müssen explizit Multicastdatenverkehr über alle Netzwerkschnittstellen senden. Andernfalls werden pakete möglicherweise nicht für die Loopbackschnittstelle oder für andere Schnittstellen generiert.</span><span class="sxs-lookup"><span data-stu-id="e5d33-121">Applications must explicitly send multicast traffic over all network interfaces; otherwise, packets may not be generated for the loopback interface or for other interfaces.</span></span> <span data-ttu-id="e5d33-122">Um sicherzustellen, dass die Pakete nicht im Netzwerk angezeigt werden, befolgen Sie die Anweisungen unter Überprüfen von Netzwerkverfolgungen für [die UDP-WS-Ermittlung,](inspecting-network-traces-for-udp-ws-discovery.md) und suchen Sie nach Beweisen für fehlende Multicastnachrichten.</span><span class="sxs-lookup"><span data-stu-id="e5d33-122">To verify that the packets are not appearing on the network, follow the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and look for evidence of missing multicast messages.</span></span>

## <a name="verifying-that-messages-are-being-multicast"></a><span data-ttu-id="e5d33-123">Überprüfen, ob Nachrichten Multicast verwenden</span><span class="sxs-lookup"><span data-stu-id="e5d33-123">Verifying that messages are being multicast</span></span>

<span data-ttu-id="e5d33-124">Vergewissern Sie sich [immer, dass](probe-message.md) Testnachrichten multicastt werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-124">Always verify that [Probe](probe-message.md) messages are being multicast.</span></span> <span data-ttu-id="e5d33-125">Überprüfen Sie optional, ob [Hello-](hello-message.md) und [Resolve-Nachrichten](resolve-message.md) multicast sind.</span><span class="sxs-lookup"><span data-stu-id="e5d33-125">Optionally, verify that [Hello](hello-message.md) and [Resolve](resolve-message.md) messages are being multicast.</span></span> <span data-ttu-id="e5d33-126">Beachten Sie, dass nicht alle Anwendungen Nachrichten auflösen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-126">Note that not all applications use Resolve messages.</span></span> <span data-ttu-id="e5d33-127">Weitere Informationen zu Nachrichtenmustern, die von Clients und Hosts verwendet werden, finden Sie unter Discovery [and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and Erste Schritte with [WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="e5d33-127">For more information about message patterns used by clients and hosts, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and [Getting Started with WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span></span>

<span data-ttu-id="e5d33-128">Nachrichten müssen ausgelöst werden, um wie in Schritt 3 oben beschrieben gesendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-128">Messages must be triggered in order to be sent as described in step 3 above.</span></span> <span data-ttu-id="e5d33-129">Der WSD-Debugclient zeigt die unformatierte SOAP-Nachricht als Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="e5d33-129">The WSD Debug Client displays the raw SOAP message as output.</span></span> <span data-ttu-id="e5d33-130">Da alle vom WSD-Debugclient im Multicastmodus gedruckten Nachrichten über einen Multicastsocket empfangen werden, wird die Nachrichtenzieladresse nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e5d33-130">Because all messages printed by WSD Debug Client in multicast mode are received over a multicast socket, the message destination address is not displayed.</span></span>

<span data-ttu-id="e5d33-131">Die folgende Beispielausgabe des WSD-Debugclients zeigt eine Testmeldung.</span><span class="sxs-lookup"><span data-stu-id="e5d33-131">The following sample WSD Debug Client output shows a Probe message.</span></span> <span data-ttu-id="e5d33-132">Das \<wsa:Action> -Element identifiziert die Nachricht als Testnachricht.</span><span class="sxs-lookup"><span data-stu-id="e5d33-132">The \<wsa:Action> element identifies the message as a Probe message.</span></span> <span data-ttu-id="e5d33-133">Überprüfen Sie das \<wsa:Action> Feld, um sicherzustellen, dass die empfangene Nachricht eine Testnachricht war.</span><span class="sxs-lookup"><span data-stu-id="e5d33-133">Inspect the \<wsa:Action> field to verify that the received message was a Probe message.</span></span>

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

<span data-ttu-id="e5d33-134">Die folgende Beispielausgabe des WSD-Debugclients zeigt eine Hello-Meldung.</span><span class="sxs-lookup"><span data-stu-id="e5d33-134">The following sample WSD Debug Client output shows a Hello message.</span></span> <span data-ttu-id="e5d33-135">Das \<wsa:Action> -Element identifiziert die Nachricht als Hello-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e5d33-135">The \<wsa:Action> element identifies the message as a Hello message.</span></span>

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

## <a name="filtering-wsd-debug-client-results"></a><span data-ttu-id="e5d33-136">Filtern von WSD-Debugclientergebnissen</span><span class="sxs-lookup"><span data-stu-id="e5d33-136">Filtering WSD Debug Client Results</span></span>

<span data-ttu-id="e5d33-137">Durch Filtern der Ergebnisse des WSD-Debugclients können Incidentdatenverkehr im Zusammenhang mit dem Gerät identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-137">Filtering the WSD Debug Client results can help identify incident traffic involving the device.</span></span> <span data-ttu-id="e5d33-138">Filterung ist nur in lauten Netzwerken erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e5d33-138">Filtering is only necessary on noisy networks.</span></span>

<span data-ttu-id="e5d33-139">Es gibt zwei Möglichkeiten, Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="e5d33-139">There are two ways to filter results.</span></span> <span data-ttu-id="e5d33-140">Die zu filternden IP-Adressen können beim Starten des WSD-Debugclients explizit identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-140">The IP addresses to filter can be explicitly identified when starting the WSD Debug Client.</span></span> <span data-ttu-id="e5d33-141">Alternativ können die IP-Adressen angegeben werden, nachdem der Client gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="e5d33-141">Alternatively, the IP addresses can be specified after the client has started.</span></span> <span data-ttu-id="e5d33-142">In diesem Abschnitt werden beide Methoden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e5d33-142">This section describes both methods.</span></span>

<span data-ttu-id="e5d33-143">**So geben Sie ip-Adressen an, die beim Starten des WSD-Debugclients gefiltert werden sollen**</span><span class="sxs-lookup"><span data-stu-id="e5d33-143">**To specify IP addresses to filter when starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="e5d33-144">Konfigurieren Sie den Host und den Client so, dass sie über das Netzwerk ausgeführt werden .(Stellen Sie also sicher, dass der Host und der Client auf verschiedenen Computern ausgeführt werden.)</span><span class="sxs-lookup"><span data-stu-id="e5d33-144">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="e5d33-145">Erfassen Sie die IP-Adressen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="e5d33-145">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="e5d33-146">Wenn das Gerät über mehrere Adressen verfügt (z. B. sowohl IPv4- als auch IPv6-Adressen), müssen alle Adressen gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-146">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="e5d33-147">Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: \**WSDDebug \_client.exe /mode multicast /ip add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="e5d33-147">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast /ip add** *<device IP>*</span></span>

<span data-ttu-id="e5d33-148">*<device IP>* ist eine IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e5d33-148">*<device IP>* is an IP address.</span></span> <span data-ttu-id="e5d33-149">Die folgende Liste enthält einige Beispielformate für diese IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e5d33-149">The following list shows some sample formats for this IP address.</span></span>

-   <span data-ttu-id="e5d33-150">192.168.0.1</span><span class="sxs-lookup"><span data-stu-id="e5d33-150">192.168.0.1</span></span>
-   <span data-ttu-id="e5d33-151">::1</span><span class="sxs-lookup"><span data-stu-id="e5d33-151">::1</span></span>
-   <span data-ttu-id="e5d33-152">mydevice.contoso.com</span><span class="sxs-lookup"><span data-stu-id="e5d33-152">mydevice.contoso.com</span></span>

<span data-ttu-id="e5d33-153">Der WSD-Debugclient löst automatisch hostnames auf, die an der Eingabeaufforderung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-153">The WSD Debug Client automatically resolves hostnames supplied at the command prompt.</span></span>

<span data-ttu-id="e5d33-154">**So filtern Sie ergebnisse nach dem Starten des WSD-Debugclients**</span><span class="sxs-lookup"><span data-stu-id="e5d33-154">**To filter results after starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="e5d33-155">Konfigurieren Sie den Host und den Client so, dass sie über das Netzwerk ausgeführt werden .(Stellen Sie also sicher, dass der Host und der Client auf verschiedenen Computern ausgeführt werden.)</span><span class="sxs-lookup"><span data-stu-id="e5d33-155">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="e5d33-156">Erfassen Sie die IP-Adressen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="e5d33-156">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="e5d33-157">Wenn das Gerät über mehrere Adressen verfügt (z. B. sowohl IPv4- als auch IPv6-Adressen), müssen alle Adressen gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-157">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="e5d33-158">Öffnen Sie eine Eingabeaufforderung, und führen Sie den folgenden Befehl aus: **WSDDebug \_client.exe /mode multicast**</span><span class="sxs-lookup"><span data-stu-id="e5d33-158">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
4.  <span data-ttu-id="e5d33-159">Führen Sie an der Eingabeaufforderung des WSD-Debugclients den folgenden Befehl aus: \**ip add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="e5d33-159">At the WSD Debug Client command prompt, run the following command: **ip add** *<device IP>*</span></span>
5.  <span data-ttu-id="e5d33-160">Wiederholen Sie Schritt 4, bis alle IP-Adressen des Geräts hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="e5d33-160">Repeat step 4 until all device IP addresses have been added.</span></span>

<span data-ttu-id="e5d33-161">Beim folgenden Verfahren wird davon ausgegangen, dass der WSD-Debugclient gestartet wurde und eine Filterung nach IP-Adresse erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e5d33-161">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="e5d33-162">**So überprüfen Sie, ob die richtigen IP-Adressen gefiltert werden**</span><span class="sxs-lookup"><span data-stu-id="e5d33-162">**To verify that the correct IP addresses are being filtered**</span></span>

-   <span data-ttu-id="e5d33-163">Führen Sie an der Eingabeaufforderung des WSD-Debugclients den folgenden Befehl aus: **ip print**</span><span class="sxs-lookup"><span data-stu-id="e5d33-163">At the WSD Debug Client command prompt, run the following command: **ip print**</span></span>

    <span data-ttu-id="e5d33-164">Die Liste der ip-Adressen, die gefiltert werden, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e5d33-164">The list of IP addresses being filtered appears.</span></span>

<span data-ttu-id="e5d33-165">Beim folgenden Verfahren wird davon ausgegangen, dass der WSD-Debugclient gestartet wurde und eine Filterung nach IP-Adresse erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e5d33-165">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="e5d33-166">**So deaktivieren Sie die Filterung**</span><span class="sxs-lookup"><span data-stu-id="e5d33-166">**To disable filtering**</span></span>

-   <span data-ttu-id="e5d33-167">Führen Sie an der Eingabeaufforderung des WSD-Debugclients den folgenden Befehl aus: **ip clear**</span><span class="sxs-lookup"><span data-stu-id="e5d33-167">At the WSD Debug Client command prompt, run the following command: **ip clear**</span></span>

    <span data-ttu-id="e5d33-168">Der ganze Multicastdatenverkehr wird nun in der Debugausgabe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e5d33-168">All multicast traffic will now be shown in the debug output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5d33-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5d33-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5d33-170">WSDAPI-Diagnoseverfahren</span><span class="sxs-lookup"><span data-stu-id="e5d33-170">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="e5d33-171">Erste Schritte mit WSDAPI – Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="e5d33-171">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



