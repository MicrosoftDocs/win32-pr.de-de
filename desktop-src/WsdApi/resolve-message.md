---
description: Eine WS-Discovery Nachricht, die von einem Client verwendet wird, um nach dem Namen nach Diensten im Netzwerk zu suchen.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Meldung auflösen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3390d97aad972f001b98587c6b5e7cd7ac708b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355632"
---
# <a name="resolve-message"></a><span data-ttu-id="4f93b-103">Meldung auflösen</span><span class="sxs-lookup"><span data-stu-id="4f93b-103">Resolve Message</span></span>

<span data-ttu-id="4f93b-104">Eine Auflösungs Meldung ist eine WS-Discovery Nachricht, die von einem Client verwendet wird, um nach dem Namen nach Diensten im Netzwerk zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4f93b-104">A Resolve message is a WS-Discovery message used by a client to search for services on the network by name.</span></span> <span data-ttu-id="4f93b-105">Ein Client sendet nur dann eine Auflösungs Nachricht, wenn eine HTTP-Nachricht (z. b. eine [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange-Anforderung oder eine Dienst Nachricht) gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f93b-105">A client will only send a Resolve message when an HTTP message (such as a [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange request or a service message) will be sent.</span></span> <span data-ttu-id="4f93b-106">Weitere Informationen zum Auflösen von Nachrichten finden Sie im Abschnitt 6,1 der [WS-Discovery-Spezifikation](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span><span class="sxs-lookup"><span data-stu-id="4f93b-106">For more information about Resolve messages, see section 6.1 of the [WS-Discovery Specification](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span></span>

<span data-ttu-id="4f93b-107">Eine Auflösungs Meldung wird von UDP-Multicast an Port 3702 gesendet.</span><span class="sxs-lookup"><span data-stu-id="4f93b-107">A Resolve message is sent by UDP multicast to port 3702.</span></span> <span data-ttu-id="4f93b-108">Unicast-Auflösungs Nachrichten werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f93b-108">Unicast Resolve messages are not supported.</span></span>

<span data-ttu-id="4f93b-109">DPWS-Clients senden Auflösungs Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4f93b-109">DPWS clients send Resolve messages.</span></span> <span data-ttu-id="4f93b-110">In der folgenden Liste sind Szenarien aufgeführt, in denen WSDAPI eine Resolve-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="4f93b-110">The following list shows scenarios in which WSDAPI will send a Resolve message.</span></span>

-   <span data-ttu-id="4f93b-111">Ein Funktions Ermittlungs Client sendet eine Resolve-Nachricht, wenn keine xaddrs in eine [Probe Matches](probematches-message.md) -Nachricht eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4f93b-111">A Function Discovery client sends a Resolve message if no XAddrs are included in a [ProbeMatches](probematches-message.md) message.</span></span>
-   <span data-ttu-id="4f93b-112">Ein Client, der die [**iwsdiscoveryprovider:: searchbyid**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) -Methode aufrufen, sendet eine Resolve-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4f93b-112">A client calling the [**IWSDiscoveryProvider::SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) methods will send a Resolve message.</span></span>
-   <span data-ttu-id="4f93b-113">Ein Client, der [**wsdcreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) anruft, kann eine Auflösungs Nachricht senden, wenn eine logische Geräteadresse an *pszdeviceid* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4f93b-113">A client calling [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) may send a Resolve message if a logical device address is passed to *pszDeviceId*.</span></span>
-   <span data-ttu-id="4f93b-114">Ein Client, der [**wsdcreatedeviceproxyadvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) aufruft, sendet eine Resolve-Nachricht, wenn die Funktion mit dem pdeviceaddress-Parameter auf **null** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4f93b-114">A client calling [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) will send a Resolve message if the function is called with the pDeviceAddress parameter set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="4f93b-115">Dieses Thema zeigt eine DPWS-Beispiel Nachricht, die von WSDAPI-Clients und-Hosts generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4f93b-115">This topic shows a sample DPWS message generated by WSDAPI clients and hosts.</span></span> <span data-ttu-id="4f93b-116">WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die nicht diesem Beispiel entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4f93b-116">WSDAPI will parse and accept other DPWS-compliant messages that do not conform to this sample.</span></span> <span data-ttu-id="4f93b-117">Verwenden Sie dieses Beispiel nicht zum Überprüfen der DPWS-Interoperabilität. Verwenden Sie stattdessen das [WSDAPI-grundlegende Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4f93b-117">Do not use this sample to verify DPWS interoperability; use the [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) instead.</span></span>

 

<span data-ttu-id="4f93b-118">Die folgende SOAP-Nachricht zeigt eine Beispiel Auflösungs Meldung an.</span><span class="sxs-lookup"><span data-stu-id="4f93b-118">The following SOAP message shows a sample Resolve message.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
urn:schemas-xmlsoap-org:ws:2005:04:discovery
</wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Resolve>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Resolve>
</soap:Body>
</soap:Envelope>
```

<span data-ttu-id="4f93b-119">Eine Resolve-Nachricht weist die folgenden Schwerpunkt Punkte auf.</span><span class="sxs-lookup"><span data-stu-id="4f93b-119">A Resolve message has the following focus points.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f93b-120">Fokuspunkt</span><span class="sxs-lookup"><span data-stu-id="4f93b-120">Focus point</span></span></th>
<th><span data-ttu-id="4f93b-121">XML</span><span class="sxs-lookup"><span data-stu-id="4f93b-121">XML</span></span></th>
<th><span data-ttu-id="4f93b-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f93b-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4f93b-123">Beheben</span><span class="sxs-lookup"><span data-stu-id="4f93b-123">Resolve</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td><span data-ttu-id="4f93b-124">Die Aktion SOAP auflösen identifiziert die Nachricht als Auflösungs Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4f93b-124">The Resolve SOAP action identifies the message as a Resolve message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f93b-125">Meldungs-ID</span><span class="sxs-lookup"><span data-stu-id="4f93b-125">MessageID</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td><span data-ttu-id="4f93b-126">Enthält die Nachrichten-ID, auf die in einer <a href="resolvematches-message.md">resolvematches</a> -Meldung verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4f93b-126">Contains the message identifier, which is referenced in a <a href="resolvematches-message.md">ResolveMatches</a> message.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f93b-127">Adresse</span><span class="sxs-lookup"><span data-stu-id="4f93b-127">Address</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td><span data-ttu-id="4f93b-128">Enthält die Adresse des zu lösenden Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="4f93b-128">Contains the address of the endpoint being resolved.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4f93b-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4f93b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f93b-130">Ermittlungs-und metadatenaustauschnachrichten</span><span class="sxs-lookup"><span data-stu-id="4f93b-130">Discovery and Metadata Exchange Messages</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[<span data-ttu-id="4f93b-131">Resolvematches-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4f93b-131">ResolveMatches Message</span></span>](resolvematches-message.md)
</dt> </dl>

 

 



