---
description: Wdemdmconfigprofile \/ roamanwendbarkeit (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Roamanwendbarkeit (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d78618598b758d4c2654f0f2911637e638aacf
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388796"
---
# <a name="span-idwwan_profile_v4element_1_roamapplicabilityspanmodemdmconfigprofileroamapplicability-v4"></a><span data-ttu-id="ba485-103"><span id="WWAN_profile_v4.element_1_RoamApplicability"></span>Wdemdmconfigprofile \/ roamanwendbarkeit (v4)</span><span class="sxs-lookup"><span data-stu-id="ba485-103"><span id="WWAN_profile_v4.element_1_RoamApplicability"></span>ModemDMConfigProfile\/RoamApplicability (v4)</span></span>

<span data-ttu-id="ba485-104">Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle roamingbedingung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ba485-104">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="ba485-105">Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ba485-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="ba485-106">Der Wert dieses Elements muss ein gültiger [**roamapplicabilitytype**](simpletype-roamapplicabilitytype.md) -Wert sein.</span><span class="sxs-lookup"><span data-stu-id="ba485-106">The value of this element must be a valid [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="ba485-107">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="ba485-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a><span data-ttu-id="ba485-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba485-108">Syntax</span></span>

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="ba485-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ba485-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="ba485-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="ba485-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="ba485-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba485-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="ba485-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba485-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="ba485-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba485-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="ba485-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba485-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba485-115">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ba485-115">Parent Element</span></span></th>
<th><span data-ttu-id="ba485-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba485-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ba485-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="ba485-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="ba485-118">Modem-DM-Konfigurations Profil.</span><span class="sxs-lookup"><span data-stu-id="ba485-118">Modem DM configuration profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba485-119"><a href="element-profileconditionedon.md">Profileconditionedon</a></span><span class="sxs-lookup"><span data-stu-id="ba485-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="ba485-120">Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="ba485-120">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="ba485-121">Dieses Element ist neu für v4.</span><span class="sxs-lookup"><span data-stu-id="ba485-121">This element is new for v4.</span></span> <span data-ttu-id="ba485-122">Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unterschiedlichen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="ba485-122">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="ba485-123">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ba485-123">This element is optional.</span></span> <span data-ttu-id="ba485-124">Wenn Sie ihn nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="ba485-124">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="ba485-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba485-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba485-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba485-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



