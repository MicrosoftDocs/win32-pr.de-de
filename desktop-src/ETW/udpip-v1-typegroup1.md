---
description: 'UdpIp_V1_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für UDP/IP-Ereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
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
ms.openlocfilehash: d7dadaac3d418d2351f9e27c694309deb373615e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105408"
---
# <a name="udpip_v1_typegroup1-class"></a><span data-ttu-id="4979e-104">UdpIp \_ V1 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="4979e-104">UdpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="4979e-105">Diese Klasse ist die Ereignistypklasse für UDP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="4979e-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="4979e-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="4979e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4979e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4979e-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="4979e-108">Member</span><span class="sxs-lookup"><span data-stu-id="4979e-108">Members</span></span>

<span data-ttu-id="4979e-109">Die **Klasse UdpIp \_ V1 \_ TypeGroup1** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="4979e-109">The **UdpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="4979e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4979e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4979e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4979e-111">Properties</span></span>

<span data-ttu-id="4979e-112">Die **Klasse UdpIp \_ V1 \_ TypeGroup1** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4979e-112">The **UdpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4979e-113">daddr</span><span class="sxs-lookup"><span data-stu-id="4979e-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4979e-114">Datentyp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="4979e-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4979e-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4979e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4979e-116">Qualifizierer: WmiDataId(3), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="4979e-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="4979e-117">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="4979e-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4979e-118">dport</span><span class="sxs-lookup"><span data-stu-id="4979e-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4979e-119">Datentyp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="4979e-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4979e-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4979e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4979e-121">Qualifizierer: WmiDataId(5), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="4979e-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="4979e-122">Zielportnummer.</span><span class="sxs-lookup"><span data-stu-id="4979e-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="4979e-123">PID</span><span class="sxs-lookup"><span data-stu-id="4979e-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4979e-124">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4979e-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4979e-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4979e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4979e-126">Qualifizierer: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="4979e-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="4979e-127">Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4979e-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="4979e-128">saddr</span><span class="sxs-lookup"><span data-stu-id="4979e-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4979e-129">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="4979e-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4979e-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4979e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4979e-131">Qualifizierer: WmiDataId(4), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="4979e-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="4979e-132">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="4979e-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4979e-133">Größe</span><span class="sxs-lookup"><span data-stu-id="4979e-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4979e-134">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4979e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4979e-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4979e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4979e-136">Qualifizierer: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="4979e-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4979e-137">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="4979e-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="4979e-138">Sport</span><span class="sxs-lookup"><span data-stu-id="4979e-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4979e-139">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="4979e-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4979e-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4979e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4979e-141">Qualifizierer: WmiDataId(6), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="4979e-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="4979e-142">Quellportnummer.</span><span class="sxs-lookup"><span data-stu-id="4979e-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4979e-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4979e-143">Requirements</span></span>



| <span data-ttu-id="4979e-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4979e-144">Requirement</span></span> | <span data-ttu-id="4979e-145">Wert</span><span class="sxs-lookup"><span data-stu-id="4979e-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4979e-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4979e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4979e-147">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4979e-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4979e-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4979e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4979e-149">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4979e-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4979e-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4979e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4979e-151">**UdpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="4979e-151">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> <dt>

[<span data-ttu-id="4979e-152">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="4979e-152">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




