---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b370c353cee43a001a35b8e5bd407547818d705e21334aff07d41e854f334cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066360"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

Modem-DM-Konfigurationsprofil.

## <a name="element-hierarchy"></a>Elementhierarchie

**<ModemDMConfigProfile>**

## <a name="syntax"></a>Syntax

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a>Key

`?`   optional (null oder eins)

`*`   optional (null oder mehr)

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
<td><a href="element-1-adminenable.md">AdminEnable</a></td>
<td><p>Gibt an, ob das Profil administratorisch aktiviert ist. Dies ist ein neues Element für v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Gibt an, ob das Profil verwaltungsgesteuert roaminggesteuert ist. Dieses Element ist neu für v4. Der Wert dieses Elements ist ein <a href="simpletype-roamcontroltype.md"><strong>roamControlType-Wert.</strong></a> Dies ist ein optionales Element. Wenn kein Wert angegeben wird, ist <strong>AllRoamAllowed</strong> der Standardwert.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-apnid.md">ApnID</a></td>
<td><p>Eine diesem Profil zugeordnete APN-ID. Dieses Element ist neu in v4 und optional.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-context.md">Context</a></td>
<td><p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-name.md">Name</a></td>
<td><p>Der Name des Profils. Weitere Informationen finden Sie in der Dokumentation zum <a href="../mbn/schema-name-mbnprofile-element.md"><strong>v1-Element Name.</strong></a></p></td>
</tr>
<tr class="even">
<td><a href="element-oemconnectionid.md">OemConnectionId</a></td>
<td><p>Die OEM-Verbindungs-ID für die Modem-DM-Konfiguration.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></td>
<td><p>Gibt an, wie dieses Modem-DM-Profil erstellt wurde.</p>
<p>Dieser Wert wird verwendet, um zu entscheiden, ob ein Benutzer das Profil löschen kann. Benutzer können nur <strong>UserProvisioned-Profile</strong> löschen.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-roamapplicability.md">RoamApplicability</a></td>
<td><p>Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle Roamingbedingung die angegebene ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden. Der Wert dieses Elements muss ein gültiger <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType-Wert</strong></a> sein.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-simiccid.md">SimIccID</a></td>
<td><p>Die SIM-Identifikationsnummer für GSM-Geräte. Weitere Informationen finden Sie in der Dokumentation für das <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID-Element</strong></a> v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

Dieses äußerste Element (Dokument) darf nicht in anderen Elementen enthalten sein.

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

 

 



