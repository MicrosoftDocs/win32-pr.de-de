---
description: Mbnprofileext- \/ Kontext (v4)
MS-HAID: WWAN\_profile\_v4.element\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Kontext
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eff61884-1d37-4e1a-85f0-2fadf14227ac
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8ec231b5d7e2769d86262864e0b9a53621c36a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348169"
---
# <a name="span-idwwan_profile_v4element_contextspanmbnprofileextcontext-v4"></a><span data-ttu-id="e1cfd-103"><span id="WWAN_profile_v4.element_Context"></span>Mbnprofileext- \/ Kontext (v4)</span><span class="sxs-lookup"><span data-stu-id="e1cfd-103"><span id="WWAN_profile_v4.element_Context"></span>MBNProfileExt\/Context (v4)</span></span>

<span data-ttu-id="e1cfd-104">Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="e1cfd-105">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="e1cfd-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="e1cfd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1cfd-106">Syntax</span></span>

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

### <a name="key"></a><span data-ttu-id="e1cfd-107">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e1cfd-107">Key</span></span>

<span data-ttu-id="e1cfd-108">`?`   optional (0 (null) oder eins)</span><span class="sxs-lookup"><span data-stu-id="e1cfd-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="e1cfd-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e1cfd-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="e1cfd-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="e1cfd-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="e1cfd-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="e1cfd-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e1cfd-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cfd-113">Untergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="e1cfd-113">Child Element</span></span></th>
<th><span data-ttu-id="e1cfd-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1cfd-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cfd-115"><a href="element-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="e1cfd-115"><a href="element-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="e1cfd-116">Identifiziert die APN-oder Dial-Zeichenfolge, die zum Herstellen einer Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="e1cfd-117">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>accessstring</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cfd-118"><a href="element-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="e1cfd-118"><a href="element-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="e1cfd-119">>Gibt das Authentifizierungsprotokoll an, das zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="e1cfd-120">Beachten Sie, dass in v4 ein neuer-Enumerationswert für dieses Element verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="e1cfd-121"><strong>Autoselection</strong> bedeutet, dass ein Authentifizierungsprotokoll von niedrigeren Ebenen ausgewählt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="e1cfd-122">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>authprotocol</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cfd-123"><a href="element-compression.md">Komprimierung</a></span><span class="sxs-lookup"><span data-stu-id="e1cfd-123"><a href="element-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="e1cfd-124">Gibt an, ob die Komprimierung im Daten Link für Header und Datenübertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="e1cfd-125">Weitere Informationen finden Sie in der Dokumentation für das v1- <a href="../mbn/schema-compression-contexttype-element.md"><strong>Komprimierungs</strong></a> Element.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cfd-126"><a href="element-iptype.md">Iptype</a></span><span class="sxs-lookup"><span data-stu-id="e1cfd-126"><a href="element-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="e1cfd-127">Gibt den IP-Typ an, der für diese Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="e1cfd-128">Dieses Element ist neu in v4 des Schemas.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="e1cfd-129">Das-Element kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cfd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e1cfd-130">Value</span></span></th>
<th><span data-ttu-id="e1cfd-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e1cfd-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cfd-132">Standard</span><span class="sxs-lookup"><span data-stu-id="e1cfd-132">Default</span></span></td>
<td><span data-ttu-id="e1cfd-133">Der IP-Typ muss von niedrigeren Ebenen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cfd-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="e1cfd-134">IPv4</span></span></td>
<td><span data-ttu-id="e1cfd-135">IPv4 verwenden</span><span class="sxs-lookup"><span data-stu-id="e1cfd-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cfd-136">IPv6</span><span class="sxs-lookup"><span data-stu-id="e1cfd-136">IPv6</span></span></td>
<td><span data-ttu-id="e1cfd-137">IPv6 verwenden</span><span class="sxs-lookup"><span data-stu-id="e1cfd-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cfd-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="e1cfd-138">IPv4v6</span></span></td>
<td><span data-ttu-id="e1cfd-139">Verwenden Sie IPv4 und/oder IPv6 als verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cfd-140">Xlat</span><span class="sxs-lookup"><span data-stu-id="e1cfd-140">XLAT</span></span></td>
<td><span data-ttu-id="e1cfd-141">Verwenden von 464xlat zum Tunneln von IPv4 über IPv6-Netzwerke</span><span class="sxs-lookup"><span data-stu-id="e1cfd-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cfd-142"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="e1cfd-142"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="e1cfd-143">Anmelde Informationen für eine Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="e1cfd-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e1cfd-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cfd-145">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="e1cfd-145">Parent Element</span></span></th>
<th><span data-ttu-id="e1cfd-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1cfd-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cfd-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="e1cfd-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="e1cfd-148">Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="e1cfd-149">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="e1cfd-150">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="e1cfd-151">Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cfd-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="e1cfd-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="e1cfd-153">Modem-DM-Konfigurations Profil.</span><span class="sxs-lookup"><span data-stu-id="e1cfd-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="e1cfd-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1cfd-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1cfd-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1cfd-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



