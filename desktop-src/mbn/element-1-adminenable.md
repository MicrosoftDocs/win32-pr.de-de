---
description: "\"Rodemdmconfigprofile\" \\/ adminenable (v4)"
MS-HAID: WWAN\_profile\_v4.element\_1\_AdminEnable
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Adminenable (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a20ab248c585e6f599ddb43e6c3f93183baf7373
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388875"
---
# <a name="span-idwwan_profile_v4element_1_adminenablespanmodemdmconfigprofileadminenable-v4"></a><span data-ttu-id="73090-103"><span id="WWAN_profile_v4.element_1_AdminEnable"></span>"Rodemdmconfigprofile" \/ adminenable (v4)</span><span class="sxs-lookup"><span data-stu-id="73090-103"><span id="WWAN_profile_v4.element_1_AdminEnable"></span>ModemDMConfigProfile\/AdminEnable (v4)</span></span>

<span data-ttu-id="73090-104">Gibt an, ob das Profil administrativ aktiviert ist. Dies ist ein neues Element für v4.</span><span class="sxs-lookup"><span data-stu-id="73090-104">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="73090-105">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="73090-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<AdminEnable\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<AdminEnable\>**

## <a name="syntax"></a><span data-ttu-id="73090-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="73090-106">Syntax</span></span>

``` syntax
<AdminEnable>

  boolean

</AdminEnable>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="73090-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="73090-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="73090-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="73090-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="73090-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="73090-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="73090-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73090-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="73090-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="73090-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="73090-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73090-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73090-113">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="73090-113">Parent Element</span></span></th>
<th><span data-ttu-id="73090-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73090-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73090-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="73090-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="73090-116">Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="73090-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="73090-117">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="73090-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="73090-118">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="73090-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="73090-119">Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="73090-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73090-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="73090-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="73090-121">Modem-DM-Konfigurations Profil.</span><span class="sxs-lookup"><span data-stu-id="73090-121">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="73090-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73090-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73090-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="73090-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



