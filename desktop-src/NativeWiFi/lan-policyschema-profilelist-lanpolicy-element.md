---
description: Enthält eine Liste der Profile, die auf Domänen-oder Computer Ebene angewendet werden sollen.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: ProfileList-Element (lanpolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: b85c284262c070f7a9349933f99ad858cf047913
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373158"
---
# <a name="profilelist-lanpolicy-element"></a><span data-ttu-id="800f2-103">ProfileList-Element (lanpolicy)</span><span class="sxs-lookup"><span data-stu-id="800f2-103">profileList (LANPolicy) Element</span></span>

<span data-ttu-id="800f2-104">Das ProfileList-Element (lanpolicy) enthält eine Liste der Profile, die auf der Domänen-oder Computer Ebene angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="800f2-104">The profileList (LANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="800f2-105">Profile müssen auf dem LAN- [ \_ Profil Schema](lan-profileschema-schema.md)mit einem Stamm Element von " [**lanprofile**](lan-profileschema-lanprofile-element.md)" basieren.</span><span class="sxs-lookup"><span data-stu-id="800f2-105">Profiles must be based on the [LAN\_profile schema](lan-profileschema-schema.md), with a root element of [**LANProfile**](lan-profileschema-lanprofile-element.md).</span></span> <span data-ttu-id="800f2-106">Profile, die auf einem beliebigen anderen Schema basieren, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="800f2-106">Profiles based on any other schema will be ignored.</span></span>

<span data-ttu-id="800f2-107">Wenn [**enableautoconfig**](lan-policyschema-enableautoconfig-globalflags-element.md) auf false festgelegt ist, darf dieses Element nicht in einem LAN-Richtlinien Profil vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="800f2-107">When [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) is set to FALSE, this element must not be present in a LAN policy profile.</span></span> <span data-ttu-id="800f2-108">Wenn **enableautoconfig** auf true festgelegt ist, ist dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="800f2-108">When **enableAutoConfig** is set to TRUE, then this element is required.</span></span>

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="800f2-109">Das **ProfileList** -Element wird durch das [**lanpolicy**](lan-policyschema-lanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="800f2-109">The **profileList** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="800f2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="800f2-110">Remarks</span></span>

<span data-ttu-id="800f2-111">Dieses Element sollte genau ein Netzwerk Profil enthalten.</span><span class="sxs-lookup"><span data-stu-id="800f2-111">This element should contain exactly one network profile.</span></span> <span data-ttu-id="800f2-112">Wenn mehr als ein Profil in der Richtlinie angegeben ist, wird nur das erste Netzwerk angewendet.</span><span class="sxs-lookup"><span data-stu-id="800f2-112">If more than one profile is specified in the policy, only the first network will be applied.</span></span>

## <a name="requirements"></a><span data-ttu-id="800f2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="800f2-113">Requirements</span></span>



| <span data-ttu-id="800f2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="800f2-114">Requirement</span></span> | <span data-ttu-id="800f2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="800f2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="800f2-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="800f2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="800f2-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="800f2-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="800f2-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="800f2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="800f2-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="800f2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="800f2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="800f2-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="800f2-121">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="800f2-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="800f2-122">**Lanpolicy**</span><span class="sxs-lookup"><span data-stu-id="800f2-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="800f2-123">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="800f2-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="800f2-124">**Lanpolicy**</span><span class="sxs-lookup"><span data-stu-id="800f2-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




