---
description: Enthält eine Liste der Profile, die auf Domänen-oder Computer Ebene angewendet werden sollen.
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: ProfileList-Element (wlanpolicy)
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
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366135"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="5e8b9-103">ProfileList-Element (wlanpolicy)</span><span class="sxs-lookup"><span data-stu-id="5e8b9-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="5e8b9-104">Das ProfileList-Element (wlanpolicy) enthält eine Liste von Profilen, die auf Domänen-oder Computer Ebene angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e8b9-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="5e8b9-105">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="5e8b9-105">This element is optional.</span></span> <span data-ttu-id="5e8b9-106">Wenn dieses Element vorhanden ist, muss es mindestens ein Profil enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e8b9-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="5e8b9-107">Profile müssen auf dem WLAN- [ \_ Profil Schema](wlan-profileschema-schema.md)mit einem Stamm Element von [**wlanprofile**](wlan-profileschema-wlanprofile-element.md)basieren.</span><span class="sxs-lookup"><span data-stu-id="5e8b9-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

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

<span data-ttu-id="5e8b9-108">Das **ProfileList** -Element wird durch das [**wlanpolicy**](wlan-policyschema-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="5e8b9-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e8b9-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e8b9-109">Requirements</span></span>



| <span data-ttu-id="5e8b9-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e8b9-110">Requirement</span></span> | <span data-ttu-id="5e8b9-111">Wert</span><span class="sxs-lookup"><span data-stu-id="5e8b9-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e8b9-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e8b9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8b9-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e8b9-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e8b9-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e8b9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8b9-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e8b9-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e8b9-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e8b9-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e8b9-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="5e8b9-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5e8b9-118">**Wlanpolicy**</span><span class="sxs-lookup"><span data-stu-id="5e8b9-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="5e8b9-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="5e8b9-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5e8b9-120">**Wlanpolicy**</span><span class="sxs-lookup"><span data-stu-id="5e8b9-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




