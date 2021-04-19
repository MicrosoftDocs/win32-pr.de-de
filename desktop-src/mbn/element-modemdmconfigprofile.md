---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350426"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>"Mudedmconfigprofile"

Modem-DM-Konfigurations Profil.

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

### <a name="key"></a>Schlüssel

`?`   optional (0 (null) oder eins)

`*`   optional (0 (null) oder mehr)

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
<td><a href="element-1-adminenable.md">Adminenable</a></td>
<td><p>Gibt an, ob das Profil administrativ aktiviert ist. Dies ist ein neues Element für v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-adminroamcontrol.md">Adminroamcontrol</a></td>
<td><p>Gibt an, ob das Profil administrativ durchlaufen wird. Dieses Element ist neu für v4. Der Wert dieses Elements ist ein <a href="simpletype-roamcontroltype.md"><strong>roamcontroltype</strong></a> -Wert. Dies ist ein optionales Element. Wenn kein Wert angegeben wird, ist <strong>allroamallowed</strong> der Standardwert.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-apnid.md">Apnid</a></td>
<td><p>Eine APN-ID, die diesem Profil zugeordnet ist. Dieses Element ist neu in v4 und optional.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-context.md">Context</a></td>
<td><p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-name.md">Name</a></td>
<td><p>Der Name des Profils. Weitere Informationen finden Sie in der Dokumentation für das v1- <a href="../mbn/schema-name-mbnprofile-element.md"><strong>namens</strong></a> Element.</p></td>
</tr>
<tr class="even">
<td><a href="element-oemconnectionid.md">Oemconnectionid</a></td>
<td><p>Die OEM-Verbindungs-ID für die Modem-DM-Konfiguration.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-profilecreationtype.md">Profilekreationtype (in "mudedmconfigprofile")</a></td>
<td><p>Gibt an, wie dieses Modem-DM-Profil erstellt wurde.</p>
<p>Dieser Wert wird verwendet, um zu entscheiden, ob ein Benutzer das Profil löschen kann. Benutzer können nur <strong>Benutzer bereitgestellte</strong> Profile löschen.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-roamapplicability.md">Roamanwendbarkeit</a></td>
<td><p>Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle roamingbedingung festgelegt ist. Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren. Der Wert dieses Elements muss ein gültiger <a href="simpletype-roamapplicabilitytype.md"><strong>roamapplicabilitytype</strong></a> -Wert sein.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-simiccid.md">Simiccid</a></td>
<td><p>Die SIM-identikations Nummer für GSM-Geräte. Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>simiccid-</strong></a> Element.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

Dieses äußerste (Dokument-) Element darf nicht in anderen Elementen enthalten sein.

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

 

 



