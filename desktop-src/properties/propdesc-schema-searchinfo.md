---
description: Gibt an, wie die Windows Suchmaschine in Bezug auf eine bestimmte Eigenschaftendefinition konfiguriert wird.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e279f6ffe8ce161c421bc7c3e8918f93a94b90cfa11f65989b0e5531c298374e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885940"
---
# <a name="searchinfo"></a>searchInfo

Gibt an, wie die Windows Suchmaschine in Bezug auf eine bestimmte Eigenschaftendefinition konfiguriert wird. Wenn kein [searchInfo-Element]() bereitgestellt wird, ist die -Eigenschaft nicht in der Windows-Suchmaschine enthalten. Dieses Element wurde für Windows 7 geändert.

## <a name="syntax-for-windows-7"></a>Syntax für Windows 7


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a>Syntax für Windows Vista


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                   | Untergeordnete Elemente |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Keine           |



 

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>Öffentlich. Optional. Gibt an, ob der Eigenschaftswert im invertierten Index gespeichert werden soll. Dadurch können Endbenutzer Volltextabfragen für die Werte dieser Eigenschaft ausführen. Die Standardeinstellung ist &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>Öffentlich. Optional. Gibt an, ob die Eigenschaft auch in der Windows Suchdatenbank als Spalte gespeichert werden soll, damit unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) prädikatbasierte Abfragen erstellen können (z. B. &quot; Auswählen * Where &quot; System.Title &quot; ='qqq' &quot; ). Wenn der Schemaersteller Endbenutzern (oder Entwicklern) ermöglichen möchte, prädikatbasierte Abfragen für die Eigenschaften zu erstellen, muss dies auf TRUE festgelegt &quot; &quot; werden. Die Standardeinstellung ist &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot;true&quot;. Wenn die Eigenschaft mehrwertige Ist, ist dieses Attribut immer &quot; &quot; true.</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Öffentlich. Optional. Um die Sortierung und Gruppierung zu optimieren, kann die Windows Suchmaschine sekundäre Indizes für Eigenschaften erstellen, die isColumn= &quot; true &quot; aufweisen. Dieses Attribut ist nur nützlich, wenn inInvertedIndex in Windows Vista true ist &quot; &quot; oder wenn isColumn &quot; in Windows 7 true &quot; ist. Wenn die Eigenschaft in der Regel häufig nach Benutzern sortiert wird, sollte dieses Attribut angegeben werden. Der Standardwert in Windows Vista ist &quot; NotIndexed. &quot; Der Standardwert in Windows 7 ist &quot; &quot; OnDemand. Die folgenden Werte sind gültig.
<ul>
<li><strong>NotIndexed:</strong>Erstellen Sie niemals einen Wertindex.</li>
<li><strong>OnDisk:</strong>Erstellen Sie standardmäßig einen Wertindex für diese Eigenschaft.</li>
<li><strong>OnDiskAll</strong> (nur Windows 7 und höher): Erstellen Sie standardmäßig einen Wertindex für diese Eigenschaft, und wenn es sich um eine Vektoreigenschaft handelt, auch einen Wertindex für alle verketteten Vektorwerte.</li>
<li><strong>OnDiskVector</strong> (nur Windows 7 und höher): Erstellen Sie standardmäßig einen Wertindex für die verketteten Vektorwerte.</li>
<li><strong>OnDemand</strong> (nur Windows 7 und höher): Erstellen Sie nur Wertindizes nach Bedarf, d. h., sie werden nur zum ersten Mal für eine Abfrage verwendet.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maxsize</td>
<td>Öffentlich. Optional. Die maximale Größe in Bytes, die für eine bestimmte Eigenschaft zulässig ist, die in der Windows-Suchdatenbank gespeichert ist. Der Standardwert lautet:
<ul>
<li><strong>Windows Vista:</strong>128 Bytes</li>
<li><strong>Windows 7 und höher:</strong>512 Bytes</li>
</ul>
Beachten Sie, dass diese maximale Größe in Bytes und nicht in Zeichen gemessen wird. Die maximale Anzahl von Zeichen hängt von ihrer Codierung ab.<br/></td>
</tr>
<tr class="even">
<td>Zugriffstasten</td>
<td><strong>Windows 7 und höher.</strong> Öffentlich. Optional. Eine Liste der mnemonischen Werte, die verwendet werden können, um in Suchabfragen auf die -Eigenschaft zu verweisen. Die Liste ist durch das Zeichen "|" getrennt.</td>
</tr>
</tbody>
</table>



 

 

 
