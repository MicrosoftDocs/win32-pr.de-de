---
description: Kontext von "fidemdmconfigprofile" \/ (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Kontext (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 133f48d9c9a1c9dd9f0e04f59d5e35478caa9227
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388847"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span data-ttu-id="d5253-103"><span id="WWAN_profile_v4.element_1_Context"></span>Kontext von "fidemdmconfigprofile" \/ (v4)</span><span class="sxs-lookup"><span data-stu-id="d5253-103"><span id="WWAN_profile_v4.element_1_Context"></span>ModemDMConfigProfile\/Context (v4)</span></span>

<span data-ttu-id="d5253-104">Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d5253-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="d5253-105">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="d5253-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="d5253-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5253-106">Syntax</span></span>

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a><span data-ttu-id="d5253-107">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d5253-107">Key</span></span>

<span data-ttu-id="d5253-108">`?`   optional (0 (null) oder eins)</span><span class="sxs-lookup"><span data-stu-id="d5253-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="d5253-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d5253-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="d5253-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="d5253-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="d5253-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5253-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="d5253-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5253-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5253-113">Untergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d5253-113">Child Element</span></span></th>
<th><span data-ttu-id="d5253-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5253-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5253-115"><a href="element-1-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="d5253-115"><a href="element-1-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="d5253-116">Identifiziert die APN-oder Dial-Zeichenfolge, die zum Herstellen einer Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5253-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="d5253-117">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>accessstring</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="d5253-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5253-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="d5253-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="d5253-119">>Gibt das Authentifizierungsprotokoll an, das zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5253-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="d5253-120">Beachten Sie, dass in v4 ein neuer-Enumerationswert für dieses Element verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d5253-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="d5253-121"><strong>Autoselection</strong> bedeutet, dass ein Authentifizierungsprotokoll von niedrigeren Ebenen ausgewählt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d5253-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="d5253-122">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>authprotocol</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="d5253-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5253-123"><a href="element-1-compression.md">Komprimierung</a></span><span class="sxs-lookup"><span data-stu-id="d5253-123"><a href="element-1-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="d5253-124">Gibt an, ob die Komprimierung im Daten Link für Header und Datenübertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5253-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="d5253-125">Weitere Informationen finden Sie in der Dokumentation für das v1- <a href="../mbn/schema-compression-contexttype-element.md"><strong>Komprimierungs</strong></a> Element.</span><span class="sxs-lookup"><span data-stu-id="d5253-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5253-126"><a href="element-1-iptype.md">Iptype</a></span><span class="sxs-lookup"><span data-stu-id="d5253-126"><a href="element-1-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="d5253-127">Gibt den IP-Typ an, der für diese Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5253-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="d5253-128">Dieses Element ist neu in v4 des Schemas.</span><span class="sxs-lookup"><span data-stu-id="d5253-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="d5253-129">Das-Element kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d5253-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d5253-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d5253-130">Value</span></span></th>
<th><span data-ttu-id="d5253-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d5253-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5253-132">Standard</span><span class="sxs-lookup"><span data-stu-id="d5253-132">Default</span></span></td>
<td><span data-ttu-id="d5253-133">Der IP-Typ muss von niedrigeren Ebenen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="d5253-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5253-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="d5253-134">IPv4</span></span></td>
<td><span data-ttu-id="d5253-135">IPv4 verwenden</span><span class="sxs-lookup"><span data-stu-id="d5253-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5253-136">IPv6</span><span class="sxs-lookup"><span data-stu-id="d5253-136">IPv6</span></span></td>
<td><span data-ttu-id="d5253-137">IPv6 verwenden</span><span class="sxs-lookup"><span data-stu-id="d5253-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5253-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="d5253-138">IPv4v6</span></span></td>
<td><span data-ttu-id="d5253-139">Verwenden Sie IPv4 und/oder IPv6 als verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5253-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5253-140">Xlat</span><span class="sxs-lookup"><span data-stu-id="d5253-140">XLAT</span></span></td>
<td><span data-ttu-id="d5253-141">Verwenden von 464xlat zum Tunneln von IPv4 über IPv6-Netzwerke</span><span class="sxs-lookup"><span data-stu-id="d5253-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5253-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="d5253-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="d5253-143">Anmelde Informationen für eine Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d5253-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="d5253-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5253-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5253-145">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d5253-145">Parent Element</span></span></th>
<th><span data-ttu-id="d5253-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5253-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5253-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="d5253-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="d5253-148">Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="d5253-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="d5253-149">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="d5253-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="d5253-150">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d5253-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="d5253-151">Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="d5253-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5253-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="d5253-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="d5253-153">Modem-DM-Konfigurations Profil.</span><span class="sxs-lookup"><span data-stu-id="d5253-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="d5253-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5253-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5253-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5253-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



