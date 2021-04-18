---
title: Dienst Host
description: Der Dienst Host ist die Laufzeitumgebung zum Hosten eines Diensts in einem Prozess.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Dienst Host-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106371818"
---
# <a name="service-host"></a><span data-ttu-id="178ca-106">Dienst Host</span><span class="sxs-lookup"><span data-stu-id="178ca-106">Service Host</span></span>

<span data-ttu-id="178ca-107">Der Dienst Host ist die Laufzeitumgebung zum Hosten eines Diensts in einem Prozess.</span><span class="sxs-lookup"><span data-stu-id="178ca-107">The service host is the runtime environment for hosting a service within a process.</span></span>


<span data-ttu-id="178ca-108">Ein Dienst kann einen oder mehrere Endpunkte innerhalb eines Dienst Hosts konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="178ca-108">A service can configure one or more endpoints inside a service host.</span></span>

![Diagramm, das die Struktur eines Dienst Hosts mit einem Dienst Endpunkt anzeigt.](images/servicehost.png)

## <a name="creating-a-service-host"></a><span data-ttu-id="178ca-110">Erstellen eines Dienst Hosts</span><span class="sxs-lookup"><span data-stu-id="178ca-110">Creating a service host</span></span>

<span data-ttu-id="178ca-111">Vor dem Erstellen eines Dienst Hosts muss ein Dienst seine Endpunkte definieren.</span><span class="sxs-lookup"><span data-stu-id="178ca-111">Before creating a service host, a service needs to define its endpoints.</span></span> <span data-ttu-id="178ca-112">Ein Endpunkt im Dienst Host wird in der [**WS- \_ dienstend \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) Punkt Struktur angegeben und durch die folgenden Informationen definiert:</span><span class="sxs-lookup"><span data-stu-id="178ca-112">An endpoint in service host is specified in the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structure and it is defined by the following information:</span></span>

-   <span data-ttu-id="178ca-113">Eine Adresse, bei der es sich um den physischen URI handelt, auf dem der Dienst gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="178ca-113">An address, which is the physical URI on which the service will be hosted.</span></span>
-   <span data-ttu-id="178ca-114">Eine [**WS \_ - \_ Kanaltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) -Struktur, die den Typ des zugrunde liegenden Kanals für den Endpunkt angibt.</span><span class="sxs-lookup"><span data-stu-id="178ca-114">A [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) structure that specifies the type of the underlying channel for the endpoint.</span></span>
-   <span data-ttu-id="178ca-115">Eine [**WS- \_ Kanal \_ Bindungs**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) Struktur, die die Bindung des Kanals angibt.</span><span class="sxs-lookup"><span data-stu-id="178ca-115">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) structure that specifies the binding of the channel.</span></span>
-   <span data-ttu-id="178ca-116">Eine [**WS- \_ Sicherheits \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) Struktur, die die Sicherheits Beschreibung für den Endpunkt enthält.</span><span class="sxs-lookup"><span data-stu-id="178ca-116">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure that contains the security description for the endpoint.</span></span>
-   <span data-ttu-id="178ca-117">Eine [**WS- \_ Dienst \_ Vertrags**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) Struktur, die den [Dienstvertrag](contract.md) für den Endpunkt darstellt.</span><span class="sxs-lookup"><span data-stu-id="178ca-117">A [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure that represents the [service contract](contract.md) for the endpoint.</span></span>
-   <span data-ttu-id="178ca-118">Eine [**WS- \_ Dienst- \_ Sicherheits \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) Struktur, die eine Autorisierungs Rückruffunktion für den Endpunkt angibt.</span><span class="sxs-lookup"><span data-stu-id="178ca-118">A [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) structure that specifies an authorization callback function for the endpoint.</span></span>
-   <span data-ttu-id="178ca-119">Eine Eigenschaften Struktur des [**WS- \_ Dienst \_ Endpunkts \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) , die ein Array von dienstend Punkt Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="178ca-119">A [**WS\_SERVICE\_ENDPOINT\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) structure that contains an array of service endpoint properties.</span></span>

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

<span data-ttu-id="178ca-120">Für SOAP über UDP werden nur unidirektionale Verträge unterstützt, die durch die [**WS- \_ UDP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in der **WS- \_ \_ channelbindungsenumeration** dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="178ca-120">Only one-way contracts are supported for SOAP over UDP, represented by [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in the **WS\_CHANNEL\_BINDING** enumeration.</span></span>

<span data-ttu-id="178ca-121">Nachdem ein Endpunkt definiert wurde, kann er an die [**wscreateservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) -Funktion übergeben werden, die ein Array von Zeigern auf [**WS- \_ dienstend \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) Punkt Strukturen annimmt.</span><span class="sxs-lookup"><span data-stu-id="178ca-121">After an endpoint is defined, it can be passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function, which takes an array of pointers to [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures.</span></span>

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

<span data-ttu-id="178ca-122">Eine Anwendung kann optional ein Array von [**Dienst Eigenschaften**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) für [**wscreateservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) bereitstellen, um benutzerdefinierte Einstellungen auf dem Dienst Host zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="178ca-122">An application can optionally provide an array of [**service properties**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) to [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) to configure custom settings on the service host.</span></span>

<span data-ttu-id="178ca-123">Eine Anwendung öffnet den Dienst Host, um mit der Annahme von Client Anforderungen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="178ca-123">An application opens the service host to start accepting client requests.</span></span>

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="178ca-124">Nach dem Öffnen des Dienst Hosts kann die Anwendung ihn schließen, wenn keine weiteren Vorgänge vorhanden sind, die dies erfordern.</span><span class="sxs-lookup"><span data-stu-id="178ca-124">After opening the service host, the application can close it if there are no more operations that require it.</span></span> <span data-ttu-id="178ca-125">Beachten Sie, dass dadurch keine Ressourcen freigegeben werden und dass Sie mit einem nachfolgenden Aufrufen von [**wsresetservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)erneut geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="178ca-125">Note that this does not release its resources, and that it can be reopened with a subsequent call to [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span></span>

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="178ca-126">Nach dem Schließen des Dienst Hosts kann eine Anwendung den Dienst Host für die Wiederverwendung zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="178ca-126">After closing the service host, an application may reset the service host for reuse.</span></span>

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

<span data-ttu-id="178ca-127">Wenn die Anwendung mit dem Dienst Host ausgeführt wird, können die Ressourcen, die dem Dienst Host zugeordnet sind, durch Aufrufen der [**wsfreeservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) -Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="178ca-127">When the application is done with the service host it can free the resources associated with the service host by calling the [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) function.</span></span> <span data-ttu-id="178ca-128">Beachten Sie, dass [**wscloseservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) aufgerufen werden muss, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="178ca-128">Note that [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) must be called before calling this function.</span></span>

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

<span data-ttu-id="178ca-129">Informationen zum Anfügen eines benutzerdefinierten Zustands an den Dienst Host finden Sie unter [Benutzer Host Status](user-host-state.md) .</span><span class="sxs-lookup"><span data-stu-id="178ca-129">For information on attaching a custom state to the service host, see [User Host State](user-host-state.md)</span></span>

<span data-ttu-id="178ca-130">Informationen zur Autorisierung in einem Dienst Host für einen bestimmten Endpunkt finden Sie unter [Dienst Autorisierung](service-authorization.md).</span><span class="sxs-lookup"><span data-stu-id="178ca-130">For information on authorization in a service host for a given endpoint, see [Service Authorization](service-authorization.md).</span></span>

<span data-ttu-id="178ca-131">Weitere Informationen zum Implementieren von Dienst Vorgängen und Dienstverträgen für einen Dienst finden Sie in den Themen zu [Dienst Vorgängen](server-side-service-operations.md) und [Dienst](contract.md)Verträgen.</span><span class="sxs-lookup"><span data-stu-id="178ca-131">For iinformation on implementing service operations and service contracts for a service, see the [service operations](server-side-service-operations.md) and [service contract](contract.md)topics.</span></span>

## <a name="security"></a><span data-ttu-id="178ca-132">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="178ca-132">Security</span></span>

<span data-ttu-id="178ca-133">Eine Anwendung kann die folgenden Eigenschaften verwenden, um die Menge der Ressourcen zu steuern, die der Dienst Host für die Anwendung bereitstellt:</span><span class="sxs-lookup"><span data-stu-id="178ca-133">An application can use the followin properties to control the amount of resources the service host allocates on behalf of the application:</span></span>

-   <span data-ttu-id="178ca-134">[**WS \_ Dienst \_ Endpunkt \_ Eigenschaft \_ Max. \_ Annahme von \_ Kanälen**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="178ca-134">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_ACCEPTING\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="178ca-135">[**WS \_ maximale Parallelität der Dienst \_ Endpunkt \_ Eigenschaft \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="178ca-135">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CONCURRENCY**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="178ca-136">[**WS \_ \_ \_ \_ Maximale \_ Kanäle für Dienst Endpunkt Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="178ca-136">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="178ca-137">[**WS \_ \_ \_ \_ \_ \_ Maximale \_ Größe für den eigenschaftenheap des Dienst Endpunkts**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)</span><span class="sxs-lookup"><span data-stu-id="178ca-137">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_BODY\_HEAP\_MAX\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="178ca-138">[**WS \_ \_Maximale Anzahl \_ von \_ \_ aufrufspooleigenschaften \_ \_ für Dienst Endpunkt**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="178ca-138">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CALL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="178ca-139">[**WS \_ \_ \_ \_ Maximale \_ \_ \_ channelpoolgröße des Dienst Endpunkts**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span><span class="sxs-lookup"><span data-stu-id="178ca-139">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNEL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span></span>

<span data-ttu-id="178ca-140">Für jede dieser Eigenschaften werden sichere Standardwerte ausgewählt. eine Anwendung muss sorgfältig sein, wenn Sie diese Eigenschaften ändern möchte.</span><span class="sxs-lookup"><span data-stu-id="178ca-140">Secure defaults are chosen for each of these properties, an application must be careful if it wishes to modify these properties.</span></span> <span data-ttu-id="178ca-141">Zusätzlich zu den oben erwähnten Eigenschaften können auch [Kanal](channel.md)-, [Listener](listener.md) -und [Nachrichten](message.md) spezifische Eigenschaften von der Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="178ca-141">Beyond the above-mentioned properties, [channel](channel.md), [listener](listener.md) and [message](message.md) specific properties can also be modified by the application.</span></span> <span data-ttu-id="178ca-142">Beachten Sie die Sicherheitsüberlegungen dieser Komponenten, bevor Sie diese Einstellungen ändern.</span><span class="sxs-lookup"><span data-stu-id="178ca-142">Refer to the security considerations of these components before modifying any of these settings.</span></span>

<span data-ttu-id="178ca-143">Außerdem sollten die folgenden Überlegungen zum Anwendungs Entwurf sorgfältig ausgewertet werden, wenn die wwsapi-Dienst Host-API verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="178ca-143">In addition, the following application design considerations should be carefully evaluated when using WWSAPI service host API:</span></span>

-   <span data-ttu-id="178ca-144">Bei der Verwendung von Mex sollten Anwendungen darauf achten, keine sensiblen Daten offenzulegen.</span><span class="sxs-lookup"><span data-stu-id="178ca-144">When using MEX, applications should be careful not to disclose any sensitive data.</span></span> <span data-ttu-id="178ca-145">Wenn die Art der Daten, die durch MEX verfügbar gemacht werden, vertraulich ist, kann die Anwendung den MEX-Endpunkt mit einer sicheren Bindung konfigurieren, die mindestens eine Authentifizierung erfordert, und die Autorisierung als Teil des Endpunkts mithilfe des [**WS- \_ Dienst \_ Sicherheits \_ Rückrufs**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)implementieren.</span><span class="sxs-lookup"><span data-stu-id="178ca-145">As a mitigation, if the nature of the data being exposed through MEX is sensitive, applications may choose to configure the MEX endpoint with a secure binding requiring authentication at the very least and implement authorization as part of the endpoint using the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="178ca-146">In der Standardeinstellung werden umfangreiche Fehlerinformationen durch Fehler auf Dienst Host über die [**WS- \_ Dienst \_ Eigenschaft \_ Fehler \_ Offenlegungs**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) Eigenschaft deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="178ca-146">By default rich error information through faults is disabled on service host by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span> <span data-ttu-id="178ca-147">Es ist nach dem Ermessen der Anwendung, umfangreiche Fehlerinformationen als Teil des Fehlers zu senden.</span><span class="sxs-lookup"><span data-stu-id="178ca-147">It is upon the discretion of the application to send rich error information as part of the fault.</span></span> <span data-ttu-id="178ca-148">Dies kann jedoch zur Offenlegung von Informationen führen. Daher wird empfohlen, dass diese Einstellung nur für Debugszenarien geändert wird.</span><span class="sxs-lookup"><span data-stu-id="178ca-148">However, this can result in information disclosure and thus it is recommended that this setting is only changed for debugging scenarios.</span></span>
-   <span data-ttu-id="178ca-149">Neben der Überprüfung, die für das Basisprofil 2,0 und die XML-Serialisierung ausgeführt wird, führt der Dienst Host keine Überprüfung des Daten Inhalts aus, der als Teil der Dienst Vorgangs Parameter</span><span class="sxs-lookup"><span data-stu-id="178ca-149">Beyond validation performed for Basic Profile 2.0 and XML serialization, service host performs no validation on the data content received as part of service operation parameters.</span></span> <span data-ttu-id="178ca-150">Es liegt in der Verantwortung der Anwendung, alle Parameter Validierungen eigenständig auszuführen.</span><span class="sxs-lookup"><span data-stu-id="178ca-150">It is the responsibility of the application to perform all parameter validations on its own.</span></span>
-   <span data-ttu-id="178ca-151">Die Autorisierung ist nicht als Teil des Dienst Hosts implementiert.</span><span class="sxs-lookup"><span data-stu-id="178ca-151">Authorization is not implemented as part of service host.</span></span> <span data-ttu-id="178ca-152">Anwendungen können jedoch mithilfe der [**WS- \_ Sicherheits \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) und des [**WS- \_ Dienst \_ Sicherheits \_ Rückrufs**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)Ihr eigenes Autorisierungs Schema implementieren.</span><span class="sxs-lookup"><span data-stu-id="178ca-152">However, applications can implement their own authorization scheme using [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) and the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="178ca-153">Es liegt in der Verantwortung der Anwendung, sichere Bindungen für ihren Endpunkt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="178ca-153">It is the responsibility of the application to use secure bindings on its endpoint.</span></span> <span data-ttu-id="178ca-154">Der Dienst Host bietet keine Sicherheitsfunktionen, die über die Konfiguration des Endpunkts hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="178ca-154">Service host does not provide any security beyond what is configured on the endpoint.</span></span>

<span data-ttu-id="178ca-155">Die folgenden API-Elemente werden mit dem Dienst Host verwendet.</span><span class="sxs-lookup"><span data-stu-id="178ca-155">The following API elements are used with the service host.</span></span>

| <span data-ttu-id="178ca-156">Rückruf</span><span class="sxs-lookup"><span data-stu-id="178ca-156">Callback</span></span>                                                                             | <span data-ttu-id="178ca-157">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="178ca-157">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="178ca-158">**WS- \_ Dienst \_ Annahme- \_ Kanal \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="178ca-158">**WS\_SERVICE\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | <span data-ttu-id="178ca-159">Wird aufgerufen, wenn ein Kanal für einen Endpunkt Listener durch den Dienst Host akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="178ca-159">Invoked when a channel is accepted on an endpoint listener by the service host.</span></span> |
| [<span data-ttu-id="178ca-160">**WS- \_ Dienst- \_ Schluss \_ Kanal \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="178ca-160">**WS\_SERVICE\_CLOSE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | <span data-ttu-id="178ca-161">Wird aufgerufen, wenn ein Kanal an einem Endpunkt geschlossen oder abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="178ca-161">Invoked when a channel is closed or aborted on an endpoint.</span></span>                     |



 



| <span data-ttu-id="178ca-162">Enumeration</span><span class="sxs-lookup"><span data-stu-id="178ca-162">Enumeration</span></span>                                                                    | <span data-ttu-id="178ca-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="178ca-163">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="178ca-164">**Eigenschaften-ID für WS- \_ Dienst \_ Endpunkt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="178ca-164">**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | <span data-ttu-id="178ca-165">Optionale Parameter zum Konfigurieren eines [**WS- \_ Dienst \_ Endpunkts**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="178ca-165">Optional parameters for configuring a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span> |
| [<span data-ttu-id="178ca-166">**Status des WS- \_ Dienst \_ Hosts \_**</span><span class="sxs-lookup"><span data-stu-id="178ca-166">**WS\_SERVICE\_HOST\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | <span data-ttu-id="178ca-167">Die Zustände, in denen sich ein Dienst Host befinden kann.</span><span class="sxs-lookup"><span data-stu-id="178ca-167">The states that a service host can be in.</span></span>                                                   |
| [<span data-ttu-id="178ca-168">**WS- \_ Dienst- \_ Eigenschaften- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="178ca-168">**WS\_SERVICE\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | <span data-ttu-id="178ca-169">Optionale Parameter zum Konfigurieren des Dienst Hosts.</span><span class="sxs-lookup"><span data-stu-id="178ca-169">Optional parameters for configuring the service host.</span></span>                                       |



 



| <span data-ttu-id="178ca-170">Funktion</span><span class="sxs-lookup"><span data-stu-id="178ca-170">Function</span></span>                                                     | <span data-ttu-id="178ca-171">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="178ca-171">Description</span></span>                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="178ca-172">**Wsabortservicehost**</span><span class="sxs-lookup"><span data-stu-id="178ca-172">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | <span data-ttu-id="178ca-173">Unterbricht und beendet die aktuellen Vorgänge auf dem Dienst Host.</span><span class="sxs-lookup"><span data-stu-id="178ca-173">Interrupts and discontinues current operations on the service host.</span></span>                          |
| [<span data-ttu-id="178ca-174">**Wscloseservicehost**</span><span class="sxs-lookup"><span data-stu-id="178ca-174">**WsCloseServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | <span data-ttu-id="178ca-175">Schließt alle Listener, sodass keine neuen Kanäle vom Client akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="178ca-175">Closes all listeners so that no new channels are accepted from the client.</span></span>                   |
| [<span data-ttu-id="178ca-176">**Wscreateservicehost**</span><span class="sxs-lookup"><span data-stu-id="178ca-176">**WsCreateServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | <span data-ttu-id="178ca-177">Erstellt einen Dienst Host.</span><span class="sxs-lookup"><span data-stu-id="178ca-177">Creates a service host.</span></span>                                                                      |
| [<span data-ttu-id="178ca-178">**Wsfreeservicehost**</span><span class="sxs-lookup"><span data-stu-id="178ca-178">**WsFreeServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | <span data-ttu-id="178ca-179">Gibt den einem Dienst Host Objekt zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="178ca-179">Releases the memory associated with a service host object.</span></span>                                   |
| [<span data-ttu-id="178ca-180">**Wsgetservicehostproperty**</span><span class="sxs-lookup"><span data-stu-id="178ca-180">**WsGetServiceHostProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | <span data-ttu-id="178ca-181">Ruft eine angegebene Dienst Host Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="178ca-181">Retrieves a specified Service Host property.</span></span>                                                 |
| [<span data-ttu-id="178ca-182">**Wsopeinservicehost**</span><span class="sxs-lookup"><span data-stu-id="178ca-182">**WsOpenServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | <span data-ttu-id="178ca-183">Öffnet einen Dienst Host für die Kommunikation und startet die Listener für alle Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="178ca-183">Opens a service host for communication and starts the listeners on all the endpoints.</span></span>        |
| [<span data-ttu-id="178ca-184">**Wsresetservicehost**</span><span class="sxs-lookup"><span data-stu-id="178ca-184">**WsResetServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | <span data-ttu-id="178ca-185">Setzt den Dienst Host für die Wiederverwendung zurück und setzt den zugrunde liegenden Kanal und die Listener für die Wiederverwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="178ca-185">Resets the service host for reuse and resets the underlying channel and listeners for reuse.</span></span> |



 



| <span data-ttu-id="178ca-186">Handle</span><span class="sxs-lookup"><span data-stu-id="178ca-186">Handle</span></span>                                       | <span data-ttu-id="178ca-187">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="178ca-187">Description</span></span>                                      |
|----------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="178ca-188">**WS- \_ Dienst \_ Host**</span><span class="sxs-lookup"><span data-stu-id="178ca-188">**WS\_SERVICE\_HOST**</span></span>](ws-service-host.md) | <span data-ttu-id="178ca-189">Ein nicht transparenter Typ, der zum Verweisen auf einen Dienst Host verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="178ca-189">An opaque type used to reference a service host.</span></span> |



 



| <span data-ttu-id="178ca-190">Struktur</span><span class="sxs-lookup"><span data-stu-id="178ca-190">Structure</span></span>                                                                              | <span data-ttu-id="178ca-191">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="178ca-191">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="178ca-192">**WS- \_ Dienst \_ Endpunkt**</span><span class="sxs-lookup"><span data-stu-id="178ca-192">**WS\_SERVICE\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | <span data-ttu-id="178ca-193">Stellt einen einzelnen Endpunkt auf einem Dienst Host dar.</span><span class="sxs-lookup"><span data-stu-id="178ca-193">Represents an individual endpoint on a service host.</span></span>                            |
| [<span data-ttu-id="178ca-194">**Eigenschaft des WS- \_ Dienst \_ Endpunkts \_**</span><span class="sxs-lookup"><span data-stu-id="178ca-194">**WS\_SERVICE\_ENDPOINT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | <span data-ttu-id="178ca-195">Gibt eine Dienst spezifische Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="178ca-195">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="178ca-196">**WS- \_ Dienst \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="178ca-196">**WS\_SERVICE\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | <span data-ttu-id="178ca-197">Gibt eine Dienst spezifische Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="178ca-197">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="178ca-198">**WS- \_ Dienst \_ Eigenschaft \_ Accept \_ Callback**</span><span class="sxs-lookup"><span data-stu-id="178ca-198">**WS\_SERVICE\_PROPERTY\_ACCEPT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | <span data-ttu-id="178ca-199">Gibt den Rückruf an, der aufgerufen wird, wenn ein Kanal erfolgreich akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="178ca-199">Specifies the callback which is called when a channel is successfully accepted.</span></span> |
| [<span data-ttu-id="178ca-200">**Rückruf für die WS- \_ Dienst \_ Eigenschaft \_ Close \_**</span><span class="sxs-lookup"><span data-stu-id="178ca-200">**WS\_SERVICE\_PROPERTY\_CLOSE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | <span data-ttu-id="178ca-201">Gibt den Rückruf an, der aufgerufen wird, wenn ein Kanal im Begriff ist, geschlossen zu werden.</span><span class="sxs-lookup"><span data-stu-id="178ca-201">Specifies the callback which is called when a channel is about to be closed.</span></span>    |



 

 

 




