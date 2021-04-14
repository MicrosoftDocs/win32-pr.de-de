---
description: "\"Zielstregroupguid\""
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroupGuid
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: "\"Zielstregroupguid\""
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d20d6c9d1687ea0e3fca344fd3b534ccc0b3ee57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393526"
---
# <a name="span-idwwan_profile_v4element_purposegroupguidspanpurposegroupguid"></a><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>"Zielstregroupguid"

Stellt ein Profil in einer Zweck Gruppe von Profilen dar.

Profile werden durch Ihren [**guidtype**](simpletype-guidtype.md) -Wert angegeben.

Vier GUID-Werte werden definiert, wie in der folgenden Tabelle aufgeführt.

| Zweck Gruppe | GUID                                 |
|---------------|--------------------------------------|
| Internet      | 3e5545d2-1137-4dc8-a198-33F & 1c657515f |
| mms           | 53e2c5d3-D13C-4068-AA38-9c48ff2e55a8 |
| IMS           | 474d66ed-0e4b-476b-A455-19bb1239ed13 |
| SUPL          | 6d42669l-52a9-408e-9493-1071dcc437bd |

 

## <a name="element-hierarchy"></a>Elementhierarchie

[<MBNProfileExt>](element-mbnprofileext.md)  
[<PurposeGroups>](element-purposegroups.md)  
**<PurposeGroupGuid>**

## <a name="syntax"></a>Syntax

``` syntax
<PurposeGroupGuid>

  guidType

</PurposeGroupGuid>
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
<td><a href="element-purposegroups.md">Zielstregruppen</a></td>
<td><p>Eine optionale Liste der Gruppen von Profilen, wobei jede Gruppe Profile enthält, die für einen allgemeinen Zweck verwendet werden.</p>
<p>Dieses Element ist neu für V4 des Schemas.</p>
<p>Ein Profil kann in mehreren Gruppen aufgelistet werden.</p></td>
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

 

 



