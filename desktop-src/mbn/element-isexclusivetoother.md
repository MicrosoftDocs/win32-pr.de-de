---
description: Isexclusivean other
MS-HAID: WWAN\_profile\_v4.element\_IsExclusiveToOther
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Isexclusivean other
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a948ad9b6a457f74e98eab745d851bdd2399c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359826"
---
# <a name="span-idwwan_profile_v4element_isexclusivetootherspanisexclusivetoother"></a><span data-ttu-id="a7ee0-103"><span id="WWAN_profile_v4.element_IsExclusiveToOther"></span>Isexclusivean other</span><span class="sxs-lookup"><span data-stu-id="a7ee0-103"><span id="WWAN_profile_v4.element_IsExclusiveToOther"></span>IsExclusiveToOther</span></span>

<span data-ttu-id="a7ee0-104">Gibt an, dass dieses Profil für andere Profile desselben Profil Satzes exklusiv ist. Dieses Element ist neu für v4.</span><span class="sxs-lookup"><span data-stu-id="a7ee0-104">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="a7ee0-105">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="a7ee0-105">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<IsExclusiveToOther>**

## <a name="syntax"></a><span data-ttu-id="a7ee0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7ee0-106">Syntax</span></span>

``` syntax
<IsExclusiveToOther>

  boolean

</IsExclusiveToOther>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="a7ee0-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a7ee0-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="a7ee0-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="a7ee0-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="a7ee0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7ee0-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="a7ee0-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7ee0-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="a7ee0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7ee0-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="a7ee0-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7ee0-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7ee0-113">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a7ee0-113">Parent Element</span></span></th>
<th><span data-ttu-id="a7ee0-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7ee0-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7ee0-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="a7ee0-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="a7ee0-116">Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="a7ee0-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="a7ee0-117">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="a7ee0-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="a7ee0-118">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a7ee0-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="a7ee0-119">Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="a7ee0-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="a7ee0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7ee0-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7ee0-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7ee0-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



