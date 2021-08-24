---
description: MBNProfileExt \/ RoamApplicability (v4)
MS-HAID: WWAN\_profile\_v4.element\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RoamApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4515f8842d87361ce54cbd3e68de4e6d0e805caa7b46b675a086a83b84741c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607220"
---
# <a name="span-idwwan_profile_v4element_roamapplicabilityspanmbnprofileextroamapplicability-v4"></a><span id="WWAN_profile_v4.element_RoamApplicability"></span>MBNProfileExt \/ RoamApplicability (v4)

Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle Roamingbedingung die angegebene ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden. Der Wert dieses Elements muss ein gültiger [**roamApplicabilityType-Wert**](simpletype-roamapplicabilitytype.md) sein.

## <a name="element-hierarchy"></a>Elementhierarchie

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a>Syntax

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Übergeordnetes Element</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Modem-DM-Konfigurationsprofil.</p></td>
</tr>
<tr class="even">
<td><a href="element-profileconditionedon.md">ProfileConditionedOn</a></td>
<td><p>Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</p>
<p>Dieses Element ist neu für v4. Sie können mehrere Profile angeben, die unter verschiedenen Bedingungen gelten, und das richtige Profil automatisch verwenden, wenn es anwendbar ist. Dieses Element ist optional. Wenn Sie es nicht angeben, ist das Profil immer in Bezug auf die aufgeführten Bedingungen anwendbar.</p></td>
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

 

 



