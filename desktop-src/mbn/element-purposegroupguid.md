---
description: "\"Zielstregroupguid\""
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroupGuid
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: "\"Zielstregroupguid\""
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d20d6c9d1687ea0e3fca344fd3b534ccc0b3ee57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393526"
---
# <a name="span-idwwan_profile_v4element_purposegroupguidspanpurposegroupguid"></a><span data-ttu-id="f72d4-103"><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>"Zielstregroupguid"</span><span class="sxs-lookup"><span data-stu-id="f72d4-103"><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>PurposeGroupGuid</span></span>

<span data-ttu-id="f72d4-104">Stellt ein Profil in einer Zweck Gruppe von Profilen dar.</span><span class="sxs-lookup"><span data-stu-id="f72d4-104">Represents one profile in a PurposeGroup of profiles.</span></span>

<span data-ttu-id="f72d4-105">Profile werden durch Ihren [**guidtype**](simpletype-guidtype.md) -Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="f72d4-105">Profiles are specified by their [**guidType**](simpletype-guidtype.md) value.</span></span>

<span data-ttu-id="f72d4-106">Vier GUID-Werte werden definiert, wie in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f72d4-106">Four GUID values are defined, as listed in the following table.</span></span>

| <span data-ttu-id="f72d4-107">Zweck Gruppe</span><span class="sxs-lookup"><span data-stu-id="f72d4-107">Purpose group</span></span> | <span data-ttu-id="f72d4-108">GUID</span><span class="sxs-lookup"><span data-stu-id="f72d4-108">GUID</span></span>                                 |
|---------------|--------------------------------------|
| <span data-ttu-id="f72d4-109">Internet</span><span class="sxs-lookup"><span data-stu-id="f72d4-109">Internet</span></span>      | <span data-ttu-id="f72d4-110">3e5545d2-1137-4dc8-a198-33F & 1c657515f</span><span class="sxs-lookup"><span data-stu-id="f72d4-110">3E5545D2-1137-4DC8-A198-33F1C657515F</span></span> |
| <span data-ttu-id="f72d4-111">mms</span><span class="sxs-lookup"><span data-stu-id="f72d4-111">MMS</span></span>           | <span data-ttu-id="f72d4-112">53e2c5d3-D13C-4068-AA38-9c48ff2e55a8</span><span class="sxs-lookup"><span data-stu-id="f72d4-112">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span></span> |
| <span data-ttu-id="f72d4-113">IMS</span><span class="sxs-lookup"><span data-stu-id="f72d4-113">IMS</span></span>           | <span data-ttu-id="f72d4-114">474d66ed-0e4b-476b-A455-19bb1239ed13</span><span class="sxs-lookup"><span data-stu-id="f72d4-114">474D66ED-0E4B-476B-A455-19BB1239ED13</span></span> |
| <span data-ttu-id="f72d4-115">SUPL</span><span class="sxs-lookup"><span data-stu-id="f72d4-115">SUPL</span></span>          | <span data-ttu-id="f72d4-116">6d42669l-52a9-408e-9493-1071dcc437bd</span><span class="sxs-lookup"><span data-stu-id="f72d4-116">6D42669F-52A9-408E-9493-1071DCC437BD</span></span> |

 

## <a name="element-hierarchy"></a><span data-ttu-id="f72d4-117">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="f72d4-117">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<PurposeGroups>](element-purposegroups.md)  
**<PurposeGroupGuid>**

## <a name="syntax"></a><span data-ttu-id="f72d4-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="f72d4-118">Syntax</span></span>

``` syntax
<PurposeGroupGuid>

  guidType

</PurposeGroupGuid>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="f72d4-119"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f72d4-119"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="f72d4-120"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="f72d4-120"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="f72d4-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="f72d4-121">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="f72d4-122"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f72d4-122"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="f72d4-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="f72d4-123">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="f72d4-124"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f72d4-124"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f72d4-125">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f72d4-125">Parent Element</span></span></th>
<th><span data-ttu-id="f72d4-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f72d4-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f72d4-127"><a href="element-purposegroups.md">Zielstregruppen</a></span><span class="sxs-lookup"><span data-stu-id="f72d4-127"><a href="element-purposegroups.md">PurposeGroups</a></span></span></td>
<td><p><span data-ttu-id="f72d4-128">Eine optionale Liste der Gruppen von Profilen, wobei jede Gruppe Profile enthält, die für einen allgemeinen Zweck verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f72d4-128">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span></p>
<p><span data-ttu-id="f72d4-129">Dieses Element ist neu für V4 des Schemas.</span><span class="sxs-lookup"><span data-stu-id="f72d4-129">This element is new for v4 of the schema.</span></span></p>
<p><span data-ttu-id="f72d4-130">Ein Profil kann in mehreren Gruppen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="f72d4-130">One profile can be listed in multiple groups.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="f72d4-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f72d4-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f72d4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f72d4-132">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



