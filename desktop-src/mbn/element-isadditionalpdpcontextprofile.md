---
description: Isadditionalpdpcontextprofile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Isadditionalpdpcontextprofile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343358"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span data-ttu-id="3e3d7-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>Isadditionalpdpcontextprofile</span><span class="sxs-lookup"><span data-stu-id="3e3d7-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span></span>

<span data-ttu-id="3e3d7-104">Das **isadditionalpdpcontextprofile** -Element enthält einen **booleschen** Wert, der **true** ist, wenn es sich um ein "zusätzliches PDP (Packet Data Protocol)"-Kontext Profil handelt, andernfalls " **false**".</span><span class="sxs-lookup"><span data-stu-id="3e3d7-104">The **IsAdditionalPdpContextProfile** element contains a **boolean** that is **true** if this is an "additional PDP (Packet Data Protocol) context" profile and **false**, otherwise.</span></span> <span data-ttu-id="3e3d7-105">Die Standardeinstellung lautet **false**.</span><span class="sxs-lookup"><span data-stu-id="3e3d7-105">Default is **false**.</span></span>

<span data-ttu-id="3e3d7-106">Ein "zusätzliches PDP-Kontext Profil" ist ein Profil, das nicht über den Standardport des physischen Adapters aktiviert wird. Wenn dieses Element auf "true" festgelegt wird, wird sichergestellt, dass dieses Profil nicht unpassend in der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3e3d7-106">An "additional PDP context" profile is a profile that does not get activated over the physical adapter default port, and setting this element to true ensures that this profile is not displayed inappropriately in the user interface.</span></span>

<span data-ttu-id="3e3d7-107">Beachten Sie Folgendes: Wenn dieses Element auf "true" festgelegt ist, muss Folgendes ebenfalls zutreffen:</span><span class="sxs-lookup"><span data-stu-id="3e3d7-107">Note that if this element is set to true, then the following must also be true.</span></span>

-   <span data-ttu-id="3e3d7-108">Das [**IsDefault**](./schema-isdefault-mbnprofile-element.md) -Element muss nicht angegeben werden, oder es muss auf **false** festgelegt werden, damit das Profil gültig ist.</span><span class="sxs-lookup"><span data-stu-id="3e3d7-108">The [**IsDefault**](./schema-isdefault-mbnprofile-element.md) element must be unspecified or set to **false** for the profile to be valid.</span></span>
-   <span data-ttu-id="3e3d7-109">Das [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) -Element muss nicht angegeben werden oder auf " **Manual** " festgelegt sein, damit das Profil gültig ist.</span><span class="sxs-lookup"><span data-stu-id="3e3d7-109">The [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) element must be unspecified or set to **manual** for the profile to be valid.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3e3d7-110">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="3e3d7-110">Element hierarchy</span></span>

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a><span data-ttu-id="3e3d7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e3d7-111">Syntax</span></span>

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3e3d7-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e3d7-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3e3d7-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="3e3d7-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3e3d7-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e3d7-114">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3e3d7-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e3d7-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="3e3d7-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e3d7-116">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3e3d7-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e3d7-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="3e3d7-118">Dieses äußerste (Dokument-) Element darf nicht in anderen Elementen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3e3d7-118">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e3d7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e3d7-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e3d7-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e3d7-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
