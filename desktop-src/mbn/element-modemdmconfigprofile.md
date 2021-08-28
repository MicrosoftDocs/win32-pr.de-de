---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80684cdf2d47d203318afbfd7b5e6bc02de1d3dc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982743"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

Modem DM-Konfigurationsprofil.

## <a name="element-hierarchy"></a>Elementhierarchie

**&lt;ModemDMConfigProfile&gt;**

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

`?`   optional (null oder eins)

`*`   optional (null oder mehr)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente


| Untergeordnetes Element | BESCHREIBUNG | 
|---------------|-------------|
| <a href="element-1-adminenable.md">AdminEnable</a> | <p>Gibt an, ob das Profil administratorisch aktiviert ist. Dies ist ein neues Element für v4.</p> | 
| <a href="element-1-adminroamcontrol.md">AdminRoamControl</a> | <p>Gibt an, ob das Profil vom Administrator per Roaming gesteuert wird. Dieses Element ist neu für v4. Der Wert dieses Elements ist ein <a href="simpletype-roamcontroltype.md"><strong>roamControlType-Wert.</strong></a> Dies ist ein optionales Element. Wenn kein Wert angegeben wird, ist <strong>AllRoamAllowed</strong> der Standardwert.</p> | 
| <a href="element-1-apnid.md">ApnID</a> | <p>Eine DIESEM Profil zugeordnete APN-ID. Dieses Element ist in v4 neu und optional.</p> | 
| <a href="element-1-context.md">Context</a> | <p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p> | 
| <a href="element-1-name.md">Name</a> | <p>Der Name des Profils. Weitere Informationen finden Sie in der <a href="../mbn/schema-name-mbnprofile-element.md"><strong></strong></a> Dokumentation für das v1 Name-Element.</p> | 
| <a href="element-oemconnectionid.md">OemConnectionId</a> | <p>Die OEM-Verbindungs-ID für die Dm-Konfiguration des Modems.</p> | 
| <a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a> | <p>Gibt an, wie dieses Modem-DM-Profil erstellt wurde.</p><p>Dieser Wert wird verwendet, um zu entscheiden, ob ein Benutzer das Profil löschen kann. Benutzer können nur <strong>UserProvisioned-Profile</strong> löschen.</p> | 
| <a href="element-1-roamapplicability.md">RoamApplicability</a> | <p>Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle Roamingbedingung die angegebene ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden. Der Wert dieses Elements muss ein gültiger <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType-Wert</strong></a> sein.</p> | 
| <a href="element-1-simiccid.md">SimIccID</a> | <p>Die SIM-Identifikationsnummer für GSM-Geräte. Weitere Informationen finden Sie in der Dokumentation für das <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>v1 SimIccID-Element.</strong></a></p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

Dieses äußerste Element (Dokument) darf nicht in anderen Elementen enthalten sein.

## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



