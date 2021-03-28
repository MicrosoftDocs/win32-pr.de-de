---
description: Diese Klasse ist die Ereignistyp Klasse für UDP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: UdpIp_V1_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 58f7506aefa79c3bc9136d2e3e76d662f545a921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977105"
---
# <a name="udpip_v1_typegroup1-class"></a><span data-ttu-id="e0b9d-104">Udpip \_ v1 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="e0b9d-104">UdpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="e0b9d-105">Diese Klasse ist die Ereignistyp Klasse für UDP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="e0b9d-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b9d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0b9d-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="e0b9d-108">Member</span><span class="sxs-lookup"><span data-stu-id="e0b9d-108">Members</span></span>

<span data-ttu-id="e0b9d-109">Die **udpip \_ v1 \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e0b9d-109">The **UdpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="e0b9d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0b9d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0b9d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0b9d-111">Properties</span></span>

<span data-ttu-id="e0b9d-112">Die **udpip \_ v1 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-112">The **UdpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0b9d-113">daddr</span><span class="sxs-lookup"><span data-stu-id="e0b9d-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b9d-114">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e0b9d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-116">Qualifizierer: wmidataid (3), Erweiterung ("ipaddr")</span><span class="sxs-lookup"><span data-stu-id="e0b9d-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="e0b9d-117">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e0b9d-118">dport</span><span class="sxs-lookup"><span data-stu-id="e0b9d-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b9d-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e0b9d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-121">Qualifizierer: wmidataid (5), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="e0b9d-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="e0b9d-122">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="e0b9d-123">PID</span><span class="sxs-lookup"><span data-stu-id="e0b9d-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b9d-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e0b9d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-126">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="e0b9d-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="e0b9d-127">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="e0b9d-128">saddr</span><span class="sxs-lookup"><span data-stu-id="e0b9d-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b9d-129">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e0b9d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-131">Qualifizierer: wmidataid (4), Erweiterung ("ipaddr")</span><span class="sxs-lookup"><span data-stu-id="e0b9d-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="e0b9d-132">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e0b9d-133">size</span><span class="sxs-lookup"><span data-stu-id="e0b9d-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b9d-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e0b9d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-136">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="e0b9d-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="e0b9d-137">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="e0b9d-138">Reit</span><span class="sxs-lookup"><span data-stu-id="e0b9d-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b9d-139">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e0b9d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b9d-141">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="e0b9d-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="e0b9d-142">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0b9d-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e0b9d-143">Requirements</span></span>



| <span data-ttu-id="e0b9d-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0b9d-144">Requirement</span></span> | <span data-ttu-id="e0b9d-145">Wert</span><span class="sxs-lookup"><span data-stu-id="e0b9d-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e0b9d-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0b9d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b9d-147">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0b9d-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e0b9d-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0b9d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b9d-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0b9d-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0b9d-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0b9d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b9d-151">**Udpip \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-151">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> <dt>

[<span data-ttu-id="e0b9d-152">**Udpip**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-152">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




