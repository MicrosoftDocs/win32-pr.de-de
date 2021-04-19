---
description: Zielstregruppen
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Zielstregruppen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370cf6b0dc13848ca21a2a06e0b9806d753878c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350425"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span data-ttu-id="36bce-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>Zielstregruppen</span><span class="sxs-lookup"><span data-stu-id="36bce-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span></span>

<span data-ttu-id="36bce-104">Eine optionale Liste der Gruppen von Profilen, wobei jede Gruppe Profile enthält, die für einen allgemeinen Zweck verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36bce-104">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span>

<span data-ttu-id="36bce-105">Dieses Element ist neu für V4 des Schemas.</span><span class="sxs-lookup"><span data-stu-id="36bce-105">This element is new for v4 of the schema.</span></span>

<span data-ttu-id="36bce-106">Ein Profil kann in mehreren Gruppen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="36bce-106">One profile can be listed in multiple groups.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="36bce-107">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="36bce-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a><span data-ttu-id="36bce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="36bce-108">Syntax</span></span>

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a><span data-ttu-id="36bce-109">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="36bce-109">Key</span></span>

<span data-ttu-id="36bce-110">`{}`   bestimmter Bereich von vorkommen</span><span class="sxs-lookup"><span data-stu-id="36bce-110">`{}`   specific range of occurrences</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="36bce-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="36bce-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="36bce-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="36bce-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="36bce-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="36bce-113">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="36bce-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36bce-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36bce-115">Untergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="36bce-115">Child Element</span></span></th>
<th><span data-ttu-id="36bce-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36bce-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bce-117"><a href="element-purposegroupguid.md">"Zielstregroupguid"</a></span><span class="sxs-lookup"><span data-stu-id="36bce-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span></span></td>
<td><p><span data-ttu-id="36bce-118">Stellt ein Profil in einer Zweck Gruppe von Profilen dar.</span><span class="sxs-lookup"><span data-stu-id="36bce-118">Represents one profile in a PurposeGroup of profiles.</span></span></p>
<p><span data-ttu-id="36bce-119">Profile werden durch Ihren <a href="simpletype-guidtype.md"><strong>guidtype</strong></a> -Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="36bce-119">Profiles are specified by their <a href="simpletype-guidtype.md"><strong>guidType</strong></a> value.</span></span></p>
<p><span data-ttu-id="36bce-120">Vier GUID-Werte werden definiert, wie in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="36bce-120">Four GUID values are defined, as listed in the following table.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="36bce-121">Zweck Gruppe</span><span class="sxs-lookup"><span data-stu-id="36bce-121">Purpose group</span></span></th>
<th><span data-ttu-id="36bce-122">GUID</span><span class="sxs-lookup"><span data-stu-id="36bce-122">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bce-123">Internet</span><span class="sxs-lookup"><span data-stu-id="36bce-123">Internet</span></span></td>
<td><span data-ttu-id="36bce-124">3e5545d2-1137-4dc8-a198-33F & 1c657515f</span><span class="sxs-lookup"><span data-stu-id="36bce-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36bce-125">mms</span><span class="sxs-lookup"><span data-stu-id="36bce-125">MMS</span></span></td>
<td><span data-ttu-id="36bce-126">53e2c5d3-D13C-4068-AA38-9c48ff2e55a8</span><span class="sxs-lookup"><span data-stu-id="36bce-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36bce-127">IMS</span><span class="sxs-lookup"><span data-stu-id="36bce-127">IMS</span></span></td>
<td><span data-ttu-id="36bce-128">474d66ed-0e4b-476b-A455-19bb1239ed13</span><span class="sxs-lookup"><span data-stu-id="36bce-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36bce-129">SUPL</span><span class="sxs-lookup"><span data-stu-id="36bce-129">SUPL</span></span></td>
<td><span data-ttu-id="36bce-130">6d42669l-52a9-408e-9493-1071dcc437bd</span><span class="sxs-lookup"><span data-stu-id="36bce-130">6D42669F-52A9-408E-9493-1071DCC437BD</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="36bce-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36bce-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36bce-132">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="36bce-132">Parent Element</span></span></th>
<th><span data-ttu-id="36bce-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36bce-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bce-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="36bce-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="36bce-135">Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="36bce-135">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="36bce-136">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="36bce-136">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="36bce-137">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="36bce-137">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="36bce-138">Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="36bce-138">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="36bce-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36bce-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36bce-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="36bce-140">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



