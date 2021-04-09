---
description: Profileconditionedon
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Profileconditionedon
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129028"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span data-ttu-id="1b0d9-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>Profileconditionedon</span><span class="sxs-lookup"><span data-stu-id="1b0d9-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span></span>

<span data-ttu-id="1b0d9-104">Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-104">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span>

<span data-ttu-id="1b0d9-105">Dieses Element ist neu für v4.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-105">This element is new for v4.</span></span> <span data-ttu-id="1b0d9-106">Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unterschiedlichen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-106">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="1b0d9-107">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-107">This element is optional.</span></span> <span data-ttu-id="1b0d9-108">Wenn Sie ihn nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-108">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1b0d9-109">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="1b0d9-109">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a><span data-ttu-id="1b0d9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b0d9-110">Syntax</span></span>

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a><span data-ttu-id="1b0d9-111">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="1b0d9-111">Key</span></span>

<span data-ttu-id="1b0d9-112">`?`   optional (0 (null) oder eins)</span><span class="sxs-lookup"><span data-stu-id="1b0d9-112">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1b0d9-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1b0d9-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1b0d9-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="1b0d9-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1b0d9-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1b0d9-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b0d9-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b0d9-117">Untergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1b0d9-117">Child Element</span></span></th>
<th><span data-ttu-id="1b0d9-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b0d9-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b0d9-119"><a href="element-cellularclass.md">Cellularclass</a></span><span class="sxs-lookup"><span data-stu-id="1b0d9-119"><a href="element-cellularclass.md">CellularClass</a></span></span></td>
<td><p><span data-ttu-id="1b0d9-120">Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle Mobilfunk-Klasse das angegebene ist.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-120">Specifies that this profile is active only when the current cellular class is the one specified.</span></span> <span data-ttu-id="1b0d9-121">Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-121">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b0d9-122"><a href="element-imsi.md">IMSI</a></span><span class="sxs-lookup"><span data-stu-id="1b0d9-122"><a href="element-imsi.md">IMSI</a></span></span></td>
<td><p><span data-ttu-id="1b0d9-123">Gibt an, dass dieses Profil nur aktiv ist, wenn der aktuelle IMSI-Wert, der in der ICCID verwendet wird, der angegebene Wert ist.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-123">Specifies that this profile is active only when the current IMSI being used in the ICCID is the one specified.</span></span> <span data-ttu-id="1b0d9-124">Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-124">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b0d9-125"><a href="element-iwlanapplicability.md">Iwlananwendbarkeit</a></span><span class="sxs-lookup"><span data-stu-id="1b0d9-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span></span></td>
<td><p><span data-ttu-id="1b0d9-126">Gibt an, dass dieses Profil nur aktiv ist, wenn es mit einem iWLAN-Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-126">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="1b0d9-127">Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-127">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="1b0d9-128">Der Wert dieses Elements muss ein gültiger <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanapplicabilitytype</strong></a> -Wert sein.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-128">The value of this element must be a valid <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b0d9-129"><a href="element-ratapplicability.md">Ratanwendbarkeit</a></span><span class="sxs-lookup"><span data-stu-id="1b0d9-129"><a href="element-ratapplicability.md">RATApplicability</a></span></span></td>
<td><p><span data-ttu-id="1b0d9-130">Gibt an, dass dieses Profil nur aktiv ist, wenn der rattyp das angegebene ist.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-130">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="1b0d9-131">Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-131">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b0d9-132"><a href="element-roamapplicability.md">Roamanwendbarkeit</a></span><span class="sxs-lookup"><span data-stu-id="1b0d9-132"><a href="element-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="1b0d9-133">Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle roamingbedingung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-133">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="1b0d9-134">Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-134">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="1b0d9-135">Der Wert dieses Elements muss ein gültiger <a href="simpletype-roamapplicabilitytype.md"><strong>roamapplicabilitytype</strong></a> -Wert sein.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-135">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1b0d9-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b0d9-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b0d9-137">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1b0d9-137">Parent Element</span></span></th>
<th><span data-ttu-id="1b0d9-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b0d9-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b0d9-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="1b0d9-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="1b0d9-140">Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-140">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="1b0d9-141">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-141">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="1b0d9-142">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-142">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="1b0d9-143">Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="1b0d9-143">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="1b0d9-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b0d9-144">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b0d9-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b0d9-145">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



