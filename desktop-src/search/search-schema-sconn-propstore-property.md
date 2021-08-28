---
description: Das &lt; optionale &gt; Eigenschaftenelement gibt eine Eigenschaft an, die vom Suchconnector verwendet wird. Diese Eigenschaften sind spezifisch für diesen Suchconnector, sodass kein vordefinierter Satz von Namen verwendet werden kann. Dieses Element verfügt über keine untergeordneten Elemente.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: property-Element von propertyStore (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ad97c22ac87d67fdec0d007d4333bffe16aad1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886773"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>property-Element von propertyStore (Connectorschema suchen)

Das &lt; optionale &gt; Eigenschaftenelement gibt eine Eigenschaft an, die vom Suchconnector verwendet wird. Diese Eigenschaften sind spezifisch für diesen Suchconnector, sodass kein vordefinierter Satz von Namen verwendet werden kann. Dieses Element verfügt über keine untergeordneten Elemente.

## <a name="syntax"></a>Syntax


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
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



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                           | Untergeordnete Elemente |
|------------------------------------------------------------------------------------------|----------------|
| [propertyStore-Element (Connectorschema suchen)](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a>Attribute




| attribute | Beschreibung | Werte | 
|-----------|-------------|--------|
| name | Öffentlich. Erforderlich. Der Anzeigename der Eigenschaft. |   | 
| Typ | Öffentlich. Erforderlich. Der Typ der Eigenschaft. | Any: Standard. Der Wert wird nicht vom Eigenschaftensubsystem umerciert. VT_NULL wird von GetPropertyType zurückgegeben.<ul><li>NULL: Für diese Eigenschaft ist kein Wert enthalten. VT_NULL wird von GetPropertyType zurückgegeben.</li><li>Zeichenfolge: Der Wert muss ein VT_LPWSTR.</li><li>Boolescher Wert: Der Wert muss ein VT_BOOL.</li><li>Byte: Der Wert muss ein VT_UI1.</li><li>Puffer: Der Wert muss ein VT_UI1 | VT_VECTOR Puffer von Bytes.</li><li>Int16: Der Wert muss ein VT_I2.</li><li>UInt16: Der Wert muss ein VT_UI2.</li><li>Int32: Der Wert muss ein VT_I4.</li><li>UInt32: Der Wert muss ein VT_UI4.</li><li>Int64: Der Wert muss ein VT_I8.</li><li>UInt64: Der Wert muss ein VT_UI8</li><li>Double: Der Wert muss ein VT_R8.</li><li>DateTime: Der Wert muss ein VT_FILETIME.</li><li>GUID: Der Wert muss ein VT_CLSID.</li><li>Blob: Der Wert muss ein VT_BLOB.</li><li>Objekt: Der Wert muss ein VT_UNKNOWN.</li><li>Stream: Der Wert muss ein VT_STREAM.</li><li>Zwischenablage: Der Wert muss ein VT_CF.</li></ul> | 
| schema | Öffentlich. Optional. Das Schema, in dem die Eigenschaft definiert ist. |   | 




 

## <a name="remarks"></a>Hinweise

OpenSearch-Connectors können die OpenSearchHTMLRolloverTemplate-Eigenschaft verwenden. Diese Eigenschaft identifiziert eine Vorlage, die nach der OpenSearch formatiert ist. Die Vorlage OpenSearchHTMLRolloverTemplate wird verwendet, wenn der Benutzer in der Befehlsleiste auf die Schaltfläche "Auf Website suchen" klickt.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt ein &lt; propertyStore-Element &gt; mit zwei &lt; &gt; Eigenschaftenelementen.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



