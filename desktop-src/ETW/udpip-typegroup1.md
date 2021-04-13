---
description: Diese Klasse ist die Ereignistyp Klasse für UDP/IP-IPv4-Sende-und-Empfangs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: f04e0b4c-6a2b-4452-9bdf-38c08b487863
title: UdpIp_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup1
- UdpIp_TypeGroup1.PID
- UdpIp_TypeGroup1.size
- UdpIp_TypeGroup1.daddr
- UdpIp_TypeGroup1.saddr
- UdpIp_TypeGroup1.dport
- UdpIp_TypeGroup1.sport
- UdpIp_TypeGroup1.seqnum
- UdpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d977841cbfe9a88d14056d77a9b943f4d5d4a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978872"
---
# <a name="udpip_typegroup1-class"></a><span data-ttu-id="9b93c-104">Udpip \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="9b93c-104">UdpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="9b93c-105">Diese Klasse ist die Ereignistyp Klasse für UDP/IP-IPv4-Sende-und-Empfangs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="9b93c-105">This class is the event type class for UDP/IP IPv4 send and receive events.</span></span>

<span data-ttu-id="9b93c-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9b93c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b93c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b93c-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"SendIPV4", "RecvIPV4"}]
class UdpIp_TypeGroup1 : UdpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="9b93c-108">Member</span><span class="sxs-lookup"><span data-stu-id="9b93c-108">Members</span></span>

<span data-ttu-id="9b93c-109">Die **udpip- \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9b93c-109">The **UdpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="9b93c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b93c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b93c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b93c-111">Properties</span></span>

<span data-ttu-id="9b93c-112">Die **udpip- \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b93c-112">The **UdpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b93c-113">nicht konform</span><span class="sxs-lookup"><span data-stu-id="9b93c-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b93c-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b93c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b93c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-116">Qualifizierer: wmidataid (8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="9b93c-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9b93c-117">Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.</span><span class="sxs-lookup"><span data-stu-id="9b93c-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="9b93c-118">daddr</span><span class="sxs-lookup"><span data-stu-id="9b93c-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b93c-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="9b93c-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b93c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-121">Qualifizierer: wmidataid (3), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="9b93c-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="9b93c-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9b93c-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9b93c-123">dport</span><span class="sxs-lookup"><span data-stu-id="9b93c-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b93c-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="9b93c-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b93c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-126">Qualifizierer: wmidataid (5), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="9b93c-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="9b93c-127">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="9b93c-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="9b93c-128">PID</span><span class="sxs-lookup"><span data-stu-id="9b93c-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b93c-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b93c-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b93c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-131">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="9b93c-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="9b93c-132">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9b93c-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="9b93c-133">saddr</span><span class="sxs-lookup"><span data-stu-id="9b93c-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b93c-134">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="9b93c-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b93c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-136">Qualifizierer: wmidataid (4), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="9b93c-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="9b93c-137">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9b93c-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9b93c-138">SEQNUM</span><span class="sxs-lookup"><span data-stu-id="9b93c-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b93c-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b93c-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b93c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-141">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="9b93c-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="9b93c-142">Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="9b93c-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="9b93c-143">size</span><span class="sxs-lookup"><span data-stu-id="9b93c-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b93c-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b93c-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b93c-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-146">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="9b93c-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9b93c-147">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="9b93c-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="9b93c-148">Reit</span><span class="sxs-lookup"><span data-stu-id="9b93c-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b93c-149">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="9b93c-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b93c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b93c-151">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="9b93c-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="9b93c-152">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="9b93c-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b93c-153">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9b93c-153">Requirements</span></span>



| <span data-ttu-id="9b93c-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b93c-154">Requirement</span></span> | <span data-ttu-id="9b93c-155">Wert</span><span class="sxs-lookup"><span data-stu-id="9b93c-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9b93c-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b93c-156">Minimum supported client</span></span><br/> | <span data-ttu-id="9b93c-157">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b93c-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9b93c-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b93c-158">Minimum supported server</span></span><br/> | <span data-ttu-id="9b93c-159">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b93c-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b93c-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9b93c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b93c-161">**Udpip**</span><span class="sxs-lookup"><span data-stu-id="9b93c-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




