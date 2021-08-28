---
description: Gibt an, wie die Bezeichnungen der Eigenschaft angezeigt werden.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d2d358270bfdf231f990feee54d90f6f39f16fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475096"
---
# <a name="labelinfo"></a>labelInfo

Gibt an, wie die Bezeichnungen der Eigenschaft angezeigt werden. Es sollte nur ein [labelInfo-Element]() für jedes [propertyDescription-Element geben.](./propdesc-schema-propertydescription.md)

Wenn mehrere Elemente enthalten sind, wird das letzte verwendet. Wenn kein [labelInfo-Element]() angegeben wird, wird die Bezeichnung der Eigenschaft nicht angezeigt. Dies wäre jedoch in der Regel ein Fehler.

## <a name="syntax"></a>Syntax


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
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
| label | Öffentlich. Optional. Die Bezeichnung, wie sie auf der Benutzeroberfläche angezeigt wird (z. B. die Detailspaltenbezeichnung oder der Vorschaubereich). Die Syntax ermöglicht eine direkte Anzeigezeichenfolge oder einen indirekten Anzeigezeichenfolgenverweis. Verwenden Sie die indirekte Anzeigezeichenfolge, da sie lokalisiert werden kann. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName gibt</strong></a> den aufgelösten Anzeigenamen zurück. | 
| Sortdescription | Optional. Gibt die als Sortieroptionen angebotenen Zeichenfolgen an. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription</strong></a> gibt diese Sortierbeschreibung zurück. Die folgenden Werte stellen die entsprechenden Benutzeroberflächenzeichenfolgen zur Verfügung.<ul><li>Allgemein: "Sort going up" /"Sort going down"</li><li>AToZ: "A on top" /"Z on top"</li><li>LowestHighest: "Lowest on top" /"Highest on top"</li><li>OldestNewest: "Oldest on top" /"Newest on top"</li><li>SmallestLargest: "Smallest on top" /"Largest on top"</li></ul> | 
| invitationText | Optional. Der Hilfezeichenfolgentext, der dem Benutzer als Anweisung für das Steuerelement oder die QuickInfo angezeigt wird (z.B. "Enter author name."). Die Syntax ermöglicht eine direkte Anzeigezeichenfolge oder einen indirekten Anzeigezeichenfolgenverweis. Verwenden Sie die indirekte Anzeigezeichenfolge, da sie lokalisiert werden kann. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation gibt</strong></a> den aufgelösten Einladungstext zurück. | 
| hideLabel | Optional. Der Standardwert lautet "false". Gibt an, ob die Bezeichnung ausgeblendet ist. | 




 

 

 
