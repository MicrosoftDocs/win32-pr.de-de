---
description: MMSConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MMSConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb98506476558ed0e39df11bab4b9446de4fd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214561"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span data-ttu-id="3038d-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MMSConfiguration</span><span class="sxs-lookup"><span data-stu-id="3038d-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span></span>

<span data-ttu-id="3038d-104">Konfigurationsinformationen für den Multimedia Messaging Service (MMS).</span><span class="sxs-lookup"><span data-stu-id="3038d-104">Configuration information for Multimedia Messaging Service (MMS).</span></span>

<span data-ttu-id="3038d-105">Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil über die folgenden Einstellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="3038d-105">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span>

-   <span data-ttu-id="3038d-106">Das [**Name**](element-name.md) -Element muss einen systemweiten eindeutigen Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3038d-106">Its [**Name**](element-name.md) element must contain a system-wide unique name.</span></span>
-   <span data-ttu-id="3038d-107">Der [**profilekreationtype**](./schema-profilecreationtype-mbnprofile-element.md) muss auf " **userprovisioned**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3038d-107">Its [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) must be set to **UserProvisioned**.</span></span>
-   <span data-ttu-id="3038d-108">Die [**simiccid**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) muss die ICCID der SIM enthalten, für die dieses Profil vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="3038d-108">Its [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) must contain the ICCID of the SIM that this profile is intended for.</span></span>
-   <span data-ttu-id="3038d-109">Der [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) muss auf " **Manual**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3038d-109">Its [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) must be set to **Manual**.</span></span>
-   <span data-ttu-id="3038d-110">Die zugehörige Ziel [**Gruppen-ID**](element-purposegroupguid.md) muss die GUID für die MMS-Zweck Gruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="3038d-110">Its [**PurposeGroupGuid**](element-purposegroupguid.md) must contain the GUID for MMS purpose group.</span></span>
-   <span data-ttu-id="3038d-111">[**Isadditionalpdpcontextprofile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) muss auf " **true**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3038d-111">Its [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) must be set to **true**.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3038d-112">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="3038d-112">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a><span data-ttu-id="3038d-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="3038d-113">Syntax</span></span>

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a><span data-ttu-id="3038d-114">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="3038d-114">Key</span></span>

<span data-ttu-id="3038d-115">`?`   optional (0 (null) oder eins)</span><span class="sxs-lookup"><span data-stu-id="3038d-115">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3038d-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3038d-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3038d-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="3038d-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3038d-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="3038d-118">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3038d-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3038d-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3038d-120">Untergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="3038d-120">Child Element</span></span></th>
<th><span data-ttu-id="3038d-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3038d-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3038d-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span><span class="sxs-lookup"><span data-stu-id="3038d-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span></span></td>
<td><p><span data-ttu-id="3038d-123">Gibt die maximale Größe von MMS-Nachrichten in Kilobyte an.</span><span class="sxs-lookup"><span data-stu-id="3038d-123">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="3038d-124">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="3038d-124">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3038d-125"><a href="element-mmscport.md">MmscPort</a></span><span class="sxs-lookup"><span data-stu-id="3038d-125"><a href="element-mmscport.md">MmscPort</a></span></span></td>
<td><p><span data-ttu-id="3038d-126">Gibt die Portnummer des MMSC-Servers für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="3038d-126">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="3038d-127">Geben Sie 0 an, um anzugeben, dass kein bestimmter Port angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3038d-127">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="3038d-128">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="3038d-128">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3038d-129"><a href="element-mmscurl.md">MmscUrl</a></span><span class="sxs-lookup"><span data-stu-id="3038d-129"><a href="element-mmscurl.md">MmscUrl</a></span></span></td>
<td><p><span data-ttu-id="3038d-130">Gibt die URL des MMSC-Servers für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="3038d-130">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="3038d-131">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="3038d-131">Optional.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3038d-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3038d-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3038d-133">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="3038d-133">Parent Element</span></span></th>
<th><span data-ttu-id="3038d-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3038d-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3038d-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="3038d-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="3038d-136">Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="3038d-136">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="3038d-137">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="3038d-137">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="3038d-138">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3038d-138">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="3038d-139">Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="3038d-139">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="3038d-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3038d-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3038d-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="3038d-141">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
