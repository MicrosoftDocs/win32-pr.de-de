---
description: Gibt an, wie die Windows-Suchmaschine in Bezug auf eine bestimmte Eigenschaftendefinition konfiguriert wird.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcfc901dfb4610210c4990c962b5251710e5653
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465627"
---
# <a name="searchinfo"></a>searchInfo

Gibt an, wie die Windows-Suchmaschine in Bezug auf eine bestimmte Eigenschaftendefinition konfiguriert wird. Wenn kein [searchInfo-Element]() bereitgestellt wird, ist die -Eigenschaft nicht in der Windows enthalten. Dieses Element wurde für Windows 7 geändert.

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




| Attribut | BESCHREIBUNG | 
|-----------|-------------|
| inInvertedIndex | Öffentlich. Optional. Gibt an, ob der Eigenschaftswert im invertierten Index gespeichert werden soll. Dadurch können Endbenutzer Volltextabfragen für die Werte dieser Eigenschaft ausführen. Der Standardwert lautet "false". | 
| isColumn | Öffentlich. Optional. Gibt an, ob die Eigenschaft auch in der Windows-Suchdatenbank als Spalte gespeichert werden soll, damit unabhängige Softwarehersteller prädikatbasierte Abfragen erstellen können (z.B. "Select * Where "System.Title"='qqq'"). Wenn der Schemaersteller Endbenutzern (oder Entwicklern) das Erstellen prädikatbasierter Abfragen für die Eigenschaften ermöglichen möchte, muss dies auf "true" festgelegt werden. Der Standardwert lautet "false". | 
| isColumnSparse | Öffentlich. Optional. Der Standardwert ist "true". Wenn die Eigenschaft mehrere Werte hat, ist dieses Attribut immer "true". | 
| columnIndexType | Öffentlich. Optional. Um die Sortierung und Gruppierung zu optimieren, kann die Windows-Suchmaschine sekundäre Indizes für Eigenschaften erstellen, die isColumn="true" aufweisen. Dieses Attribut ist nur nützlich, wenn inInvertedIndex in Windows Vista "true" ist oder wenn isColumn in Windows 7 ist. Wenn die Eigenschaft häufig nach Benutzern sortiert wird, sollte dieses Attribut angegeben werden. Der Standardwert in Windows Vista ist "NotIndexed". Der Standardwert in Windows 7 ist "OnDemand". Die folgenden Werte sind gültig.<ul><li><strong>NotIndexed:</strong>Erstellen Sie niemals einen Wertindex.</li><li><strong>OnDisk:</strong>Erstellen Sie standardmäßig einen Wertindex für diese Eigenschaft.</li><li><strong>OnDiskAll</strong> (nur Windows 7 und höher): Erstellen Sie standardmäßig einen Wertindex für diese Eigenschaft, und wenn es sich um eine Vektoreigenschaft handelt, auch einen Wertindex für alle verketteten Vektorwerte.</li><li><strong>OnDiskVector</strong> (nur Windows 7 und höher): Erstellen Sie standardmäßig einen Wertindex für die verketteten Vektorwerte.</li><li><strong>OnDemand</strong> (nur Windows 7 und höher): Erstellen Sie nur Wertindizes nach Bedarf, d. h. nur bei der ersten Verwendung für eine Abfrage.</li></ul> | 
| Maxsize | Öffentlich. Optional. Die maximale Größe in Bytes, die für eine bestimmte Eigenschaft zulässig ist, die in der Windows gespeichert ist. Der Standardwert lautet:<ul><li><strong>Windows Vista:</strong>128 Bytes</li><li><strong>Windows 7 und höher:</strong>512 Bytes</li></ul>Beachten Sie, dass diese maximale Größe in Bytes und nicht in Zeichen gemessen wird. Die maximale Anzahl von Zeichen hängt von ihrer Codierung ab.<br /> | 
| Zugriffstasten | <strong>Windows 7 und höher.</strong> Öffentlich. Optional. Eine Liste von mnemonischen Werten, die verwendet werden können, um in Suchabfragen auf die -Eigenschaft zu verweisen. Die Liste ist durch das -Zeichen getrennt.|'-Zeichen. | 




 

 

 
