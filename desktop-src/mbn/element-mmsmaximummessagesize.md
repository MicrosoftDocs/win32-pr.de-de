---
description: MmsMaximumMessageSize
MS-HAID: WWAN\_profile\_v4.element\_MmsMaximumMessageSize
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsMaximumMessageSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5b020e7fd6ad4f39bd488c3af0ef14a3aab1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214704"
---
# <a name="span-idwwan_profile_v4element_mmsmaximummessagesizespanmmsmaximummessagesize"></a><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>Mmsmaximummessagesize

Gibt die maximale Größe von MMS-Nachrichten in Kilobyte an. Dies ist optional.

## <a name="element-hierarchy"></a>Elementhierarchie

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmsMaximumMessageSize>**

## <a name="syntax"></a>Syntax

``` syntax
<MmsMaximumMessageSize>

  nonNegativeInteger

</MmsMaximumMessageSize>
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
<td><a href="element-mmsconfiguration.md">MMSConfiguration</a></td>
<td><p>Konfigurationsinformationen für den Multimedia Messaging Service (MMS).</p>
<p>Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil über die folgenden Einstellungen verfügen.</p>
<ul>
<li>Das <a href="element-name.md"><strong>Name</strong></a> -Element muss einen systemweiten eindeutigen Namen enthalten.</li>
<li>Der <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>profilekreationtype</strong></a> muss auf " <strong>userprovisioned</strong>" festgelegt werden.</li>
<li>Die <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>simiccid</strong></a> muss die ICCID der SIM enthalten, für die dieses Profil vorgesehen ist.</li>
<li>Der <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> muss auf " <strong>Manual</strong>" festgelegt werden.</li>
<li>Die zugehörige Ziel <a href="element-purposegroupguid.md"><strong>Gruppen-ID</strong></a> muss die GUID für die MMS-Zweck Gruppe enthalten.</li>
<li><a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>Isadditionalpdpcontextprofile</strong></a> muss auf " <strong>true</strong>" festgelegt werden.</li>
</ul></td>
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

 

 
