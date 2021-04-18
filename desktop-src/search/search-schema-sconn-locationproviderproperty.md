---
description: Das optionale- <property> Element gibt die Eigenschaften an, die vom Speicherort Anbieter verwendet werden.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Property-Element von locationprovider (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106351913"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>Property-Element von locationprovider (Suchconnector-Schema)

Das optionale- <property> Element gibt die Eigenschaften an, die vom Speicherort Anbieter verwendet werden. Diese Eigenschaften sind spezifisch für diesen Speicherort Anbieter. Daher gibt es keine vordefinierte Gruppe von Namen, die verwendet werden können. Das- <property> Element verfügt über zwei Attribute, wie in diesem Thema beschrieben.

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



## <a name="property-element-information"></a><property> Element Informationen



| Übergeordnetes Element                                                                                 | Untergeordnete Elemente                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [locationprovider-Element (Suchconnector-Schema)](search-schema-sconn-locationprovider.md) | -Eigenschaft, die in diesem Thema beschrieben wird. |



 


## <a name="property-attributes"></a><property> Legt



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
<td>Erforderlich. Der Anzeigename der Eigenschaft.</td>
<td> </td>
</tr>
<tr class="even">
<td>type</td>
<td>Erforderlich. Der Typ der Eigenschaft.</td>
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
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Für den OpenSearch-Anbieter werden die folgenden Eigenschaften verwendet:

-   Opensearchshortname: Kurzname des Such Dienstanbieter
-   Opensearchquerytemplate: Vorlage, die nach der OpenSearch-Vorlagen Konvention formatiert ist, für den Abfragedienst
-   Maximumresultcount: (Anzahl) maximale Anzahl von Ergebnissen, die vom Suchdienst zurückgegeben werden.
-   Linkisfilepath: (Boolean) Wenn true, versucht der Anbieter, die zurückgegebenen Elemente als Dateien zu interpretieren, wobei die Erweiterungen verwendet werden, um das richtige shellitem in der Ansicht zu erstellen. Bei "false" werden Elemente als URL-Verknüpfungen behandelt.

 

 



