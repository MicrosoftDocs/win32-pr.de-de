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
# <a name="metadata-import"></a>Metadatenimport

Das wwsapi umfasst API-Elemente, die zum Verarbeiten von WSDL und Richtlinien von einem Endpunkt verwendet werden können, mit dem Ziel, Informationen zu extrahieren, die für die Kommunikation mit dem Endpunkt verwendet werden können. Diese APIs werden in der Regel verwendet, wenn das vom Endpunkt unterstützte Kommunikationsprotokoll nicht bereits bekannt ist.


Verwenden Sie die folgende Sequenz, um Metadaten zu verarbeiten:

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

Informationen dazu, wie WSDL-und WS-Policy Assertionen der API entsprechen, finden Sie im Thema [metadatenzuordnung](metadata-mapping.md) .

## <a name="security"></a>Sicherheit

Die heruntergeladenen Metadaten sind nur so gut wie die Adresse, die zum Herunterladen verwendet wird. Eine Anwendung sollte sicherstellen, dass die Adresse von vertraut. Außerdem sollte eine Anwendung sicherstellen, dass Sie ein Sicherheitsprotokoll zum Herunterladen der Metadatendokumente verwendet, die keine Manipulation der Metadaten ermöglichen.

Eine Anwendung sollte die Adressen der Dienste überprüfen, die von den Metadaten verfügbar gemacht werden. Standardmäßig stellt die Laufzeit sicher, dass der Hostname des Diensts mit dem der ursprünglichen URL übereinstimmt, die zum Herunterladen der Metadaten verwendet wurde, aber die Anwendung möchte möglicherweise weitere Überprüfungen durchführen. Eine Anwendung kann die Überprüfung des Host namens durch Überschreiben der Eigenschaft [**\_ \_ \_ \_ \_ Hostnamen Überprüfen der WS-Metadateneigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) deaktivieren. Wenn die standardmäßig durchgeführte Überprüfung des Host namens deaktiviert ist, muss sich die Anwendung vor den Metadatendokumenten schützen, die die Adresse eines Dienstanbieter von einer anderen Partei enthalten, der nicht auf andere Weise als vertrauenswürdig eingestuft wird.

Standardmäßig ist die maximale Menge an Arbeitsspeicher, die von der Metadatenlaufzeit verwendet wird, um die Metadaten zu deserialisieren und zu verarbeiten, 256 KB, und die maximale Anzahl von Dokumenten, die hinzugefügt werden können, ist 32. Diese Standardwerte können von den Eigenschaften [**\_ \_ \_ Heap \_ angeforderte \_ Größe des WS-metadateneigenschaftenheaps**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) und Eigenschaften für die **Eigenschaft " \_ \_ \_ Max \_** . Diese Begrenzungen dienen dazu, die Menge der Downloads einzuschränken und die Menge des belegten Arbeitsspeichers einzuschränken, um die Metadaten zu sammeln. Das Erhöhen dieser Werte kann zu einer übermäßigen Speicherauslastung, CPU-Auslastung oder Auslastung der Netzwerkbandbreite führen. Beachten Sie, dass eine kleine Nachricht aufgrund der Erweiterung von Wörterbuch Zeichenfolgen im Binärformat zu einer viel größeren deserialisierten Form führen kann. Daher reicht die Verwendung von kleinen Nachrichten nicht aus, um die Speicher Belegung von Metadaten einzuschränken, wenn das Binärformat verwendet wird.

Standardmäßig ist die maximale Anzahl von Richtlinien Alternativen 32, obwohl Sie von der [**WS- \_ Richtlinien \_ Eigenschaft \_ Max \_ alternatives**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) -Eigenschaft überschrieben werden kann. Wenn eine Anwendung durch die einzelnen Alternativen sucht, die nach einer Entsprechung suchen, muss Sie möglicherweise alle alternativen durchsuchen, bevor eine Entsprechung gefunden wird. Das Erhöhen der maximalen Anzahl von Alternativen kann zu einer übermäßigen CPU-Auslastung führen.

Die folgenden Enumerationen sind Teil des metadatenimports:

-   [**ID der WS- \_ \_ Metadateneigenschaft \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [**WS \_ - \_ metadatenstatus**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [**WS \_ - \_ Richtlinien \_ Erweiterungstyp**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [**WS- \_ Richtlinien \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [**WS- \_ Richtlinien \_ Status**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [**Typ der WS- \_ \_ sicherheitsbindungs \_ Einschränkung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

Die folgenden Funktionen sind Teil des metadatenimports:

-   [**Wscreatemetadata**](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [**Wsfremetadata**](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [**WsGetMetadataEndpoints**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [**WsGetMetadataProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [**WsGetMissingMetadataDocumentAddress**](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [**Wsgetpolicyalternativecount**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [**Wsgetpolicyproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [**Wsmatchpolicyalternative**](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [**Wsummetadata**](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [**Wsresetmetadata**](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

Die folgenden Handles sind Teil des metadatenimports:

-   [WS- \_ Metadaten](ws-metadata.md)
-   [WS- \_ Richtlinie](ws-policy.md)

Die folgenden Strukturen sind Teil des metadatenimports:

-   [**WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**WS \_ - \_ channeleigenschafteneinschränkung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [**WS- \_ Endpunkt- \_ Richtlinien \_ Erweiterung**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [**WS-HTTP-Header Authentifizierung- \_ \_ \_ \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [**WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**WS \_ - \_ Metadatenendpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [**WS \_ - \_ Metadatenendpunkte**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [**WS \_ - \_ Metadateneigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [**WS- \_ Richtlinien \_ Einschränkungen**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [**WS- \_ Richtlinien \_ Erweiterung**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [**WS- \_ Richtlinien \_ Eigenschaften**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [**WS- \_ Richtlinien \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [**Einschränkung der WS- \_ Anforderungs \_ Sicherheits \_ Token- \_ Eigenschaft \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [**WS \_ - \_ sicherheitsbindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [**Einschränkung der WS- \_ Sicherheits \_ Bindungs \_ Eigenschaft \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [**WS- \_ Sicherheits \_ Einschränkungen**](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [**WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [**WS- \_ Sicherheits \_ Eigenschafts \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [**WS \_ SSL \_ - \_ Transport \_ sicherheitsbindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [**WS \_ TCP \_ SSPI \_ - \_ Transport \_ sicherheitsbindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




