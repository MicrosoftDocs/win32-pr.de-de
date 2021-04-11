---
description: Enthält Informationen über den Ersteller des Profils.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Profilekreationtype (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129569"
---
# <a name="profilecreationtype-mbnprofile-element"></a><span data-ttu-id="c52e1-103">Profilekreationtype (mbnprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="c52e1-103">ProfileCreationType (MBNProfile) Element</span></span>

<span data-ttu-id="c52e1-104">Das **profilekreationtype (mbnprofile)** -Element enthält Informationen zum Ersteller des Profils.</span><span class="sxs-lookup"><span data-stu-id="c52e1-104">The **ProfileCreationType (MBNProfile)** element contains information about the creator of the profile.</span></span>

<span data-ttu-id="c52e1-105">Dieses Element kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c52e1-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="c52e1-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c52e1-106">Value</span></span>                 | <span data-ttu-id="c52e1-107">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c52e1-107">Meaning</span></span>                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c52e1-108">"Userprovisioned"</span><span class="sxs-lookup"><span data-stu-id="c52e1-108">"UserProvisioned"</span></span>     | <span data-ttu-id="c52e1-109">Dieses Profil wird von Informationen erstellt, die vom Benutzer des Geräts bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c52e1-109">This profile is created by information provided by the user of device.</span></span>                                                     |
| <span data-ttu-id="c52e1-110">"Adminprovisioned"</span><span class="sxs-lookup"><span data-stu-id="c52e1-110">"AdminProvisioned"</span></span>    | <span data-ttu-id="c52e1-111">Dieses Profil wird von IT-Administratoren erstellt und an Benutzer verteilt.</span><span class="sxs-lookup"><span data-stu-id="c52e1-111">This profile is created by IT administrators and distributed to users.</span></span>                                                     |
| <span data-ttu-id="c52e1-112">"Operatorprovisioned"</span><span class="sxs-lookup"><span data-stu-id="c52e1-112">"OperatorProvisioned"</span></span> | <span data-ttu-id="c52e1-113">Dieses Profil wird von einem Netzwerk Operator erstellt und an Benutzer verteilt.</span><span class="sxs-lookup"><span data-stu-id="c52e1-113">This profile is created by a network operator and distributed to users.</span></span>                                                    |
| <span data-ttu-id="c52e1-114">"Deviceprovisioned"</span><span class="sxs-lookup"><span data-stu-id="c52e1-114">"DeviceProvisioned"</span></span>   | <span data-ttu-id="c52e1-115">Dieses Profil wird vom mobilen Breitbanddienst erstellt, indem die Informationen verwendet werden, die im bereitgestellten Gerätekontext gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="c52e1-115">This profile is created by the Mobile Broadband service by using the information stored in the device provisioned context.</span></span> |



 

<span data-ttu-id="c52e1-116">Dies ist ein optionales Element.</span><span class="sxs-lookup"><span data-stu-id="c52e1-116">This is an optional element.</span></span>

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="c52e1-117">Das **profilekreationtype** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="c52e1-117">The **ProfileCreationType** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c52e1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c52e1-118">Requirements</span></span>



| <span data-ttu-id="c52e1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c52e1-119">Requirement</span></span> | <span data-ttu-id="c52e1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c52e1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c52e1-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c52e1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c52e1-122">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c52e1-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c52e1-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c52e1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c52e1-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c52e1-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c52e1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c52e1-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c52e1-126">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="c52e1-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c52e1-127">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="c52e1-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="c52e1-128">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="c52e1-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c52e1-129">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="c52e1-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




