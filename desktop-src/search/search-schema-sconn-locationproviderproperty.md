---
description: Das <property> optionale -Element gibt die eigenschaften an, die vom Speicherortanbieter verwendet werden.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: property-Element von locationProvider (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623d54ef98986c603acc709bcd39ca1ac5504b89
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471556"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>property-Element von locationProvider (Search Connector Schema)

Das <property> optionale -Element gibt die eigenschaften an, die vom Speicherortanbieter verwendet werden. Diese Eigenschaften sind spezifisch für diesen Standortanbieter, sodass keine vordefinierten Namen verwendet werden müssen. Das <property> -Element verfügt über zwei Attribute, wie in diesem Thema beschrieben.

## <a name="syntax"></a>Syntax


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="property-element-information"></a><property> Elementinformationen



| Übergeordnetes Element                                                                                 | Untergeordnete Elemente                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [locationProvider-Element (Connectorschema suchen)](search-schema-sconn-locationprovider.md) | -Eigenschaft, die in diesem Thema beschrieben wird. |



 


## <a name="property-attributes"></a><property> Attribute




| Attribut | BESCHREIBUNG | Werte | 
|-----------|-------------|--------|
| name | Erforderlich. Der Anzeigename der Eigenschaft. |   | 
| Typ | Erforderlich. Der Typ der Eigenschaft. | Any: Standard. Der Wert wird nicht vom Eigenschaftensubsystem umerciert. VT_NULL wird von GetPropertyType zurückgegeben.<ul><li>NULL: Für diese Eigenschaft ist kein Wert enthalten. VT_NULL wird von GetPropertyType zurückgegeben.</li><li>Zeichenfolge: Der Wert muss ein VT_LPWSTR.</li><li>Boolescher Wert: Der Wert muss ein VT_BOOL.</li><li>Byte: Der Wert muss ein VT_UI1.</li><li>Puffer: Der Wert muss ein VT_UI1 | VT_VECTOR Puffer von Bytes.</li><li>Int16: Der Wert muss ein VT_I2.</li><li>UInt16: Der Wert muss ein VT_UI2.</li><li>Int32: Der Wert muss ein VT_I4.</li><li>UInt32: Der Wert muss ein VT_UI4.</li><li>Int64: Der Wert muss ein VT_I8.</li><li>UInt64: Der Wert muss ein VT_UI8</li><li>Double: Der Wert muss eine VT_R8.</li><li>DateTime: Der Wert muss ein VT_FILETIME.</li><li>GUID: Der Wert muss ein VT_CLSID.</li><li>Blob: Der Wert muss ein VT_BLOB.</li><li>Objekt: Der Wert muss ein VT_UNKNOWN.</li><li>Stream: Der Wert muss ein VT_STREAM.</li><li>Zwischenablage: Der Wert muss ein VT_CF.</li></ul> | 




 

## <a name="remarks"></a>Hinweise

Für den OpenSearch werden die folgenden Eigenschaften verwendet:

-   OpenSearchShortName: Kurzname des Suchdiensts
-   OpenSearchQueryTemplate: Vorlage, formatiert nach OpenSearch Vorlagenkonvention für den Abfragedienst
-   MaximumResultCount: (Anzahl) Maximale Anzahl von Ergebnissen, die vom Suchdienst zurückgegeben werden
-   LinkIsFilePath: (Boolean): Wenn true, versucht der Anbieter, zurückgegebene Elemente als Dateien zu interpretieren, und verwendet deren Erweiterungen, um das richtige ShellItem in der Ansicht zu erstellen. False gibt an, dass Elemente als URL-Verknüpfungen behandelt werden.

 

 



