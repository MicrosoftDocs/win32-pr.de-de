---
description: MmscUrl
MS-HAID: WWAN\_profile\_v4.element\_MmscUrl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscUrl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2c2e21e466a0c81b42b06ef782eeef3a35f83537f934fbe2268c4c58383646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881681"
---
# <a name="span-idwwan_profile_v4element_mmscurlspanmmscurl"></a><span id="WWAN_profile_v4.element_MmscUrl"></span>MmscUrl

Gibt die URL des MMSC-Servers für das Gerät an. Optional.

## <a name="element-hierarchy"></a>Elementhierarchie

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmscUrl>**

## <a name="syntax"></a>Syntax

``` syntax
<MmscUrl>

  anyURI

</MmscUrl>
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
<td><a href="element-mmsconfiguration.md">MmsConfiguration</a></td>
<td><p>Konfigurationsinformationen für Multimedia Messaging Service (MMS).</p>
<p>Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil die folgenden Einstellungen aufweisen.</p>
<ul>
<li>Das <a href="element-name.md"><strong>Name-Element</strong></a> muss einen systemweit eindeutigen Namen enthalten.</li>
<li><a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> muss auf <strong>UserProvisioned</strong>festgelegt werden.</li>
<li>Die <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> muss die MUSTID der SIM enthalten, für die dieses Profil vorgesehen ist.</li>
<li><a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> muss auf <strong>Manuell</strong>festgelegt werden.</li>
<li><a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> muss die GUID für die MMS-Zweckgruppe enthalten.</li>
<li><a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> muss auf <strong>true</strong>festgelegt werden.</li>
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

 

 
