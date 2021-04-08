---
title: Metadatenimport
description: Das wwsapi umfasst API-Elemente, die zum Verarbeiten von WSDL und Richtlinien von einem Endpunkt verwendet werden können, mit dem Ziel, Informationen zu extrahieren, die für die Kommunikation mit dem Endpunkt verwendet werden können.
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- Metadatenimport-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c36ffdf9bcbf0d63bdef473cc52cd4d545e5a3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734992"
---
# <a name="metadata-import"></a><span data-ttu-id="caf37-106">Metadatenimport</span><span class="sxs-lookup"><span data-stu-id="caf37-106">Metadata Import</span></span>

<span data-ttu-id="caf37-107">Das wwsapi umfasst API-Elemente, die zum Verarbeiten von WSDL und Richtlinien von einem Endpunkt verwendet werden können, mit dem Ziel, Informationen zu extrahieren, die für die Kommunikation mit dem Endpunkt verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="caf37-107">The WWSAPI includes API elements that can be used to process WSDL and Policy from an endpoint with the goal of extracting information that can be used to communicate with the endpoint.</span></span> <span data-ttu-id="caf37-108">Diese APIs werden in der Regel verwendet, wenn das vom Endpunkt unterstützte Kommunikationsprotokoll nicht bereits bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="caf37-108">These APIs are typically used when the communication protocol supported by the endpoint is not already known.</span></span>


<span data-ttu-id="caf37-109">Verwenden Sie die folgende Sequenz, um Metadaten zu verarbeiten:</span><span class="sxs-lookup"><span data-stu-id="caf37-109">Use the following sequence to process metadata:</span></span>

``` syntax
WsCreateMetadata    // create a metadata object

while there are metadata documents to add
{
    // retrieve the metadata document from it's location
    // (download, read from file, etc)

    // add the document to the metadata object
    WsReadMetadata

    // optionally query the metadata object for any missing documents
    WsGetMissingMetadataDocumentAddress?
}

// get the endpoints from the metadata object
WsGetMetadataEndpoints

for each endpoint
{            
    // examine the endpoint information to see if 
    // the endpoint is relevant for the particular scenario

    if the endpoint is relevant
    {
        // get the policy object from the endpoint

        // get the number of policy alternatives in the policy
        WsGetPolicyAlternativeCount

        for each policy alternative
        {
            // construct a policy constraints structure that specifies
            // what policy is acceptable and what information to extract
            // from the policy

            // see if the policy alternative matches the constraints
            WsMatchPolicyAlternative

            // if there is a match, then use it

            // if there is not a match, then it is also possible to 
            // try with a different constraint structure
        }
    }
}

// If reusing the metadata object for a different set of documents
WsResetMetadata? // reset metadata object, which removes all documents

WsFreeMetadata // free the metadata object
```

<span data-ttu-id="caf37-110">Informationen dazu, wie WSDL-und WS-Policy Assertionen der API entsprechen, finden Sie im Thema [metadatenzuordnung](metadata-mapping.md) .</span><span class="sxs-lookup"><span data-stu-id="caf37-110">for information about how WSDL and WS-Policy assertions correspond to the API, see the [Metadata Mapping](metadata-mapping.md) topic.</span></span>

## <a name="security"></a><span data-ttu-id="caf37-111">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="caf37-111">Security</span></span>

<span data-ttu-id="caf37-112">Die heruntergeladenen Metadaten sind nur so gut wie die Adresse, die zum Herunterladen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="caf37-112">The metadata downloaded is only as good as the address used to download it.</span></span> <span data-ttu-id="caf37-113">Eine Anwendung sollte sicherstellen, dass die Adresse von vertraut.</span><span class="sxs-lookup"><span data-stu-id="caf37-113">An application should ensure that is trusts the address.</span></span> <span data-ttu-id="caf37-114">Außerdem sollte eine Anwendung sicherstellen, dass Sie ein Sicherheitsprotokoll zum Herunterladen der Metadatendokumente verwendet, die keine Manipulation der Metadaten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="caf37-114">Also, an application should ensure that it uses a security protocol to download the metadata documents that does not allow tampering with the metadata.</span></span>

<span data-ttu-id="caf37-115">Eine Anwendung sollte die Adressen der Dienste überprüfen, die von den Metadaten verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="caf37-115">An application should inspect the addresses of the services exposed by the metadata.</span></span> <span data-ttu-id="caf37-116">Standardmäßig stellt die Laufzeit sicher, dass der Hostname des Diensts mit dem der ursprünglichen URL übereinstimmt, die zum Herunterladen der Metadaten verwendet wurde, aber die Anwendung möchte möglicherweise weitere Überprüfungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="caf37-116">By default, the runtime ensures that the host name of the service matches that of the original URL used to download the metadata, but the application may want to perform additional checks.</span></span> <span data-ttu-id="caf37-117">Eine Anwendung kann die Überprüfung des Host namens durch Überschreiben der Eigenschaft [**\_ \_ \_ \_ \_ Hostnamen Überprüfen der WS-Metadateneigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="caf37-117">An application can disable the host name verification by overwriting [**WS\_METADATA\_PROPERTY\_VERIFY\_HOST\_NAMES**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) property.</span></span> <span data-ttu-id="caf37-118">Wenn die standardmäßig durchgeführte Überprüfung des Host namens deaktiviert ist, muss sich die Anwendung vor den Metadatendokumenten schützen, die die Adresse eines Dienstanbieter von einer anderen Partei enthalten, der nicht auf andere Weise als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="caf37-118">If the hostname check that is done by default is disabled, the application will need to protect itself against the metadata documents containing the address of a service from a different party that it does not trust in some other way.</span></span>

<span data-ttu-id="caf37-119">Standardmäßig ist die maximale Menge an Arbeitsspeicher, die von der Metadatenlaufzeit verwendet wird, um die Metadaten zu deserialisieren und zu verarbeiten, 256 KB, und die maximale Anzahl von Dokumenten, die hinzugefügt werden können, ist 32.</span><span class="sxs-lookup"><span data-stu-id="caf37-119">By default, the maximum amount of memory used by the metadata runtime to deserialize and process the metadata is 256k, and the maximum number of documents that may be added is 32.</span></span> <span data-ttu-id="caf37-120">Diese Standardwerte können von den Eigenschaften [**\_ \_ \_ Heap \_ angeforderte \_ Größe des WS-metadateneigenschaftenheaps**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) und Eigenschaften für die **Eigenschaft " \_ \_ \_ Max \_** .</span><span class="sxs-lookup"><span data-stu-id="caf37-120">These default values can be overwritten by [**WS\_METADATA\_PROPERTY\_HEAP\_REQUESTED\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) and **WS\_METADATA\_PROPERTY\_MAX\_DOCUMENTS** properties.</span></span> <span data-ttu-id="caf37-121">Diese Begrenzungen dienen dazu, die Menge der Downloads einzuschränken und die Menge des belegten Arbeitsspeichers einzuschränken, um die Metadaten zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="caf37-121">These bounds are designed to limit the amount of downloads and limit the amount of memory allocated in order to accumulate the metadata.</span></span> <span data-ttu-id="caf37-122">Das Erhöhen dieser Werte kann zu einer übermäßigen Speicherauslastung, CPU-Auslastung oder Auslastung der Netzwerkbandbreite führen.</span><span class="sxs-lookup"><span data-stu-id="caf37-122">Increasing these values may lead to excessive memory usage, CPU usage, or network bandwidth consumption.</span></span> <span data-ttu-id="caf37-123">Beachten Sie, dass eine kleine Nachricht aufgrund der Erweiterung von Wörterbuch Zeichenfolgen im Binärformat zu einer viel größeren deserialisierten Form führen kann. Daher reicht die Verwendung von kleinen Nachrichten nicht aus, um die Speicher Belegung von Metadaten einzuschränken, wenn das Binärformat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="caf37-123">Note that due to expansion of dictionary strings in the binary format, a small message may lead to a much larger deserialized form, so relying on small messages to limit metadata memory allocation is not sufficient when using the binary format.</span></span>

<span data-ttu-id="caf37-124">Standardmäßig ist die maximale Anzahl von Richtlinien Alternativen 32, obwohl Sie von der [**WS- \_ Richtlinien \_ Eigenschaft \_ Max \_ alternatives**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) -Eigenschaft überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="caf37-124">By default, the maximum number of policy alternatives is 32, though it can be overwritten by [**WS\_POLICY\_PROPERTY\_MAX\_ALTERNATIVES**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) property.</span></span> <span data-ttu-id="caf37-125">Wenn eine Anwendung durch die einzelnen Alternativen sucht, die nach einer Entsprechung suchen, muss Sie möglicherweise alle alternativen durchsuchen, bevor eine Entsprechung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="caf37-125">If an application loops through each alternative looking for a match, it may need to search all alternatives before finding a match.</span></span> <span data-ttu-id="caf37-126">Das Erhöhen der maximalen Anzahl von Alternativen kann zu einer übermäßigen CPU-Auslastung führen.</span><span class="sxs-lookup"><span data-stu-id="caf37-126">Increasing the maximum number of alternatives may lead to excessive CPU utilization.</span></span>

<span data-ttu-id="caf37-127">Die folgenden Enumerationen sind Teil des metadatenimports:</span><span class="sxs-lookup"><span data-stu-id="caf37-127">The following enumerations are part of metadata import:</span></span>

-   [<span data-ttu-id="caf37-128">**ID der WS- \_ \_ Metadateneigenschaft \_**</span><span class="sxs-lookup"><span data-stu-id="caf37-128">**WS\_METADATA\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [<span data-ttu-id="caf37-129">**WS \_ - \_ metadatenstatus**</span><span class="sxs-lookup"><span data-stu-id="caf37-129">**WS\_METADATA\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [<span data-ttu-id="caf37-130">**WS \_ - \_ Richtlinien \_ Erweiterungstyp**</span><span class="sxs-lookup"><span data-stu-id="caf37-130">**WS\_POLICY\_EXTENSION\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [<span data-ttu-id="caf37-131">**WS- \_ Richtlinien \_ Eigenschaften- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="caf37-131">**WS\_POLICY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [<span data-ttu-id="caf37-132">**WS- \_ Richtlinien \_ Status**</span><span class="sxs-lookup"><span data-stu-id="caf37-132">**WS\_POLICY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [<span data-ttu-id="caf37-133">**Typ der WS- \_ \_ sicherheitsbindungs \_ Einschränkung \_**</span><span class="sxs-lookup"><span data-stu-id="caf37-133">**WS\_SECURITY\_BINDING\_CONSTRAINT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

<span data-ttu-id="caf37-134">Die folgenden Funktionen sind Teil des metadatenimports:</span><span class="sxs-lookup"><span data-stu-id="caf37-134">The following functions are part of metadata import:</span></span>

-   [<span data-ttu-id="caf37-135">**Wscreatemetadata**</span><span class="sxs-lookup"><span data-stu-id="caf37-135">**WsCreateMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [<span data-ttu-id="caf37-136">**Wsfremetadata**</span><span class="sxs-lookup"><span data-stu-id="caf37-136">**WsFreeMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [<span data-ttu-id="caf37-137">**WsGetMetadataEndpoints**</span><span class="sxs-lookup"><span data-stu-id="caf37-137">**WsGetMetadataEndpoints**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [<span data-ttu-id="caf37-138">**WsGetMetadataProperty**</span><span class="sxs-lookup"><span data-stu-id="caf37-138">**WsGetMetadataProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [<span data-ttu-id="caf37-139">**WsGetMissingMetadataDocumentAddress**</span><span class="sxs-lookup"><span data-stu-id="caf37-139">**WsGetMissingMetadataDocumentAddress**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [<span data-ttu-id="caf37-140">**Wsgetpolicyalternativecount**</span><span class="sxs-lookup"><span data-stu-id="caf37-140">**WsGetPolicyAlternativeCount**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [<span data-ttu-id="caf37-141">**Wsgetpolicyproperty**</span><span class="sxs-lookup"><span data-stu-id="caf37-141">**WsGetPolicyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [<span data-ttu-id="caf37-142">**Wsmatchpolicyalternative**</span><span class="sxs-lookup"><span data-stu-id="caf37-142">**WsMatchPolicyAlternative**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [<span data-ttu-id="caf37-143">**Wsummetadata**</span><span class="sxs-lookup"><span data-stu-id="caf37-143">**WsReadMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [<span data-ttu-id="caf37-144">**Wsresetmetadata**</span><span class="sxs-lookup"><span data-stu-id="caf37-144">**WsResetMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

<span data-ttu-id="caf37-145">Die folgenden Handles sind Teil des metadatenimports:</span><span class="sxs-lookup"><span data-stu-id="caf37-145">The following handles are part of metadata import:</span></span>

-   [<span data-ttu-id="caf37-146">WS- \_ Metadaten</span><span class="sxs-lookup"><span data-stu-id="caf37-146">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="caf37-147">WS- \_ Richtlinie</span><span class="sxs-lookup"><span data-stu-id="caf37-147">WS\_POLICY</span></span>](ws-policy.md)

<span data-ttu-id="caf37-148">Die folgenden Strukturen sind Teil des metadatenimports:</span><span class="sxs-lookup"><span data-stu-id="caf37-148">The following structures are part of metadata import:</span></span>

-   [<span data-ttu-id="caf37-149">**WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-149">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="caf37-150">**WS \_ - \_ channeleigenschafteneinschränkung \_**</span><span class="sxs-lookup"><span data-stu-id="caf37-150">**WS\_CHANNEL\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [<span data-ttu-id="caf37-151">**WS- \_ Endpunkt- \_ Richtlinien \_ Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="caf37-151">**WS\_ENDPOINT\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [<span data-ttu-id="caf37-152">**WS-HTTP-Header Authentifizierung- \_ \_ \_ \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-152">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [<span data-ttu-id="caf37-153">**WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-153">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [<span data-ttu-id="caf37-154">**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-154">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="caf37-155">**WS \_ - \_ Metadatenendpunkt**</span><span class="sxs-lookup"><span data-stu-id="caf37-155">**WS\_METADATA\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [<span data-ttu-id="caf37-156">**WS \_ - \_ Metadatenendpunkte**</span><span class="sxs-lookup"><span data-stu-id="caf37-156">**WS\_METADATA\_ENDPOINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [<span data-ttu-id="caf37-157">**WS \_ - \_ Metadateneigenschaft**</span><span class="sxs-lookup"><span data-stu-id="caf37-157">**WS\_METADATA\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [<span data-ttu-id="caf37-158">**WS- \_ Richtlinien \_ Einschränkungen**</span><span class="sxs-lookup"><span data-stu-id="caf37-158">**WS\_POLICY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [<span data-ttu-id="caf37-159">**WS- \_ Richtlinien \_ Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="caf37-159">**WS\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [<span data-ttu-id="caf37-160">**WS- \_ Richtlinien \_ Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="caf37-160">**WS\_POLICY\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [<span data-ttu-id="caf37-161">**WS- \_ Richtlinien \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="caf37-161">**WS\_POLICY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [<span data-ttu-id="caf37-162">**Einschränkung der WS- \_ Anforderungs \_ Sicherheits \_ Token- \_ Eigenschaft \_**</span><span class="sxs-lookup"><span data-stu-id="caf37-162">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [<span data-ttu-id="caf37-163">**WS \_ - \_ sicherheitsbindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-163">**WS\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [<span data-ttu-id="caf37-164">**Einschränkung der WS- \_ Sicherheits \_ Bindungs \_ Eigenschaft \_**</span><span class="sxs-lookup"><span data-stu-id="caf37-164">**WS\_SECURITY\_BINDING\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [<span data-ttu-id="caf37-165">**WS- \_ Sicherheits \_ Einschränkungen**</span><span class="sxs-lookup"><span data-stu-id="caf37-165">**WS\_SECURITY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [<span data-ttu-id="caf37-166">**WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-166">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [<span data-ttu-id="caf37-167">**WS- \_ Sicherheits \_ Eigenschafts \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-167">**WS\_SECURITY\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [<span data-ttu-id="caf37-168">**WS \_ SSL \_ - \_ Transport \_ sicherheitsbindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-168">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [<span data-ttu-id="caf37-169">**WS \_ TCP \_ SSPI \_ - \_ Transport \_ sicherheitsbindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-169">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [<span data-ttu-id="caf37-170">**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="caf37-170">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




