---
description: Iwlananwendbarkeit
MS-HAID: WWAN\_profile\_v4.element\_IwlanApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iwlananwendbarkeit
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6b8b0376f2ee882a57e4c71e392fb7b02f6eeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347158"
---
# <a name="span-idwwan_profile_v4element_iwlanapplicabilityspaniwlanapplicability"></a><span data-ttu-id="0ead1-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>Iwlananwendbarkeit</span><span class="sxs-lookup"><span data-stu-id="0ead1-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>IwlanApplicability</span></span>

<span data-ttu-id="0ead1-104">Gibt an, dass dieses Profil nur aktiv ist, wenn es mit einem iWLAN-Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="0ead1-104">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="0ead1-105">Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0ead1-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="0ead1-106">Der Wert dieses Elements muss ein gültiger [**iwlanapplicabilitytype**](simpletype-iwlanapplicabilitytype.md) -Wert sein.</span><span class="sxs-lookup"><span data-stu-id="0ead1-106">The value of this element must be a valid [**iwlanApplicabilityType**](simpletype-iwlanapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="0ead1-107">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="0ead1-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<IwlanApplicability>**

## <a name="syntax"></a><span data-ttu-id="0ead1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ead1-108">Syntax</span></span>

``` syntax
<IwlanApplicability>

  "CellularOnly" | "CellularAndIwlan" | "IwlanOnly"

</IwlanApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="0ead1-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0ead1-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="0ead1-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="0ead1-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="0ead1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0ead1-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="0ead1-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0ead1-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="0ead1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0ead1-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="0ead1-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0ead1-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ead1-115">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="0ead1-115">Parent Element</span></span></th>
<th><span data-ttu-id="0ead1-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ead1-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ead1-117"><a href="element-profileconditionedon.md">Profileconditionedon</a></span><span class="sxs-lookup"><span data-stu-id="0ead1-117"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="0ead1-118">Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="0ead1-118">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="0ead1-119">Dieses Element ist neu für v4.</span><span class="sxs-lookup"><span data-stu-id="0ead1-119">This element is new for v4.</span></span> <span data-ttu-id="0ead1-120">Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unterschiedlichen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="0ead1-120">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="0ead1-121">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0ead1-121">This element is optional.</span></span> <span data-ttu-id="0ead1-122">Wenn Sie ihn nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="0ead1-122">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="0ead1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ead1-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ead1-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ead1-124">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



