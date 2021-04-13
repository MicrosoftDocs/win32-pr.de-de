---
description: Das- <simpleLocation> Element gibt den Speicherort für Suchconnectors an, die auf Dateisystem oder auf Protokoll Handlern basieren. Dieses Element verfügt über zwei untergeordnete Elemente und keine Attribute.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: simpleloation-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12c17ace36314ceb180f14b6de0eb7a890a385b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342899"
---
# <a name="simplelocation-element-search-connector-schema"></a>simpleloation-Element (Suchconnector-Schema)

Das- <simpleLocation> Element gibt den Speicherort für Suchconnectors an, die auf Dateisystem oder auf Protokoll Handlern basieren. Dieses Element verfügt über zwei untergeordnete Elemente und keine Attribute.

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
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) | [simpleloation-URL-Element (Suchconnector-Schema)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | serialized: dieses Element enthält den Base64-codierten shelllink, der auf den im-Element definierten Speicherort verweist <url> . Windows 7 erstellt shelllink aus dem Wert des <url> -Elements und aktualisiert dieses Feld ordnungsgemäß auf dem ersten Laden dieser Bibliothek. Daher sollte es vom Autor leer gelassen werden. |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element kann anstelle von verwendet werden, <locationProvider> Wenn sich der Speicherort im Dateisystem befindet oder der Connector ein bekannter Protokollhandler (wie MAPI:) ist. Wenn <simpleLocation> vorhanden ist, darf kein-Element vorhanden sein <locationProvider> . Verwenden Sie für Webdienstanbieter-Suchconnectors stattdessen das- [<locationProvider>](search-schema-sconn-locationprovider.md) Element.

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



 

 



