---
title: Dienst Proxy
description: Bei einem Dienst Proxy handelt es sich um den Client seitigen Proxy für einen Dienst.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Dienst Proxy-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106361113"
---
# <a name="service-proxy"></a><span data-ttu-id="fb398-106">Dienst Proxy</span><span class="sxs-lookup"><span data-stu-id="fb398-106">Service Proxy</span></span>

<span data-ttu-id="fb398-107">Bei einem Dienst Proxy handelt es sich um den Client seitigen Proxy für einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="fb398-107">A service proxy is the client side proxy for a service.</span></span> <span data-ttu-id="fb398-108">Der Dienst Proxy ermöglicht Anwendungen das Senden und empfangen von [Nachrichten](message.md) über einen [Kanal](channel.md) als Methodenaufrufe.</span><span class="sxs-lookup"><span data-stu-id="fb398-108">The service proxy enables applications to send and receive [messages](message.md) over a [channel](channel.md) as method calls.</span></span>

<span data-ttu-id="fb398-109">Dienst Proxys werden bei Bedarf erstellt, geöffnet, zum aufzurufen eines Dienstanbieter verwendet und geschlossen, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="fb398-109">Service proxies are created as needed, opened, used to call a service, and closed when no longer needed.</span></span> <span data-ttu-id="fb398-110">Alternativ kann eine Anwendung einen Dienst Proxy wieder verwenden, um wiederholt eine Verbindung zum gleichen Dienst herzustellen, ohne Zeit und Ressourcen zu verwenden, die für die mehrmalige Initialisierung eines Dienst Proxys erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fb398-110">Alternatively, an application may reuse a service proxy to connect repeatedly to the same service without the expenditure of time and resources required for initialising a service proxy more than once.</span></span> <span data-ttu-id="fb398-111">Das folgende Diagramm veranschaulicht den Fluss der möglichen Zustände des Dienst Proxys und der Funktionsaufrufe oder Ereignisse, die von einem Zustand zu einem anderen geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="fb398-111">The following diagram illustrates the flow of the possible states of the service proxy and the function calls or events that lead from one state to another.</span></span>

![Das Diagramm zeigt die Dienst Proxy Zustände und die Funktionsaufrufe oder Ereignisse, die von einem Zustand zu einem anderen geführt haben.](images/serviceproxystates.png)

<span data-ttu-id="fb398-113">Diese Dienst Proxy Zustände werden in der WS- [**\_ Dienst- \_ Proxy \_ Zustands**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) Enumeration aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fb398-113">These service proxy states are enumerated in the [**WS\_SERVICE\_PROXY\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) enumeration.</span></span>

<span data-ttu-id="fb398-114">Wie das obige Diagramm und der folgende Code veranschaulichen, wird ein Dienst Proxy durch einen Aufrufen der [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) -Funktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="fb398-114">As the preceding diagram and the following code illustrate, a service proxy is created by a call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span> <span data-ttu-id="fb398-115">Als Parameter für diesen Befehl stellt wwsapi die folgenden Enumerationen bereit:</span><span class="sxs-lookup"><span data-stu-id="fb398-115">As parameters for this call, WWSAPI provides the following enumerations:</span></span>

-   [<span data-ttu-id="fb398-116">**WS \_ - \_ Kanaltyp**</span><span class="sxs-lookup"><span data-stu-id="fb398-116">**WS\_CHANNEL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [<span data-ttu-id="fb398-117">**WS- \_ Kanal \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="fb398-117">**WS\_CHANNEL\_BINDING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

<span data-ttu-id="fb398-118">Außerdem akzeptiert es optionale Parameter unter Verwendung der folgenden Datentypen:</span><span class="sxs-lookup"><span data-stu-id="fb398-118">It also accepts optional parameters using the following data types:</span></span>

-   [<span data-ttu-id="fb398-119">**WS- \_ Proxy- \_ Eigenschaften- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="fb398-119">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [<span data-ttu-id="fb398-120">**WS- \_ Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb398-120">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

<span data-ttu-id="fb398-121">Wenn der Dienst Proxy erstellt wurde, gibt die **wscreateserviceproxy** -Funktion einen Verweis auf den Dienst Proxy ( [WS- \_ Dienst \_ Proxy](ws-service-proxy.md)) über einen out-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="fb398-121">When the service proxy has been created, the **WsCreateServiceProxy** function returns a reference to the service proxy, [WS\_SERVICE\_PROXY](ws-service-proxy.md), through an out parameter.</span></span>

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

<span data-ttu-id="fb398-122">Beim Erstellen des Dienst Proxys kann die Anwendung den Dienst Proxy für die Kommunikation mit einem Dienst öffnen, indem Sie die [**wsopenserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) -Funktion aufrufen und eine [**Adress**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) Struktur mit der Netzwerkadresse des Dienst Endpunkts übergibt, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb398-122">When the service proxy has been created, the application can open the service proxy for communication to a service by calling the [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) function, passing an [**address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure containing the network address of the service endpoint to connect to.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

<span data-ttu-id="fb398-123">Wenn der Dienst Proxy geöffnet wurde, kann er von der Anwendung verwendet werden, um Aufrufe an den Dienst durchführen.</span><span class="sxs-lookup"><span data-stu-id="fb398-123">When the service proxy has been opened, the application can use it to make calls to the service.</span></span>

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

<span data-ttu-id="fb398-124">Wenn die Anwendung den Dienst Proxy nicht mehr benötigt, wird der Dienst Proxy durch Aufrufen der [**wscloseserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) -Funktion geschlossen.</span><span class="sxs-lookup"><span data-stu-id="fb398-124">When the application no longer needs the service proxy, it closes the service proxy by calling the [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) function.</span></span> <span data-ttu-id="fb398-125">Außerdem wird der zugehörige Speicher durch Aufrufen von [**wsfreeserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)freigegeben.</span><span class="sxs-lookup"><span data-stu-id="fb398-125">It also frees the associated memory by calling [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span></span>

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a><span data-ttu-id="fb398-126">Wieder verwenden des Dienst Proxys</span><span class="sxs-lookup"><span data-stu-id="fb398-126">Reusing the Service Proxy</span></span>

<span data-ttu-id="fb398-127">Alternativ kann eine Anwendung nach dem Aufrufen von [**wscloseserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) den Dienst Proxy wieder verwenden, indem Sie die [**wsresetserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="fb398-127">Alternatively, after calling [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) an application can reuse the service proxy by calling the [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) function.</span></span>

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

<span data-ttu-id="fb398-128">Weitere Informationen zur Verwendung von Dienst Proxys in verschiedenen Kontexten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="fb398-128">For more information on how service proxies are used in different contexts, see the following topics:</span></span>

-   [<span data-ttu-id="fb398-129">Dienst Proxy und-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="fb398-129">Service Proxy and Sessions</span></span>](service-proxy-and-sessions.md)
-   [<span data-ttu-id="fb398-130">Dienst Vorgang</span><span class="sxs-lookup"><span data-stu-id="fb398-130">Service Operation</span></span>](service-operation.md)
-   [<span data-ttu-id="fb398-131">Client seitige Dienst Vorgänge</span><span class="sxs-lookup"><span data-stu-id="fb398-131">Client Side Service Operations</span></span>](client-side-service-operations.md)
-   [<span data-ttu-id="fb398-132">Httpcalculatorclieintexample</span><span class="sxs-lookup"><span data-stu-id="fb398-132">HttpCalculatorClientExample</span></span>](httpcalculatorclientexample.md)

### <a name="security"></a><span data-ttu-id="fb398-133">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="fb398-133">Security</span></span>

<span data-ttu-id="fb398-134">Beachten Sie die folgenden Überlegungen zum Anwendungs Entwurf, wenn Sie die wwsapi-Dienst Proxy-API verwenden:</span><span class="sxs-lookup"><span data-stu-id="fb398-134">Following application design considerations should be carefully noted when you use the WWSAPI service proxy API:</span></span>

-   <span data-ttu-id="fb398-135">Der Dienst Proxy führt keine Überprüfung der Daten über die grundlegenden Profile 2,0-Validierung und XML-Serialisierung hinaus aus.</span><span class="sxs-lookup"><span data-stu-id="fb398-135">The service proxy will not perform any validation of the data beyond Basic Profile 2.0 validation and XML serialization.</span></span> <span data-ttu-id="fb398-136">Die Anwendung ist dafür verantwortlich, die Daten zu überprüfen, die in den Parametern enthalten sind, die Sie als Teil des Aufrufens erhalten.</span><span class="sxs-lookup"><span data-stu-id="fb398-136">It is the responsibility of the application to validate the data contained in the parameters it receives back as part of the call.</span></span>
-   <span data-ttu-id="fb398-137">Das Konfigurieren der maximalen Anzahl ausstehender Aufrufe für den Dienst Proxy mithilfe des [**WS- \_ \_ proxyeigenschafts- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) -Enumerationswerts **WS \_ Proxy \_ Eigenschaft \_ Max \_ ausstehende \_ Aufrufe** bietet Schutz vor einem Server mit langsamer Ausführung.</span><span class="sxs-lookup"><span data-stu-id="fb398-137">Configuring the maximum number of pending calls on the service proxy, by using the [**WS\_PROXY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) enumeration value **WS\_PROXY\_PROPERTY\_MAX\_PENDING\_CALLS**, provides protection against a slow running server.</span></span> <span data-ttu-id="fb398-138">Der Standardwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="fb398-138">The default maximum is 100.</span></span> <span data-ttu-id="fb398-139">Anwendungen müssen bei der Änderung der Standardeinstellungen vorsichtig sein.</span><span class="sxs-lookup"><span data-stu-id="fb398-139">Applications must be careful in modifying the defaults.</span></span>
-   <span data-ttu-id="fb398-140">Der Dienst Proxy bietet keine Sicherheitsgarantien, die über diejenigen hinausgehen, die in der [**WS- \_ Sicherheits \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) Struktur für die Kommunikation mit dem Server angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fb398-140">The service proxy provides no security guarantees beyond those specified in the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure used to communicate with the server.</span></span>
-   <span data-ttu-id="fb398-141">Achten Sie darauf, wenn Sie die Standardwerte für nach [richten](message.md) und [Kanäle](channel.md) auf dem Dienst Proxy ändern.</span><span class="sxs-lookup"><span data-stu-id="fb398-141">Take care when you modifying [message](message.md) and [channel](channel.md) defaults on the service proxy.</span></span> <span data-ttu-id="fb398-142">Lesen Sie die Sicherheitsüberlegungen in Bezug auf Nachrichten und Kanäle, bevor Sie die zugehörigen Eigenschaften ändern.</span><span class="sxs-lookup"><span data-stu-id="fb398-142">Read the security considerations associated with messages and channels before you modify any of the related properties.</span></span>
-   <span data-ttu-id="fb398-143">Der Dienst Proxy verschlüsselt alle Anmelde Informationen, die er im Arbeitsspeicher speichert.</span><span class="sxs-lookup"><span data-stu-id="fb398-143">Service proxy encrypts all credentials that it keeps in memory.</span></span>

<span data-ttu-id="fb398-144">Die folgenden API-Elemente beziehen sich auf Dienst Proxys.</span><span class="sxs-lookup"><span data-stu-id="fb398-144">The following API elements relate to service proxies.</span></span>

| <span data-ttu-id="fb398-145">Rückruf</span><span class="sxs-lookup"><span data-stu-id="fb398-145">Callback</span></span>                                                          | <span data-ttu-id="fb398-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb398-146">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb398-147">**WS- \_ Proxy \_ Nachrichten \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="fb398-147">**WS\_PROXY\_MESSAGE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | <span data-ttu-id="fb398-148">Wird aufgerufen, wenn die Header der Eingabe Nachricht über gesendet werden oder wenn ein Ausgabe Nachrichten Header soeben empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="fb398-148">Invoked when the headers of the input message are about to be sent through or when an output message headers are just received.</span></span> |



 



| <span data-ttu-id="fb398-149">Enumeration</span><span class="sxs-lookup"><span data-stu-id="fb398-149">Enumeration</span></span>                                                 | <span data-ttu-id="fb398-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb398-150">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb398-151">**WS- \_ Aufrufe- \_ Eigenschaften- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="fb398-151">**WS\_CALL\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | <span data-ttu-id="fb398-152">Listet optionale Parameter zum Konfigurieren eines Aufrufens für einen Client seitigen Dienst Vorgang auf.</span><span class="sxs-lookup"><span data-stu-id="fb398-152">Enumerates optional parameters for configuring a call on a client side service operation.</span></span> |
| [<span data-ttu-id="fb398-153">**WS- \_ Proxy- \_ Eigenschaften- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="fb398-153">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | <span data-ttu-id="fb398-154">Listet optionale Parameter zum Konfigurieren des Dienst Proxys auf.</span><span class="sxs-lookup"><span data-stu-id="fb398-154">Enumerates optional parameters for configuring the service proxy.</span></span>                         |
| [<span data-ttu-id="fb398-155">**WS- \_ Dienst \_ Proxy \_ Status**</span><span class="sxs-lookup"><span data-stu-id="fb398-155">**WS\_SERVICE\_PROXY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | <span data-ttu-id="fb398-156">Der Status des Dienst Proxys.</span><span class="sxs-lookup"><span data-stu-id="fb398-156">The state of the service proxy.</span></span>                                                           |



 



| <span data-ttu-id="fb398-157">Funktion</span><span class="sxs-lookup"><span data-stu-id="fb398-157">Function</span></span>                                                       | <span data-ttu-id="fb398-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb398-158">Description</span></span>                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="fb398-159">**Wsabandoncall**</span><span class="sxs-lookup"><span data-stu-id="fb398-159">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | <span data-ttu-id="fb398-160">Bricht einen angegebenen-Rückruf für einen angegebenen Dienst Proxy ab.</span><span class="sxs-lookup"><span data-stu-id="fb398-160">Abandons a specified call on a specified service proxy.</span></span>                           |
| [<span data-ttu-id="fb398-161">**Wsabortserviceproxy**</span><span class="sxs-lookup"><span data-stu-id="fb398-161">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | <span data-ttu-id="fb398-162">Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Dienst Proxy ab.</span><span class="sxs-lookup"><span data-stu-id="fb398-162">Cancels all pending input and output on a specified service proxy.</span></span>                |
| [<span data-ttu-id="fb398-163">**Wscall**</span><span class="sxs-lookup"><span data-stu-id="fb398-163">**WsCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | <span data-ttu-id="fb398-164">Nur intern.</span><span class="sxs-lookup"><span data-stu-id="fb398-164">Internal only.</span></span> <span data-ttu-id="fb398-165">Serialisiert Argumente in eine Nachricht und sendet Sie über den Kanal.</span><span class="sxs-lookup"><span data-stu-id="fb398-165">Serializes arguments into a message and sends it over the channel.</span></span> |
| [<span data-ttu-id="fb398-166">**Wscloseserviceproxy**</span><span class="sxs-lookup"><span data-stu-id="fb398-166">**WsCloseServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | <span data-ttu-id="fb398-167">Schließt einen Dienst Proxy für die Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="fb398-167">Closes a service proxy for communication.</span></span>                                         |
| [<span data-ttu-id="fb398-168">**Wscreateserviceproxy**</span><span class="sxs-lookup"><span data-stu-id="fb398-168">**WsCreateServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | <span data-ttu-id="fb398-169">Erstellt einen Dienst Proxy.</span><span class="sxs-lookup"><span data-stu-id="fb398-169">Creates a service proxy.</span></span>                                                          |
| [<span data-ttu-id="fb398-170">**Wsfreeserviceproxy**</span><span class="sxs-lookup"><span data-stu-id="fb398-170">**WsFreeServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | <span data-ttu-id="fb398-171">Gibt den einem Dienst Proxy zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="fb398-171">Releases the memory associated with a service proxy.</span></span>                              |
| [<span data-ttu-id="fb398-172">**Wsgetserviceproxyproperty**</span><span class="sxs-lookup"><span data-stu-id="fb398-172">**WsGetServiceProxyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | <span data-ttu-id="fb398-173">Ruft eine angegebene Dienst Proxy Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="fb398-173">Retrieves a specified service proxy property.</span></span>                                     |
| [<span data-ttu-id="fb398-174">**Wsopeinserviceproxy**</span><span class="sxs-lookup"><span data-stu-id="fb398-174">**WsOpenServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | <span data-ttu-id="fb398-175">Öffnet einen Dienst Proxy für einen Dienst Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="fb398-175">Opens a service proxy to a service endpoint.</span></span>                                      |
| [<span data-ttu-id="fb398-176">**Wsresetserviceproxy**</span><span class="sxs-lookup"><span data-stu-id="fb398-176">**WsResetServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | <span data-ttu-id="fb398-177">Setzt den Dienst Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="fb398-177">Resets service proxy.</span></span>                                                             |



 



| <span data-ttu-id="fb398-178">Handle</span><span class="sxs-lookup"><span data-stu-id="fb398-178">Handle</span></span>                                     | <span data-ttu-id="fb398-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb398-179">Description</span></span>                                       |
|--------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="fb398-180">WS- \_ Dienst \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="fb398-180">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md) | <span data-ttu-id="fb398-181">Ein nicht transparenter Typ, der zum Verweisen auf einen Dienst Proxy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb398-181">An opaque type used to reference a service proxy.</span></span> |



 



| <span data-ttu-id="fb398-182">Struktur</span><span class="sxs-lookup"><span data-stu-id="fb398-182">Structure</span></span>                                         | <span data-ttu-id="fb398-183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb398-183">Description</span></span>                 |
|---------------------------------------------------|-----------------------------|
| [<span data-ttu-id="fb398-184">**WS \_ - \_ aufrufeigenschaft**</span><span class="sxs-lookup"><span data-stu-id="fb398-184">**WS\_CALL\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | <span data-ttu-id="fb398-185">Gibt eine-aufrufeigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="fb398-185">Specifies a call property.</span></span>  |
| <span data-ttu-id="fb398-186">[**WS \_ Proxy- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span><span class="sxs-lookup"><span data-stu-id="fb398-186">[**WS\_PROXY\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span></span> | <span data-ttu-id="fb398-187">Gibt eine Proxy Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="fb398-187">Specifies a proxy property.</span></span> |



 

 

 




