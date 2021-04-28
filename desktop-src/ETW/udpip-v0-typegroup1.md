---
description: 'UdpIp_V0_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für UDP/IP-Ereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: UdpIp_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 78243a49e4504fd9e132407feebe98d9b48f7bdd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105498"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="191ba-104">UdpIp \_ V0 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="191ba-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="191ba-105">Diese Klasse ist die Ereignistypklasse für UDP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="191ba-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="191ba-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="191ba-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="191ba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="191ba-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a><span data-ttu-id="191ba-108">Member</span><span class="sxs-lookup"><span data-stu-id="191ba-108">Members</span></span>

<span data-ttu-id="191ba-109">Die **Klasse UdpIp \_ V0 \_ TypeGroup1** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="191ba-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="191ba-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="191ba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="191ba-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="191ba-111">Properties</span></span>

<span data-ttu-id="191ba-112">Die **Klasse UdpIp \_ V0 \_ TypeGroup1** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="191ba-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="191ba-113">context</span><span class="sxs-lookup"><span data-stu-id="191ba-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="191ba-114">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="191ba-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="191ba-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="191ba-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="191ba-116">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="191ba-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="191ba-117">Prozessbezeichner für das Adressobjekt, das die Anforderung erstellt oder empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="191ba-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="191ba-118">daddr</span><span class="sxs-lookup"><span data-stu-id="191ba-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="191ba-119">Datentyp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="191ba-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="191ba-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="191ba-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="191ba-121">Qualifizierer: WmiDataId(5), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="191ba-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="191ba-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="191ba-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="191ba-123">dport</span><span class="sxs-lookup"><span data-stu-id="191ba-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="191ba-124">Datentyp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="191ba-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="191ba-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="191ba-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="191ba-126">Qualifizierer: WmiDataId(6), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="191ba-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="191ba-127">Zielportnummer.</span><span class="sxs-lookup"><span data-stu-id="191ba-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="191ba-128">dsize</span><span class="sxs-lookup"><span data-stu-id="191ba-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="191ba-129">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="191ba-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="191ba-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="191ba-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="191ba-131">Qualifizierer: WmiDataId(7)</span><span class="sxs-lookup"><span data-stu-id="191ba-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="191ba-132">Größe des Zielpakets.</span><span class="sxs-lookup"><span data-stu-id="191ba-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="191ba-133">saddr</span><span class="sxs-lookup"><span data-stu-id="191ba-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="191ba-134">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="191ba-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="191ba-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="191ba-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="191ba-136">Qualifizierer: WmiDataId(2), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="191ba-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="191ba-137">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="191ba-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="191ba-138">Größe</span><span class="sxs-lookup"><span data-stu-id="191ba-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="191ba-139">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="191ba-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="191ba-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="191ba-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="191ba-141">Qualifizierer: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="191ba-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="191ba-142">Größe des Quellpakets.</span><span class="sxs-lookup"><span data-stu-id="191ba-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="191ba-143">Sport</span><span class="sxs-lookup"><span data-stu-id="191ba-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="191ba-144">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="191ba-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="191ba-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="191ba-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="191ba-146">Qualifizierer: WmiDataId(3), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="191ba-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="191ba-147">Quellportnummer.</span><span class="sxs-lookup"><span data-stu-id="191ba-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="191ba-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="191ba-148">Requirements</span></span>



| <span data-ttu-id="191ba-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="191ba-149">Requirement</span></span> | <span data-ttu-id="191ba-150">Wert</span><span class="sxs-lookup"><span data-stu-id="191ba-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="191ba-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="191ba-151">Minimum supported client</span></span><br/> | <span data-ttu-id="191ba-152">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="191ba-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="191ba-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="191ba-153">Minimum supported server</span></span><br/> | <span data-ttu-id="191ba-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="191ba-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="191ba-155">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="191ba-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="191ba-156">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="191ba-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




