---
description: "\"Fidemdmconfigprofile\" \\/ ... \\/ Komprimierung (v4)"
MS-HAID: WWAN\_profile\_v4.element\_1\_Compression
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Komprimierung (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8dc3acd6-5997-47a5-bd30-899569b9aad9
api_name:
- Compression
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5796afb061bdc758bba020384501699fe3627e16
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388840"
---
# <a name="span-idwwan_profile_v4element_1_compressionspanmodemdmconfigprofilecompression-v4"></a><span data-ttu-id="c80b4-103"><span id="WWAN_profile_v4.element_1_Compression"></span>"Fidemdmconfigprofile" \/ ... \/ Komprimierung (v4)</span><span class="sxs-lookup"><span data-stu-id="c80b4-103"><span id="WWAN_profile_v4.element_1_Compression"></span>ModemDMConfigProfile\/...\/Compression (v4)</span></span>

<span data-ttu-id="c80b4-104">Gibt an, ob die Komprimierung im Daten Link für Header und Datenübertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c80b4-104">Specifies whether compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="c80b4-105">Weitere Informationen finden Sie in der Dokumentation für das v1- [**Komprimierungs**](./schema-compression-contexttype-element.md) Element.</span><span class="sxs-lookup"><span data-stu-id="c80b4-105">For more information, see the documentation for the v1 [**Compression**](./schema-compression-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="c80b4-106">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="c80b4-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

## <a name="syntax"></a><span data-ttu-id="c80b4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c80b4-107">Syntax</span></span>

``` syntax
<Compression>

  "DISABLE" | "ENABLE"

</Compression>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="c80b4-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c80b4-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="c80b4-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="c80b4-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="c80b4-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="c80b4-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="c80b4-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c80b4-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="c80b4-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="c80b4-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="c80b4-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c80b4-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c80b4-114">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="c80b4-114">Parent Element</span></span></th>
<th><span data-ttu-id="c80b4-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c80b4-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c80b4-116"><a href="element-1-context.md">Context</a></span><span class="sxs-lookup"><span data-stu-id="c80b4-116"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="c80b4-117">Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c80b4-117">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="c80b4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c80b4-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c80b4-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="c80b4-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
