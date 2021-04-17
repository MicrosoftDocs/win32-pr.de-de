---
description: Das optionale- <property> Element gibt eine Eigenschaft an, die vom Suchconnector verwendet wird. Diese Eigenschaften sind spezifisch für diesen Suchconnector. Daher gibt es keine vordefinierte Gruppe von Namen, die verwendet werden können. Dieses Element hat keine untergeordneten Elemente.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Property-Element von PropertyStore (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525451"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>Property-Element von PropertyStore (Suchconnector-Schema)

Das optionale- <property> Element gibt eine Eigenschaft an, die vom Suchconnector verwendet wird. Diese Eigenschaften sind spezifisch für diesen Suchconnector. Daher gibt es keine vordefinierte Gruppe von Namen, die verwendet werden können. Dieses Element hat keine untergeordneten Elemente.

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
| [PropertyStore-Element (Suchconnector-Schema)](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
<th>Werte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name</td>
<td>Öffentlich. Erforderlich. Der Anzeigename der Eigenschaft.</td>
<td> </td>
</tr>
<tr class="even">
<td>type</td>
<td>Öffentlich. Erforderlich. Der Typ der Eigenschaft.</td>
<td>Beliebig: Standardwert. Der Wert wird vom Eigenschafts Subsystem nicht erzwungen. VT_NULL wird von GetPropertyType zurückgegeben.
<ul>
<li>NULL: für diese Eigenschaft ist kein Wert vorhanden. VT_NULL wird von GetPropertyType zurückgegeben.</li>
<li>String: der Wert muss ein VT_LPWSTR sein.</li>
<li>Boolescher Wert: der Wert muss ein VT_BOOL sein.</li>
<li>Byte: der Wert muss ein VT_UI1 sein.</li>
<li>Buffer: der Wert muss ein VT_UI1 sein | VT_VECTOR Puffer bytes.</li>
<li>Int16: der Wert muss ein VT_I2 sein.</li>
<li>UInt16: der Wert muss ein VT_UI2 sein.</li>
<li>Int32: der Wert muss ein VT_I4 sein.</li>
<li>UInt32: der Wert muss ein VT_UI4 sein.</li>
<li>Int64: der Wert muss ein VT_I8 sein.</li>
<li>UInt64: der Wert muss ein VT_UI8</li>
<li>Double: der Wert muss ein VT_R8 sein.</li>
<li>DateTime: der Wert muss ein VT_FILETIME sein.</li>
<li>GUID: der Wert muss ein VT_CLSID sein.</li>
<li>BLOB: der Wert muss ein VT_BLOB sein.</li>
<li>Objekt: der Wert muss ein VT_UNKNOWN sein.</li>
<li>Stream: der Wert muss ein VT_STREAM sein.</li>
<li>Zwischenablage: der Wert muss ein VT_CF sein.</li>
</ul></td>
</tr>
<tr class="odd">
<td>schema</td>
<td>Öffentlich. Dies ist optional. Das Schema, in dem die Eigenschaft definiert ist.</td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

OpenSearch-Suchconnectors können die opensearchhtmlrollovertemplate-Eigenschaft verwenden. Diese Eigenschaft identifiziert eine Vorlage, die nach der OpenSearch-Vorlagen Konvention formatiert ist. Die Vorlage "opensearchhtmlrollovertemplate" wird verwendet, wenn der Benutzer in der Befehlsleiste auf die Schaltfläche "Suche nach Website" klickt.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt ein- <propertyStore> Element mit zwei- <property> Elementen.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



