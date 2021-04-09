---
description: Islongstandingadditionalpdpcontextprofile
MS-HAID: WWAN\_profile\_v4.element\_IsLongStandingAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Islongstandingadditionalpdpcontextprofile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a6ab30af9e71b8e9bde8284137c6bff86355f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862771"
---
# <a name="span-idwwan_profile_v4element_islongstandingadditionalpdpcontextprofilespanislongstandingadditionalpdpcontextprofile"></a><span data-ttu-id="2eab5-103"><span id="WWAN_profile_v4.element_IsLongStandingAdditionalPdpContextProfile"></span>Islongstandingadditionalpdpcontextprofile</span><span class="sxs-lookup"><span data-stu-id="2eab5-103"><span id="WWAN_profile_v4.element_IsLongStandingAdditionalPdpContextProfile"></span>IsLongStandingAdditionalPdpContextProfile</span></span>

<span data-ttu-id="2eab5-104">Gibt an, dass dieses Profil ein langjähriges zusätzliches PDP-Kontext Profil ist. Wenn der Wert dieses Elements " **true**" ist, muss [**isadditionalpdpcontextprofile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) ebenfalls auf " **true**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2eab5-104">Specifies that this profile is a long-standing additional PDP context profile.If the value of this element is **true**, then [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) must also be set to **true**.</span></span> <span data-ttu-id="2eab5-105">Dies ist ein neues Element für v4.</span><span class="sxs-lookup"><span data-stu-id="2eab5-105">This is a new element for v4.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="2eab5-106">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="2eab5-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<IsLongStandingAdditionalPdpContextProfile>**

## <a name="syntax"></a><span data-ttu-id="2eab5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eab5-107">Syntax</span></span>

``` syntax
<IsLongStandingAdditionalPdpContextProfile>

  boolean

</IsLongStandingAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="2eab5-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2eab5-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="2eab5-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="2eab5-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="2eab5-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="2eab5-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="2eab5-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2eab5-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="2eab5-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="2eab5-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="2eab5-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2eab5-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2eab5-114">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="2eab5-114">Parent Element</span></span></th>
<th><span data-ttu-id="2eab5-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2eab5-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2eab5-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="2eab5-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="2eab5-117">Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="2eab5-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="2eab5-118">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="2eab5-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="2eab5-119">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2eab5-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="2eab5-120">Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="2eab5-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="2eab5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2eab5-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2eab5-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="2eab5-122">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
