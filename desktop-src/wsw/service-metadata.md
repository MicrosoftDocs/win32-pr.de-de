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
# <a name="service-metadata"></a>Dienstmetadaten

Der wwsapi-Dienst Host unterstützt WS-MetadataExchange für seine Endpunkte. Sie aktivieren einen solchen Metadatenaustausch auf dem Dienst Host mit den folgenden Schritten:

-   Geben Sie Metadatendokumente in der [**WS- \_ \_ dienstmetadateneigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) auf dem [WS- \_ Dienst \_ Host](ws-service-host.md)an.
-   Geben Sie den Dienstnamen in der [**WS- \_ \_ dienstmetadateneigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) auf dem [WS- \_ Dienst \_ Host](ws-service-host.md)an.
-   Geben Sie den Port für einzelne Endpunkte an, indem Sie die Eigenschaft [**\_ \_ \_ \_ Metadateneigenschaft des WS-Dienst Endpunkts**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) für den [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)verwenden
-   Aktivieren Sie eine oder mehrere [**WS- \_ dienstend \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) Punkt Strukturen, um die WS-MetadataExchange Anforderungen zu bedienen.
-   Optional können Sie **das \_ URL \_ - \_ \_ \_ \_ \_ Suffix für die WS-dienstend Punkt Eigenschaft** in der [**Eigenschaften-ID des WS- \_ Dienst \_ Endpunkts \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) angeben, um Ws-MetadataExchange Anforderungen an eine bestimmte Adresse zu warten.


Angeben von Metadatendokumenten/Dienstnamen auf dem Dienst Host

Der erste Schritt besteht darin, die Metadatendokumente auf dem Dienst Host anzugeben. Zu diesem Zweck erfassen Sie die einzelnen Dokumente als Array von WS \_ \_ -XML \* -Zeichen folgen. Diese Zeichen folgen können XML-Schema, WSDL oder WS-Policy Dokument sein. Dies wird durch die Eigenschaft [**\_ \_ \_ Metadateneigenschaft der WS-Dienst Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) angegeben.

Optional kann eine Anwendung auch den Dienstnamen und den Namespace als Teil der WS- [**\_ Dienst \_ Metadaten**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)angeben. Wenn das Metadatendokument das Dienst Element für den angegebenen Dienstnamen nicht angibt, generiert das Dienstmodell ein Dienst Element mit den entsprechenden WSDL-Ports für den Dienst.

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

Beachten Sie, dass keine Überprüfung der einzelnen Metadatendokumente für die Dokumente ausgeführt wird. Es liegt in der Verantwortung der Anwendung, den Inhalt der Dokumente zu überprüfen und sicherzustellen, dass alle Import Pfade relativ angegeben sind.

Der angegebene Namespace wird verwendet, um das Dokument zu suchen, in dem das Dienst Element vom Dienst Host hinzugefügt wird.

Hinzufügen des Dienst Elements zum WSDL-Dokument

Der Dienst Host stellt eine Funktion für die Anwendung bereit, um in Ihrem Namen ein Dienst Element hinzuzufügen, sofern noch nicht geschehen. Um dieses Verhalten zu aktivieren, muss eine Anwendung die Felder serivcename und servicens in der [**WS \_ - \_ dienstmetadatenstruktur**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) angeben. Wenn Service Name und servicens beide **null** sind, wird dem WSDL-Dokument kein Dienst Element hinzugefügt. Beide werden verwendet, um Dokumente zu identifizieren, in denen das Service Element hinzugefügt wird.

Wenn die Eigenschaft [**\_ \_ \_ Metadateneigenschaft der WS-Dienst Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) nicht angegeben ist, findet kein Metadatenaustausch auf dem Dienst Host statt.

Angeben des Ports auf dem WS- \_ Dienst \_ Endpunkt

Damit ein [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) als Port innerhalb des Dienst Elements im WSDL-Dokument verfügbar ist, muss die Anwendung für die [**\_ \_ \_ Eigenschaft \_ Metadateneigenschaft des WS-Dienst Endpunkts**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) angeben.

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

Es wird davon ausgegangen, dass der Verweis auf den Bindungs Namen und-Namespace in den Dokumenten vorhanden ist, die auf dem Dienst Host als Teil der WS- \_ Dienst \_ Eigenschafts Metadaten angegeben sind \_ . Die Laufzeit überprüft dies im Auftrag der Anwendung nicht.

Aktivieren der WS-MetadataExchange Wartung auf dem WS- \_ Dienst \_ Endpunkt

Damit WS-MetadataExchange Anforderungen verarbeitet werden können, muss der Dienst Host mindestens einen Endpunkt für die Wartung WS-MetadataExchange Anforderungen aktiviert haben. Dies erfolgt durch Festlegen der entsprechenden Version für WS-MetadataExchange auf dem [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Aktivieren von HTTP Get-Wartung auf dem WS- \_ Dienst \_ Endpunkt

Um servicehttp Get-Anforderungen zu verarbeiten, muss der Dienst Host mindestens einen Endpunkt haben, der für die Wartung WS-MetadataExchange Anforderungen aktiviert ist. Dies erfolgt durch Festlegen der entsprechenden Version für WS-MetadataExchange auf dem [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Angeben von URL-Suffix für Ws-MetadataExchange Anforderungen

Eine Anwendung kann optional nur das akzeptieren von Anforderungen für WS-MetadataExchange für einen bestimmten Pfad aktivieren. Dies erfolgt durch Angabe eines Suffixes für den angegebenen WS- \_ Dienst \_ Endpunkt. Dieses Suffix wird unverändert an die tatsächliche URL des WS- \_ Dienst \_ Endpunkts verkettet. Die verketteten Zeichenfolge wird als übereinstimmende URL zum empfangenen ' to '-Header verwendet.

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

Die folgenden API-Elemente beziehen sich auf die Dienst Metada.

| Enumeration                                                       | Beschreibung                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**WS \_ - \_ metadatenaustauschtyp \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | Aktiviert oder deaktiviert WS-MetadataExchange und HTTP Get-Wartung für den Endpunkt. |



 



| Struktur                                                               | BESCHREIBUNG                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Metadaten des WS- \_ Dienst \_ Endpunkts \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | Stellt das Port-Element für den Endpunkt dar.                         |
| [**WS- \_ Dienst \_ Metadaten**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | Gibt das Array der dienstmetadatendokumente an.                       |
| [**WS \_ - \_ dienstmetadatendokument \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | Gibt die einzelnen Dokumente an, aus denen die Dienst Metadaten besteht. |



 

 

 




