---
title: Dienstmetadaten
description: Der wwsapi-Dienst Host unterstützt WS-MetadataExchange für seine Endpunkte.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Dienst Metadaten Native Webdienste
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474679"
---
# <a name="service-metadata"></a><span data-ttu-id="0c4b7-106">Dienstmetadaten</span><span class="sxs-lookup"><span data-stu-id="0c4b7-106">Service Metadata</span></span>

<span data-ttu-id="0c4b7-107">Der wwsapi-Dienst Host unterstützt WS-MetadataExchange für seine Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-107">The WWSAPI service host supports WS-MetadataExchange for its endpoints.</span></span> <span data-ttu-id="0c4b7-108">Sie aktivieren einen solchen Metadatenaustausch auf dem Dienst Host mit den folgenden Schritten:</span><span class="sxs-lookup"><span data-stu-id="0c4b7-108">You enable such metadata exchange on the service host with the following steps:</span></span>

-   <span data-ttu-id="0c4b7-109">Geben Sie Metadatendokumente in der [**WS- \_ \_ dienstmetadateneigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) auf dem [WS- \_ Dienst \_ Host](ws-service-host.md)an.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-109">Specify metadata documents in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="0c4b7-110">Geben Sie den Dienstnamen in der [**WS- \_ \_ dienstmetadateneigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) auf dem [WS- \_ Dienst \_ Host](ws-service-host.md)an.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-110">Specify the service name in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="0c4b7-111">Geben Sie den Port für einzelne Endpunkte an, indem Sie die Eigenschaft [**\_ \_ \_ \_ Metadateneigenschaft des WS-Dienst Endpunkts**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) für den [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)verwenden</span><span class="sxs-lookup"><span data-stu-id="0c4b7-111">Specify the port for individual endpoints by using the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>
-   <span data-ttu-id="0c4b7-112">Aktivieren Sie eine oder mehrere [**WS- \_ dienstend \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) Punkt Strukturen, um die WS-MetadataExchange Anforderungen zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-112">Enable one or more [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures to service the WS-MetadataExchange requests.</span></span>
-   <span data-ttu-id="0c4b7-113">Optional können Sie **das \_ URL \_ - \_ \_ \_ \_ \_ Suffix für die WS-dienstend Punkt Eigenschaft** in der [**Eigenschaften-ID des WS- \_ Dienst \_ Endpunkts \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) angeben, um Ws-MetadataExchange Anforderungen an eine bestimmte Adresse zu warten.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-113">Optionally, specify **WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA\_EXCHANGE\_URL\_SUFFIX** in the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) enumeration for servicing Ws-MetadataExchange requests on a specific address.</span></span>


<span data-ttu-id="0c4b7-114">Angeben von Metadatendokumenten/Dienstnamen auf dem Dienst Host</span><span class="sxs-lookup"><span data-stu-id="0c4b7-114">Specifying Metadata documents / Service name on the Service Host</span></span>

<span data-ttu-id="0c4b7-115">Der erste Schritt besteht darin, die Metadatendokumente auf dem Dienst Host anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-115">The first step is to specify the metadata documents on the service host.</span></span> <span data-ttu-id="0c4b7-116">Zu diesem Zweck erfassen Sie die einzelnen Dokumente als Array von WS \_ \_ -XML \* -Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-116">Do this by gathering the individual documents as an array of WS\_XML\_STRING\*'s.</span></span> <span data-ttu-id="0c4b7-117">Diese Zeichen folgen können XML-Schema, WSDL oder WS-Policy Dokument sein.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-117">These strings can be XML Schema, WSDL or WS-Policy document.</span></span> <span data-ttu-id="0c4b7-118">Dies wird durch die Eigenschaft [**\_ \_ \_ Metadateneigenschaft der WS-Dienst Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) angegeben.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-118">This is specified through the [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span>

<span data-ttu-id="0c4b7-119">Optional kann eine Anwendung auch den Dienstnamen und den Namespace als Teil der WS- [**\_ Dienst \_ Metadaten**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)angeben.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-119">Optionally, an application can also specify the service name and namespace as part of the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span></span> <span data-ttu-id="0c4b7-120">Wenn das Metadatendokument das Dienst Element für den angegebenen Dienstnamen nicht angibt, generiert das Dienstmodell ein Dienst Element mit den entsprechenden WSDL-Ports für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-120">If the metadata document does not specify the service element for the given service name, the service model will generate a service element with the corresponding WSDL ports for the service.</span></span>

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

<span data-ttu-id="0c4b7-121">Beachten Sie, dass keine Überprüfung der einzelnen Metadatendokumente für die Dokumente ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-121">Note that no verification of the individual metadata documents will be performed on the documents.</span></span> <span data-ttu-id="0c4b7-122">Es liegt in der Verantwortung der Anwendung, den Inhalt der Dokumente zu überprüfen und sicherzustellen, dass alle Import Pfade relativ angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-122">It is the responsiblity of the application to validate contents of the documents and ensure that all the imports paths are relatively specified.</span></span>

<span data-ttu-id="0c4b7-123">Der angegebene Namespace wird verwendet, um das Dokument zu suchen, in dem das Dienst Element vom Dienst Host hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-123">The namespace specified is used to locate the document in which the service element will be added by the service host.</span></span>

<span data-ttu-id="0c4b7-124">Hinzufügen des Dienst Elements zum WSDL-Dokument</span><span class="sxs-lookup"><span data-stu-id="0c4b7-124">Addition of service element to the WSDL document</span></span>

<span data-ttu-id="0c4b7-125">Der Dienst Host stellt eine Funktion für die Anwendung bereit, um in Ihrem Namen ein Dienst Element hinzuzufügen, sofern noch nicht geschehen.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-125">The service host provides facility for the application to add a service element on its behalf if one is not already specified.</span></span> <span data-ttu-id="0c4b7-126">Um dieses Verhalten zu aktivieren, muss eine Anwendung die Felder serivcename und servicens in der [**WS \_ - \_ dienstmetadatenstruktur**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) angeben.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-126">In order to enable this behavior an application must specify serivceName and serviceNs fields on the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) structure.</span></span> <span data-ttu-id="0c4b7-127">Wenn Service Name und servicens beide **null** sind, wird dem WSDL-Dokument kein Dienst Element hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-127">If serviceName and serviceNs are both **NULL** no service element is added to the WSDL document.</span></span> <span data-ttu-id="0c4b7-128">Beide werden verwendet, um Dokumente zu identifizieren, in denen das Service Element hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-128">Both these are used to identify document in which the serviceElement is going to be added.</span></span>

<span data-ttu-id="0c4b7-129">Wenn die Eigenschaft [**\_ \_ \_ Metadateneigenschaft der WS-Dienst Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) nicht angegeben ist, findet kein Metadatenaustausch auf dem Dienst Host statt.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-129">If [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property is not specified no metadata exhange will take place on the service host.</span></span>

<span data-ttu-id="0c4b7-130">Angeben des Ports auf dem WS- \_ Dienst \_ Endpunkt</span><span class="sxs-lookup"><span data-stu-id="0c4b7-130">Specifying the port on the WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="0c4b7-131">Damit ein [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) als Port innerhalb des Dienst Elements im WSDL-Dokument verfügbar ist, muss die Anwendung für die [**\_ \_ \_ Eigenschaft \_ Metadateneigenschaft des WS-Dienst Endpunkts**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) angeben.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-131">For a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) to be available as a port inside the service element in the WSDL document, the application must specify [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on it.</span></span>

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

<span data-ttu-id="0c4b7-132">Es wird davon ausgegangen, dass der Verweis auf den Bindungs Namen und-Namespace in den Dokumenten vorhanden ist, die auf dem Dienst Host als Teil der WS- \_ Dienst \_ Eigenschafts Metadaten angegeben sind \_ .</span><span class="sxs-lookup"><span data-stu-id="0c4b7-132">It is assumed that the reference to the binding name and namespace exists in the documents specified on the service host as part of WS\_SERVICE\_PROPERTY\_METADATA.</span></span> <span data-ttu-id="0c4b7-133">Die Laufzeit überprüft dies im Auftrag der Anwendung nicht.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-133">The runtime does not verify this on behalf of the application.</span></span>

<span data-ttu-id="0c4b7-134">Aktivieren der WS-MetadataExchange Wartung auf dem WS- \_ Dienst \_ Endpunkt</span><span class="sxs-lookup"><span data-stu-id="0c4b7-134">Enable WS-MetadataExchange servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="0c4b7-135">Damit WS-MetadataExchange Anforderungen verarbeitet werden können, muss der Dienst Host mindestens einen Endpunkt für die Wartung WS-MetadataExchange Anforderungen aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-135">In order to service WS-MetadataExchange requests,the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="0c4b7-136">Dies erfolgt durch Festlegen der entsprechenden Version für WS-MetadataExchange auf dem [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="0c4b7-136">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="0c4b7-137">Aktivieren von HTTP Get-Wartung auf dem WS- \_ Dienst \_ Endpunkt</span><span class="sxs-lookup"><span data-stu-id="0c4b7-137">Enable HTTP GET servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="0c4b7-138">Um servicehttp Get-Anforderungen zu verarbeiten, muss der Dienst Host mindestens einen Endpunkt haben, der für die Wartung WS-MetadataExchange Anforderungen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-138">In order to serviceHTTP GET requests, the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="0c4b7-139">Dies erfolgt durch Festlegen der entsprechenden Version für WS-MetadataExchange auf dem [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="0c4b7-139">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="0c4b7-140">Angeben von URL-Suffix für Ws-MetadataExchange Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c4b7-140">Specifying URL suffix for Ws-MetadataExchange requests</span></span>

<span data-ttu-id="0c4b7-141">Eine Anwendung kann optional nur das akzeptieren von Anforderungen für WS-MetadataExchange für einen bestimmten Pfad aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-141">An application can optionally enable only accepting requests for WS-MetadataExchange on a specific path.</span></span> <span data-ttu-id="0c4b7-142">Dies erfolgt durch Angabe eines Suffixes für den angegebenen WS- \_ Dienst \_ Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-142">This is done by specifying a suffix for the given WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="0c4b7-143">Dieses Suffix wird unverändert an die tatsächliche URL des WS- \_ Dienst \_ Endpunkts verkettet.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-143">This suffix is concatenated as-is to the actual URL for the WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="0c4b7-144">Die verketteten Zeichenfolge wird als übereinstimmende URL zum empfangenen ' to '-Header verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-144">The concatenated string is used as the matching URL to the 'to' header received.</span></span>

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

<span data-ttu-id="0c4b7-145">Die folgenden API-Elemente beziehen sich auf die Dienst Metada.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-145">The following API elements relate to service metada.</span></span>

| <span data-ttu-id="0c4b7-146">Enumeration</span><span class="sxs-lookup"><span data-stu-id="0c4b7-146">Enumeration</span></span>                                                       | <span data-ttu-id="0c4b7-147">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c4b7-147">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="0c4b7-148">**WS \_ - \_ metadatenaustauschtyp \_**</span><span class="sxs-lookup"><span data-stu-id="0c4b7-148">**WS\_METADATA\_EXCHANGE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | <span data-ttu-id="0c4b7-149">Aktiviert oder deaktiviert WS-MetadataExchange und HTTP Get-Wartung für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-149">Enables or disables WS-MetadataExchange and HTTP GET servicing on the endpoint.</span></span> |



 



| <span data-ttu-id="0c4b7-150">Struktur</span><span class="sxs-lookup"><span data-stu-id="0c4b7-150">Structure</span></span>                                                               | <span data-ttu-id="0c4b7-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c4b7-151">Description</span></span>                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="0c4b7-152">**Metadaten des WS- \_ Dienst \_ Endpunkts \_**</span><span class="sxs-lookup"><span data-stu-id="0c4b7-152">**WS\_SERVICE\_ENDPOINT\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | <span data-ttu-id="0c4b7-153">Stellt das Port-Element für den Endpunkt dar.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-153">Represents the port element for the endpoint.</span></span>                         |
| [<span data-ttu-id="0c4b7-154">**WS- \_ Dienst \_ Metadaten**</span><span class="sxs-lookup"><span data-stu-id="0c4b7-154">**WS\_SERVICE\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | <span data-ttu-id="0c4b7-155">Gibt das Array der dienstmetadatendokumente an.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-155">Specifies the service metadata documents array.</span></span>                       |
| [<span data-ttu-id="0c4b7-156">**WS \_ - \_ dienstmetadatendokument \_**</span><span class="sxs-lookup"><span data-stu-id="0c4b7-156">**WS\_SERVICE\_METADATA\_DOCUMENT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | <span data-ttu-id="0c4b7-157">Gibt die einzelnen Dokumente an, aus denen die Dienst Metadaten besteht.</span><span class="sxs-lookup"><span data-stu-id="0c4b7-157">Specifies the individual documents that make up the service metadata.</span></span> |



 

 

 




