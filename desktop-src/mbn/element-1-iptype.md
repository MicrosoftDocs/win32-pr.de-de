---
description: "\"Fidemdmconfigprofile\" \\/ ... \\/ Iptype (v4)"
MS-HAID: WWAN\_profile\_v4.element\_1\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iptype (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec57fbe0bbcb4c633ddb8485f048ce4230e0ca5
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388805"
---
# <a name="span-idwwan_profile_v4element_1_iptypespanmodemdmconfigprofileiptype-v4"></a><span data-ttu-id="546b9-103"><span id="WWAN_profile_v4.element_1_IPType"></span>"Fidemdmconfigprofile" \/ ... \/ Iptype (v4)</span><span class="sxs-lookup"><span data-stu-id="546b9-103"><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile\/...\/IPType (v4)</span></span>

<span data-ttu-id="546b9-104">Gibt den IP-Typ an, der für diese Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="546b9-104">Specifies the IP type to be used on this data connection.</span></span>

<span data-ttu-id="546b9-105">Dieses Element ist neu in v4 des Schemas.</span><span class="sxs-lookup"><span data-stu-id="546b9-105">This element is new in v4 of the schema.</span></span> <span data-ttu-id="546b9-106">Das-Element kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="546b9-106">The element can have one of the following values.</span></span>

| <span data-ttu-id="546b9-107">Wert</span><span class="sxs-lookup"><span data-stu-id="546b9-107">Value</span></span>   | <span data-ttu-id="546b9-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="546b9-108">Meaning</span></span>                                       |
|---------|-----------------------------------------------|
| <span data-ttu-id="546b9-109">Standard</span><span class="sxs-lookup"><span data-stu-id="546b9-109">Default</span></span> | <span data-ttu-id="546b9-110">Der IP-Typ muss von niedrigeren Ebenen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="546b9-110">IP type is to be picked by lower layer(s)</span></span>     |
| <span data-ttu-id="546b9-111">IPv4</span><span class="sxs-lookup"><span data-stu-id="546b9-111">IPv4</span></span>    | <span data-ttu-id="546b9-112">IPv4 verwenden</span><span class="sxs-lookup"><span data-stu-id="546b9-112">Use IPv4</span></span>                                      |
| <span data-ttu-id="546b9-113">IPv6</span><span class="sxs-lookup"><span data-stu-id="546b9-113">IPv6</span></span>    | <span data-ttu-id="546b9-114">IPv6 verwenden</span><span class="sxs-lookup"><span data-stu-id="546b9-114">Use IPv6</span></span>                                      |
| <span data-ttu-id="546b9-115">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="546b9-115">IPv4v6</span></span>  | <span data-ttu-id="546b9-116">Verwenden Sie IPv4 und/oder IPv6 als verfügbar.</span><span class="sxs-lookup"><span data-stu-id="546b9-116">Use IPv4 and/or IPv6, as available.</span></span>           |
| <span data-ttu-id="546b9-117">Xlat</span><span class="sxs-lookup"><span data-stu-id="546b9-117">XLAT</span></span>    | <span data-ttu-id="546b9-118">Verwenden von 464xlat zum Tunneln von IPv4 über IPv6-Netzwerke</span><span class="sxs-lookup"><span data-stu-id="546b9-118">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span> |

 

## <a name="element-hierarchy"></a><span data-ttu-id="546b9-119">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="546b9-119">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a><span data-ttu-id="546b9-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="546b9-120">Syntax</span></span>

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="546b9-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="546b9-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="546b9-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="546b9-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="546b9-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="546b9-123">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="546b9-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="546b9-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="546b9-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="546b9-125">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="546b9-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="546b9-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="546b9-127">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="546b9-127">Parent Element</span></span></th>
<th><span data-ttu-id="546b9-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="546b9-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="546b9-129"><a href="element-1-context.md">Context</a></span><span class="sxs-lookup"><span data-stu-id="546b9-129"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="546b9-130">Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="546b9-130">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="546b9-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="546b9-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="546b9-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="546b9-132">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



