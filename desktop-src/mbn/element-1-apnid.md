---
description: "\"Mudedmconfigprofile\" \\/ apnid (v4)"
MS-HAID: WWAN\_profile\_v4.element\_1\_ApnID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Apnid (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3838a632359fcdf7bc32004103f6f90163d988
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388861"
---
# <a name="span-idwwan_profile_v4element_1_apnidspanmodemdmconfigprofileapnid-v4"></a><span id="WWAN_profile_v4.element_1_ApnID"></span>"Mudedmconfigprofile" \/ apnid (v4)

Eine APN-ID, die diesem Profil zugeordnet ist. Dieses Element ist neu in v4 und optional.

## <a name="element-hierarchy"></a>Elementhierarchie

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<ApnID\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<ApnID\>**

## <a name="syntax"></a>Syntax

``` syntax
<ApnID>

  decimal

</ApnID>
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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements. Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</p>
<p>Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt. Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</p></td>
</tr>
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Modem-DM-Konfigurations Profil.</p></td>
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

 

 



