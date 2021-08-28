---
description: Das optionale Eigenschaftenelement gibt die Eigenschaften an, &lt; &gt; die vom Standortanbieter verwendet werden.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: property-Element von locationProvider (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad478fd1d1c00ad5c7f866831cdfdf898557546b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883333"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>property-Element von locationProvider (Search Connector Schema)

Das optionale Eigenschaftenelement gibt die Eigenschaften an, &lt; &gt; die vom Standortanbieter verwendet werden. Diese Eigenschaften sind spezifisch für diesen Speicherortanbieter, sodass es keine vordefinierten Namen gibt, die verwendet werden sollen. Das &lt; &gt; Eigenschaftselement verfügt über zwei Attribute, wie in diesem Thema beschrieben.

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



## <a name="ltpropertygt-element-information"></a>&lt;&gt;property-Elementinformationen



| Übergeordnetes Element                                                                                 | Untergeordnete Elemente                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [locationProvider-Element (Search Connector Schema)](search-schema-sconn-locationprovider.md) | -Eigenschaft, die in diesem Thema beschrieben wird. |



 


## <a name="ltpropertygt-attributes"></a>&lt;&gt;Eigenschaftenattribute




| attribute | Beschreibung | Werte | 
|-----------|-------------|--------|
| name | Erforderlich. Der Anzeigename der Eigenschaft. |   | 
| Typ | Erforderlich. Der Typ der Eigenschaft. | Beliebig: Standardwert. Der Wert wird nicht vom Eigenschaftensubsystem genötigt. VT_NULL werden von GetPropertyType zurückgegeben.<ul><li>NULL: Für diese Eigenschaft ist kein Wert vorhanden. VT_NULL werden von GetPropertyType zurückgegeben.</li><li>Zeichenfolge: Der Wert muss ein VT_LPWSTR sein.</li><li>Boolescher Wert: Der Wert muss ein VT_BOOL sein.</li><li>Byte: Der Wert muss ein VT_UI1 sein.</li><li>Puffer: Der Wert muss ein VT_UI1 | VT_VECTOR Puffer von Bytes.</li><li>Int16: Der Wert muss ein VT_I2 sein.</li><li>UInt16: Der Wert muss ein VT_UI2 sein.</li><li>Int32: Der Wert muss ein VT_I4 sein.</li><li>UInt32: Der Wert muss ein VT_UI4 sein.</li><li>Int64: Der Wert muss ein VT_I8 sein.</li><li>UInt64: Der Wert muss ein VT_UI8</li><li>Double: Der Wert muss ein VT_R8 sein.</li><li>DateTime: Der Wert muss ein VT_FILETIME sein.</li><li>GUID: Der Wert muss ein VT_CLSID sein.</li><li>Blob: Der Wert muss ein VT_BLOB sein.</li><li>Objekt: Der Wert muss ein VT_UNKNOWN sein.</li><li>Stream: Der Wert muss ein VT_STREAM sein.</li><li>Zwischenablage: Der Wert muss ein VT_CF sein.</li></ul> | 




 

## <a name="remarks"></a>Hinweise

Für den OpenSearch-Anbieter werden die folgenden Eigenschaften verwendet:

-   OpenSearchShortName: Kurzname des Suchdiensts
-   OpenSearchQueryTemplate: Vorlage, formatiert gemäß OpenSearch Vorlagenkonvention für den Abfragedienst
-   MaximumResultCount: (Anzahl) Maximale Anzahl von Ergebnissen, die vom Suchdienst zurückgegeben werden
-   LinkIsFilePath: (Boolean) Wenn true, versucht der Anbieter, zurückgegebene Elemente als Dateien zu interpretieren, indem er seine Erweiterungen verwendet, um das richtige ShellItem in der Ansicht zu erstellen. False gibt an, dass Elemente als URL-Verknüpfungen behandelt werden.

 

 



