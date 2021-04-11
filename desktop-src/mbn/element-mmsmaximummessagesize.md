---
description: MmsMaximumMessageSize
MS-HAID: WWAN\_profile\_v4.element\_MmsMaximumMessageSize
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsMaximumMessageSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5b020e7fd6ad4f39bd488c3af0ef14a3aab1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214704"
---
# <a name="span-idwwan_profile_v4element_mmsmaximummessagesizespanmmsmaximummessagesize"></a><span data-ttu-id="0b177-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>Mmsmaximummessagesize</span><span class="sxs-lookup"><span data-stu-id="0b177-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>MmsMaximumMessageSize</span></span>

<span data-ttu-id="0b177-104">Gibt die maximale Größe von MMS-Nachrichten in Kilobyte an.</span><span class="sxs-lookup"><span data-stu-id="0b177-104">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="0b177-105">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="0b177-105">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="0b177-106">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="0b177-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmsMaximumMessageSize>**

## <a name="syntax"></a><span data-ttu-id="0b177-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b177-107">Syntax</span></span>

``` syntax
<MmsMaximumMessageSize>

  nonNegativeInteger

</MmsMaximumMessageSize>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="0b177-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0b177-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="0b177-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="0b177-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="0b177-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="0b177-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="0b177-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b177-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="0b177-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="0b177-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="0b177-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b177-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b177-114">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="0b177-114">Parent Element</span></span></th>
<th><span data-ttu-id="0b177-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b177-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b177-116"><a href="element-mmsconfiguration.md">MMSConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="0b177-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="0b177-117">Konfigurationsinformationen für den Multimedia Messaging Service (MMS).</span><span class="sxs-lookup"><span data-stu-id="0b177-117">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="0b177-118">Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil über die folgenden Einstellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="0b177-118">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="0b177-119">Das <a href="element-name.md"><strong>Name</strong></a> -Element muss einen systemweiten eindeutigen Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b177-119">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="0b177-120">Der <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>profilekreationtype</strong></a> muss auf " <strong>userprovisioned</strong>" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0b177-120">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="0b177-121">Die <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>simiccid</strong></a> muss die ICCID der SIM enthalten, für die dieses Profil vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="0b177-121">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="0b177-122">Der <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> muss auf " <strong>Manual</strong>" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0b177-122">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="0b177-123">Die zugehörige Ziel <a href="element-purposegroupguid.md"><strong>Gruppen-ID</strong></a> muss die GUID für die MMS-Zweck Gruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b177-123">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="0b177-124"><a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>Isadditionalpdpcontextprofile</strong></a> muss auf " <strong>true</strong>" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0b177-124">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="0b177-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b177-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b177-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b177-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
