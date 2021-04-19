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
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span data-ttu-id="0c4f4-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>"Mudedmconfigprofile"</span><span class="sxs-lookup"><span data-stu-id="0c4f4-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span></span>

<span data-ttu-id="0c4f4-104">Modem-DM-Konfigurations Profil.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-104">Modem DM configuration profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="0c4f4-105">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="0c4f4-105">Element hierarchy</span></span>

**<ModemDMConfigProfile>**

## <a name="syntax"></a><span data-ttu-id="0c4f4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c4f4-106">Syntax</span></span>

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

### <a name="key"></a><span data-ttu-id="0c4f4-107">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="0c4f4-107">Key</span></span>

<span data-ttu-id="0c4f4-108">`?`   optional (0 (null) oder eins)</span><span class="sxs-lookup"><span data-stu-id="0c4f4-108">`?`   optional (zero or one)</span></span>

<span data-ttu-id="0c4f4-109">`*`   optional (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="0c4f4-109">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="0c4f4-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0c4f4-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="0c4f4-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="0c4f4-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="0c4f4-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="0c4f4-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c4f4-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c4f4-114">Untergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="0c4f4-114">Child Element</span></span></th>
<th><span data-ttu-id="0c4f4-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c4f4-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c4f4-116"><a href="element-1-adminenable.md">Adminenable</a></span><span class="sxs-lookup"><span data-stu-id="0c4f4-116"><a href="element-1-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="0c4f4-117">Gibt an, ob das Profil administrativ aktiviert ist. Dies ist ein neues Element für v4.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-117">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c4f4-118"><a href="element-1-adminroamcontrol.md">Adminroamcontrol</a></span><span class="sxs-lookup"><span data-stu-id="0c4f4-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="0c4f4-119">Gibt an, ob das Profil administrativ durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-119">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="0c4f4-120">Dieses Element ist neu für v4.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-120">This element is new for v4.</span></span> <span data-ttu-id="0c4f4-121">Der Wert dieses Elements ist ein <a href="simpletype-roamcontroltype.md"><strong>roamcontroltype</strong></a> -Wert.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-121">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="0c4f4-122">Dies ist ein optionales Element. Wenn kein Wert angegeben wird, ist <strong>allroamallowed</strong> der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-122">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c4f4-123"><a href="element-1-apnid.md">Apnid</a></span><span class="sxs-lookup"><span data-stu-id="0c4f4-123"><a href="element-1-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="0c4f4-124">Eine APN-ID, die diesem Profil zugeordnet ist. Dieses Element ist neu in v4 und optional.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-124">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c4f4-125"><a href="element-1-context.md">Context</a></span><span class="sxs-lookup"><span data-stu-id="0c4f4-125"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="0c4f4-126">Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-126">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c4f4-127"><a href="element-1-name.md">Name</a></span><span class="sxs-lookup"><span data-stu-id="0c4f4-127"><a href="element-1-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="0c4f4-128">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-128">The name of the profile.</span></span> <span data-ttu-id="0c4f4-129">Weitere Informationen finden Sie in der Dokumentation für das v1- <a href="../mbn/schema-name-mbnprofile-element.md"><strong>namens</strong></a> Element.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-129">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c4f4-130"><a href="element-oemconnectionid.md">Oemconnectionid</a></span><span class="sxs-lookup"><span data-stu-id="0c4f4-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span></span></td>
<td><p><span data-ttu-id="0c4f4-131">Die OEM-Verbindungs-ID für die Modem-DM-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-131">The OEM connection ID for the modem DM configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c4f4-132"><a href="element-1-profilecreationtype.md">Profilekreationtype (in "mudedmconfigprofile")</a></span><span class="sxs-lookup"><span data-stu-id="0c4f4-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></span></span></td>
<td><p><span data-ttu-id="0c4f4-133">Gibt an, wie dieses Modem-DM-Profil erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-133">Specifies how this modem DM profile was created.</span></span></p>
<p><span data-ttu-id="0c4f4-134">Dieser Wert wird verwendet, um zu entscheiden, ob ein Benutzer das Profil löschen kann.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-134">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="0c4f4-135">Benutzer können nur <strong>Benutzer bereitgestellte</strong> Profile löschen.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-135">Users can only delete <strong>UserProvisioned</strong> profiles.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c4f4-136"><a href="element-1-roamapplicability.md">Roamanwendbarkeit</a></span><span class="sxs-lookup"><span data-stu-id="0c4f4-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="0c4f4-137">Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle roamingbedingung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-137">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="0c4f4-138">Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-138">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="0c4f4-139">Der Wert dieses Elements muss ein gültiger <a href="simpletype-roamapplicabilitytype.md"><strong>roamapplicabilitytype</strong></a> -Wert sein.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-139">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c4f4-140"><a href="element-1-simiccid.md">Simiccid</a></span><span class="sxs-lookup"><span data-stu-id="0c4f4-140"><a href="element-1-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="0c4f4-141">Die SIM-identikations Nummer für GSM-Geräte.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-141">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="0c4f4-142">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>simiccid-</strong></a> Element.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-142">For more details , see the documentation for the v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="0c4f4-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c4f4-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="0c4f4-144">Dieses äußerste (Dokument-) Element darf nicht in anderen Elementen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-144">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4f4-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c4f4-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c4f4-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c4f4-146">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



