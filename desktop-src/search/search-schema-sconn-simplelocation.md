---
description: Das <simpleLocation> -Element gibt den Speicherort für Suchconnectors an, die dateisystem- oder protokollhandlerbasierte Connectors sind. Dieses Element verfügt über zwei untergeordnete Elemente und keine Attribute.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: simpleLocation-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82731c5a230f8dd12b9d73cafd75dfc7d3cdd66bf1e57120701ed3ca0ba54b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862461"
---
# <a name="simplelocation-element-search-connector-schema"></a>simpleLocation-Element (Search Connector Schema)

Das <simpleLocation> -Element gibt den Speicherort für Suchconnectors an, die dateisystem- oder protokollhandlerbasierte Connectors sind. Dieses Element verfügt über zwei untergeordnete Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                                                   | Untergeordnete Elemente                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) | [simpleLocation url-Element (Search Connector Schema)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | serialisiert: Dieses Element enthält den Base64-codierten ShellLink, der auf den im -Element definierten <url> Speicherortzeigt. Windows 7 erstellt shellLink aus dem Wert des -Elements und aktualisiert dieses Feld beim ersten Laden dieser Bibliothek ordnungsgemäß, sodass es vom Autor leer <url> gelassen werden sollte. |



 

## <a name="remarks"></a>Hinweise

Dieses Element kann anstelle von verwendet werden, wenn sich der Speicherort im Dateisystem befindet oder der Connector ein bekannter Protokollhandler <locationProvider> ist (z.B. mapi:). Wenn <simpleLocation> vorhanden ist, DARF KEIN -Element <locationProvider> vorhanden sein. Verwenden Sie für Connectors für die Webdienstanbietersuche stattdessen [<locationProvider>](search-schema-sconn-locationprovider.md) das -Element.

## <a name="examples"></a>Beispiele


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



