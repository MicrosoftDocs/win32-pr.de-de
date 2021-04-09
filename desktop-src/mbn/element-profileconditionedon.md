---
description: Profileconditionedon
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Profileconditionedon
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129028"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>Profileconditionedon

Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.

Dieses Element ist neu für v4. Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unterschiedlichen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist. Dieses Element ist optional. Wenn Sie ihn nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.

## <a name="element-hierarchy"></a>Elementhierarchie

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a>Syntax

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a>Schlüssel

`?`   optional (0 (null) oder eins)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Untergeordnetes Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-cellularclass.md">Cellularclass</a></td>
<td><p>Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle Mobilfunk-Klasse das angegebene ist. Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</p></td>
</tr>
<tr class="even">
<td><a href="element-imsi.md">IMSI</a></td>
<td><p>Gibt an, dass dieses Profil nur aktiv ist, wenn der aktuelle IMSI-Wert, der in der ICCID verwendet wird, der angegebene Wert ist. Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</p></td>
</tr>
<tr class="odd">
<td><a href="element-iwlanapplicability.md">Iwlananwendbarkeit</a></td>
<td><p>Gibt an, dass dieses Profil nur aktiv ist, wenn es mit einem iWLAN-Netzwerk verbunden ist. Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren. Der Wert dieses Elements muss ein gültiger <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanapplicabilitytype</strong></a> -Wert sein.</p></td>
</tr>
<tr class="even">
<td><a href="element-ratapplicability.md">Ratanwendbarkeit</a></td>
<td><p>Gibt an, dass dieses Profil nur aktiv ist, wenn der rattyp das angegebene ist. Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</p></td>
</tr>
<tr class="odd">
<td><a href="element-roamapplicability.md">Roamanwendbarkeit</a></td>
<td><p>Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle roamingbedingung festgelegt ist. Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren. Der Wert dieses Elements muss ein gültiger <a href="simpletype-roamapplicabilitytype.md"><strong>roamapplicabilitytype</strong></a> -Wert sein.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Übergeordnetes Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements. Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</p>
<p>Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt. Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



