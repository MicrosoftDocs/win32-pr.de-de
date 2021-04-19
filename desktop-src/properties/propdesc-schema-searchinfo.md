---
description: Gibt an, wie die Windows-Such-Engine in Bezug auf eine angegebene Eigenschafts Definition konfiguriert wird.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: SearchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360177"
---
# <a name="searchinfo"></a>SearchInfo

Gibt an, wie die Windows-Such-Engine in Bezug auf eine angegebene Eigenschafts Definition konfiguriert wird. Wenn kein [SearchInfo]() -Element bereitgestellt wird, ist die Eigenschaft nicht in der Windows-Suchmaschine enthalten. Dieses Element wurde für Windows 7 geändert.

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
| [propertydescription](./propdesc-schema-propertydescription.md) | Keine           |



 

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ininvertedindex</td>
<td>Öffentlich. Dies ist optional. Gibt an, ob der Eigenschafts Wert im invertierten Index gespeichert werden soll. Dadurch können Endbenutzer voll Text Abfragen für die Werte dieser Eigenschaft ausführen. Die Standardeinstellung ist &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>iscolumn</td>
<td>Öffentlich. Dies ist optional. Gibt an, ob die Eigenschaft auch in der Windows Search-Datenbank als Spalte gespeichert werden soll, damit unabhängige Softwareanbieter (ISVs) Prädikat basierte Abfragen erstellen können (z. b &quot; . Select * Where &quot; System. Title &quot; = ' QQQ ' &quot; ). Wenn der Schema Ersteller es Endbenutzern (oder Entwicklern) ermöglichen möchte, Prädikat basierte Abfragen für die Eigenschaften zu erstellen, muss dieser Wert auf "true" festgelegt werden &quot; &quot; . Die Standardeinstellung ist &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>iscolumnsparse</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot;true&quot;. Wenn die Eigenschaft mehr wertig ist, ist dieses Attribut immer " &quot; true" &quot; .</td>
</tr>
<tr class="even">
<td>columnindextype</td>
<td>Öffentlich. Dies ist optional. Um das Sortieren und Gruppieren zu optimieren, kann das Windows Search-Modul sekundäre Indizes für Eigenschaften erstellen, deren iscolumn = &quot; true ist &quot; . Dieses Attribut ist nur nützlich, wenn ininvertedindex &quot; &quot; in Windows Vista true ist oder wenn iscolumn &quot; in Windows 7 "true" ist &quot; . Wenn die Eigenschaft tendenziell häufig von Benutzern sortiert wird, sollte dieses Attribut angegeben werden. Der Standardwert in Windows Vista ist nicht &quot; indiziert &quot; . Der Standardwert in Windows 7 ist &quot; OnDemand &quot; . Die folgenden Werte sind gültig.
<ul>
<li><strong>Notindiziert</strong>: erstellt nie einen Wertindex.</li>
<li><strong>Ondisk</strong>: erstellt standardmäßig einen Wert Index für diese Eigenschaft.</li>
<li><strong>Ondiskall</strong> (nur Windows 7 und höher): Erstellen Sie für diese Eigenschaft standardmäßig einen Wert Index, und wenn es sich um eine Vektor Eigenschaft handelt, ist dies auch ein Wert Index für alle verketteten Vektor Werte.</li>
<li><strong>Ondiskvector</strong> (nur Windows 7 und höher): Erstellen Sie standardmäßig einen Wert Index für die verketteten Vektor Werte.</li>
<li><strong>OnDemand</strong> (nur Windows 7 und höher): nur buildwertindizes nach Bedarf, d. h. nur das erste Mal, wenn Sie für eine Abfrage verwendet werden.</li>
</ul></td>
</tr>
<tr class="odd">
<td>MaxSize</td>
<td>Öffentlich. Dies ist optional. Die maximale Größe (in Bytes), die für eine bestimmte Eigenschaft zulässig ist, die in der Windows Search-Datenbank gespeichert ist. Der Standardwert lautet:
<ul>
<li><strong>Windows Vista</strong>: 128 Bytes</li>
<li><strong>Windows 7 und</strong>höher: 512 Bytes</li>
</ul>
Beachten Sie, dass diese maximale Größe in Bytes und nicht in Zeichen gemessen wird. Die maximale Anzahl von Zeichen hängt von ihrer Codierung ab.<br/></td>
</tr>
<tr class="even">
<td>Zugriffstasten</td>
<td><strong>Windows 7 und höher.</strong> Öffentlich. Dies ist optional. Eine Liste von mnetmonischen Werten, die verwendet werden können, um auf die Eigenschaft in Such Abfragen zu verweisen. Die Liste wird durch das Zeichen "|" getrennt.</td>
</tr>
</tbody>
</table>



 

 

 
