---
description: Gibt die Zeitdauer in Sekunden an, in der ein Client die Authentifizierung nach einem fehlgeschlagenen Authentifizierungs Versuch nicht erneut versucht.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: heldperiod-Element (Onex)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367920"
---
# <a name="heldperiod-onex-element"></a><span data-ttu-id="7bafb-103">heldperiod-Element (Onex)</span><span class="sxs-lookup"><span data-stu-id="7bafb-103">heldPeriod (OneX) Element</span></span>

<span data-ttu-id="7bafb-104">Das heldperiod (Onex)-Element gibt die Zeitdauer in Sekunden an, in der ein Client die Authentifizierung nach einem fehlgeschlagenen Authentifizierungs Versuch nicht erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="7bafb-104">The heldPeriod (OneX) element specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span>

<span data-ttu-id="7bafb-105">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="7bafb-105">This element is optional.</span></span> <span data-ttu-id="7bafb-106">Wenn heldperiod nicht in einem Profil angegeben ist, wird ein Wert von 1 Sekunde verwendet.</span><span class="sxs-lookup"><span data-stu-id="7bafb-106">When heldPeriod is not specified in a profile, a value of 1 second is used.</span></span>

<span data-ttu-id="7bafb-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7bafb-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="7bafb-108">Das **heldperiod** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="7bafb-108">The **heldPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bafb-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bafb-109">Requirements</span></span>



| <span data-ttu-id="7bafb-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bafb-110">Requirement</span></span> | <span data-ttu-id="7bafb-111">Wert</span><span class="sxs-lookup"><span data-stu-id="7bafb-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7bafb-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bafb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7bafb-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bafb-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7bafb-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bafb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7bafb-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bafb-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7bafb-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bafb-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="7bafb-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="7bafb-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7bafb-118">**Onex**</span><span class="sxs-lookup"><span data-stu-id="7bafb-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="7bafb-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="7bafb-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7bafb-120">**Onex**</span><span class="sxs-lookup"><span data-stu-id="7bafb-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




