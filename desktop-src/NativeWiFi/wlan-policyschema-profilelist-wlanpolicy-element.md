---
description: 'profileList(WLANPolicy)-Element: Enthält eine Liste von Profilen, die auf Domänen- oder Computerebene angewendet werden sollen.'
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: profileList-Element (WLANPolicy)
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
ms.openlocfilehash: 4c7478f38ba7336738325bac6872866cd570288b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109198"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="d9aaa-103">profileList-Element (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="d9aaa-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="d9aaa-104">Das ProfileList-Element (WLANPolicy) enthält eine Liste von Profilen, die auf Domänen- oder Computerebene angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d9aaa-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="d9aaa-105">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="d9aaa-105">This element is optional.</span></span> <span data-ttu-id="d9aaa-106">Wenn dieses Element vorhanden ist, muss es mindestens ein Profil enthalten.</span><span class="sxs-lookup"><span data-stu-id="d9aaa-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="d9aaa-107">Profile sollten auf dem WLAN-Profilschema [ \_ mit](wlan-profileschema-schema.md)dem Stammelement [**WLANProfile basieren.**](wlan-profileschema-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="d9aaa-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

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

<span data-ttu-id="d9aaa-108">Das **profileList-Element** wird durch das [**WLANPolicy-Element**](wlan-policyschema-wlanpolicy-element.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d9aaa-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9aaa-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9aaa-109">Requirements</span></span>



| <span data-ttu-id="d9aaa-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9aaa-110">Requirement</span></span> | <span data-ttu-id="d9aaa-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d9aaa-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d9aaa-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9aaa-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d9aaa-113">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9aaa-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9aaa-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9aaa-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d9aaa-115">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9aaa-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9aaa-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d9aaa-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9aaa-117">**Definitionskontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="d9aaa-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d9aaa-118">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="d9aaa-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="d9aaa-119">**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**</span><span class="sxs-lookup"><span data-stu-id="d9aaa-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d9aaa-120">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="d9aaa-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




