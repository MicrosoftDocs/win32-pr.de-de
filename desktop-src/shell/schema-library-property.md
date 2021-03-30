---
description: Das- <property> Element gibt eine Eigenschaft an, die von der Bibliothek verwendet wird. Diese Eigenschaften sind spezifisch für die Bibliothek. Daher gibt es keinen vordefinierten Satz von Eigenschaftsnamen, die verwendet werden können. Dieses Element ist optional und verfügt über keine untergeordneten Elemente.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Property-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993766"
---
# <a name="property-element-library-schema"></a>Property-Element (Bibliotheks Schema)

Das- <property> Element gibt eine Eigenschaft an, die von der Bibliothek verwendet wird. Diese Eigenschaften sind spezifisch für die Bibliothek. Daher gibt es keinen vordefinierten Satz von Eigenschaftsnamen, die verwendet werden können. Dieses Element ist optional und verfügt über keine untergeordneten Elemente.

## <a name="syntax"></a>Syntax

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                             | Untergeordnete Elemente |
|----------------------------------------------------------------------------|----------------|
| [PropertyStore-Element (Bibliotheks Schema)](schema-library-propertystore.md) | Keine           |



 

## <a name="attributes"></a>Attributes



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
<th>Werte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name</td>
<td>Öffentlich. Erforderlich. Der Anzeigename der Eigenschaft.</td>

</tr>
<tr class="even">
<td>type</td>
<td>Öffentlich. Erforderlich. Der Typ der Eigenschaft.</td>
<td><ul>
<li>Beliebig: Standardwert. Der Wert wird vom Eigenschafts Subsystem nicht erzwungen. VT_NULL wird von GetPropertyType zurückgegeben.</li>
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
<li>UInt64: der Wert muss ein VT_UI8 sein.</li>
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

Die Anforderungen für das <kanonische Name-> Element entsprechen den Anforderungen für Windows Search und das Windows-Eigenschaften System. Die Zeichenfolge muss den Typ "Canonical-Type" aufweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bibliotheks Beschreibungs Schema](library-schema-entry.md)
</dt> <dt>

[Eigenschaftsschemas](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[Suchdienst-Beschreibungs Schema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
