---
description: 'profileList (LANPolicy)-Element: Enthält eine Liste von Profilen, die auf Domänen- oder Computerebene angewendet werden sollen.'
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: profileList -Element (LANPolicy)
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
ms.openlocfilehash: 5d18ebc99f48bf72599afe750863d684b8158608
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090778"
---
# <a name="profilelist-lanpolicy-element"></a><span data-ttu-id="faef8-103">profileList -Element (LANPolicy)</span><span class="sxs-lookup"><span data-stu-id="faef8-103">profileList (LANPolicy) Element</span></span>

<span data-ttu-id="faef8-104">Das Element profileList (LANPolicy) enthält eine Liste von Profilen, die auf Domänen- oder Computerebene angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="faef8-104">The profileList (LANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="faef8-105">Profile müssen auf dem [ \_ LAN-Profilschema](lan-profileschema-schema.md)mit dem Stammelement [**LANProfile**](lan-profileschema-lanprofile-element.md)basieren.</span><span class="sxs-lookup"><span data-stu-id="faef8-105">Profiles must be based on the [LAN\_profile schema](lan-profileschema-schema.md), with a root element of [**LANProfile**](lan-profileschema-lanprofile-element.md).</span></span> <span data-ttu-id="faef8-106">Profile, die auf einem anderen Schema basieren, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="faef8-106">Profiles based on any other schema will be ignored.</span></span>

<span data-ttu-id="faef8-107">Wenn [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) auf FALSE festgelegt ist, darf dieses Element nicht in einem LAN-Richtlinienprofil vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="faef8-107">When [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) is set to FALSE, this element must not be present in a LAN policy profile.</span></span> <span data-ttu-id="faef8-108">Wenn **enableAutoConfig** auf TRUE festgelegt ist, ist dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="faef8-108">When **enableAutoConfig** is set to TRUE, then this element is required.</span></span>

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

<span data-ttu-id="faef8-109">Das **profileList-Element** wird durch das [**LANPolicy-Element**](lan-policyschema-lanpolicy-element.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="faef8-109">The **profileList** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="faef8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faef8-110">Remarks</span></span>

<span data-ttu-id="faef8-111">Dieses Element sollte genau ein Netzwerkprofil enthalten.</span><span class="sxs-lookup"><span data-stu-id="faef8-111">This element should contain exactly one network profile.</span></span> <span data-ttu-id="faef8-112">Wenn in der Richtlinie mehr als ein Profil angegeben ist, wird nur das erste Netzwerk angewendet.</span><span class="sxs-lookup"><span data-stu-id="faef8-112">If more than one profile is specified in the policy, only the first network will be applied.</span></span>

## <a name="requirements"></a><span data-ttu-id="faef8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faef8-113">Requirements</span></span>



| <span data-ttu-id="faef8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faef8-114">Requirement</span></span> | <span data-ttu-id="faef8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="faef8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="faef8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="faef8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="faef8-117">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faef8-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="faef8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="faef8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="faef8-119">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faef8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="faef8-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="faef8-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="faef8-121">**Definitionskontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="faef8-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="faef8-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="faef8-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="faef8-123">**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**</span><span class="sxs-lookup"><span data-stu-id="faef8-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="faef8-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="faef8-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




