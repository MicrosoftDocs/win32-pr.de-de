---
description: Gibt an, wie die Bezeichnungen der Eigenschaft angezeigt werden.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: Labelinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349134"
---
# <a name="labelinfo"></a>Labelinfo

Gibt an, wie die Bezeichnungen der Eigenschaft angezeigt werden. Es darf nur ein [Labelinfo]() -Element für jedes [propertydescription](./propdesc-schema-propertydescription.md) -Element vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet. Wenn kein [Labelinfo]() -Element angegeben wird, wird die Bezeichnung der Eigenschaft nicht angezeigt. Dies wäre in der Regel jedoch ein Fehler.

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
<td>label</td>
<td>Öffentlich. Dies ist optional. Die Bezeichnung, wie Sie in der Benutzeroberfläche angezeigt wird (z. b. die Bezeichnung "Details" oder "Vorschau"). Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge. Verwenden Sie die indirekte Anzeige Zeichenfolge, da Sie lokalisiert werden kann. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>Ipropertydescription:: GetDisplayName</strong></a> gibt den aufgelösten anzeigen Amen zurück.</td>
</tr>
<tr class="even">
<td>SortDescription</td>
<td>Dies ist optional. Gibt die als Sortieroptionen angebotenen Zeichen folgen an. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>Ipropertydescription:: getsortdescription</strong></a> gibt diese Sortier Beschreibung zurück. Die folgenden Werte stellen die entsprechenden UI-Zeichen folgen bereit.
<ul>
<li>Allgemein: &quot; Sortieren nach oben &quot;  /  &quot; Sortieren&quot;</li>
<li>Atoz: &quot; A in Top &quot;  /  &quot; Z on Top&quot;</li>
<li>Lowesthighest: &quot; niedrigste am oberen &quot; oberen Rand  /  &quot;&quot;</li>
<li>Oldestlatest: &quot; älteste oben nach oben &quot;  /  &quot;&quot;</li>
<li>Smallestmost: &quot; kleinste am oberen &quot; oberen Rand  /  &quot;&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>invitationtext</td>
<td>Dies ist optional. Der Text der Hilfe Zeichenfolge, der dem Benutzer als Anweisung für das Steuerelement oder die QuickInfo angezeigt wird (z.b. &quot; Name des Autors &quot; ). Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge. Verwenden Sie die indirekte Anzeige Zeichenfolge, da Sie lokalisiert werden kann. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>Ipropertydescription:: geteditinvitation</strong></a> gibt den aufgelösten Einladungstext zurück.</td>
</tr>
<tr class="even">
<td>hidelta Label</td>
<td>Dies ist optional. Die Standardeinstellung ist &quot;false&quot;. Gibt an, ob die Bezeichnung ausgeblendet ist.</td>
</tr>
</tbody>
</table>



 

 

 
