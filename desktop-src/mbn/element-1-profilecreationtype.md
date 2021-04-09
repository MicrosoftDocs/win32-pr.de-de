---
description: Profilekreationtype (in "mudedmconfigprofile")
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Profilekreationtype (in "mudedmconfigprofile")
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b755840d0308ec2d7a7bba5896b0cf67b7b61198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862515"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span data-ttu-id="1a62b-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>Profilekreationtype (in "mudedmconfigprofile")</span><span class="sxs-lookup"><span data-stu-id="1a62b-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (in ModemDMConfigProfile)</span></span>

<span data-ttu-id="1a62b-104">Gibt an, wie dieses Modem-DM-Profil erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1a62b-104">Specifies how this modem DM profile was created.</span></span>

<span data-ttu-id="1a62b-105">Dieser Wert wird verwendet, um zu entscheiden, ob ein Benutzer das Profil löschen kann.</span><span class="sxs-lookup"><span data-stu-id="1a62b-105">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="1a62b-106">Benutzer können nur **Benutzer bereitgestellte** Profile löschen.</span><span class="sxs-lookup"><span data-stu-id="1a62b-106">Users can only delete **UserProvisioned** profiles.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1a62b-107">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="1a62b-107">Element hierarchy</span></span>

[<ModemDMConfigProfile>](element-modemdmconfigprofile.md)  
**<ProfileCreationType>**

## <a name="syntax"></a><span data-ttu-id="1a62b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a62b-108">Syntax</span></span>

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1a62b-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1a62b-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1a62b-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="1a62b-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1a62b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1a62b-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1a62b-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a62b-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="1a62b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1a62b-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1a62b-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a62b-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a62b-115">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1a62b-115">Parent Element</span></span></th>
<th><span data-ttu-id="1a62b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a62b-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a62b-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="1a62b-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="1a62b-118">Modem-DM-Konfigurations Profil.</span><span class="sxs-lookup"><span data-stu-id="1a62b-118">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a><span data-ttu-id="1a62b-119">Zugehörige Elemente</span><span class="sxs-lookup"><span data-stu-id="1a62b-119">Related elements</span></span>

<span data-ttu-id="1a62b-120">Die folgenden Elemente haben denselben Namen wie dieses Element, aber ihr Inhalt oder ihre Attribute sind anders.</span><span class="sxs-lookup"><span data-stu-id="1a62b-120">The following elements have the same name as this one, but different content or attributes:</span></span>

-   <span data-ttu-id="1a62b-121">**[Profilekreationtype (in mbnprofileext)](element-profilecreationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="1a62b-121">**[ProfileCreationType (in MBNProfileExt)](element-profilecreationtype.md)**</span></span>

## <a name="requirements"></a><span data-ttu-id="1a62b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a62b-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a62b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a62b-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



