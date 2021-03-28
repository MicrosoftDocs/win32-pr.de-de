---
description: Diese Klasse ist die Ereignistyp Klasse für UDP/IP-IPv6-Sende-und-Empfangs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 059041f6-bf34-4bf8-8e1a-2dfbc6c30edc
title: UdpIp_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup2
- UdpIp_TypeGroup2.PID
- UdpIp_TypeGroup2.size
- UdpIp_TypeGroup2.daddr
- UdpIp_TypeGroup2.saddr
- UdpIp_TypeGroup2.dport
- UdpIp_TypeGroup2.sport
- UdpIp_TypeGroup2.seqnum
- UdpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88d9cb4935d005f3c25f1fb6c3c421328fb285bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978865"
---
# <a name="udpip_typegroup2-class"></a><span data-ttu-id="c5705-104">Udpip \_ TypeGroup2-Klasse</span><span class="sxs-lookup"><span data-stu-id="c5705-104">UdpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="c5705-105">Diese Klasse ist die Ereignistyp Klasse für UDP/IP-IPv6-Sende-und-Empfangs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="c5705-105">This class is the event type class for UDP/IP IPv6 send and receive events.</span></span>

<span data-ttu-id="c5705-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c5705-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5705-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5705-107">Syntax</span></span>

``` syntax
[EventType{26, 27}, EventTypeName{"SendIPV6", "RecvIPV6"}]
class UdpIp_TypeGroup2 : UdpIp
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

## <a name="members"></a><span data-ttu-id="c5705-108">Member</span><span class="sxs-lookup"><span data-stu-id="c5705-108">Members</span></span>

<span data-ttu-id="c5705-109">Die **udpip- \_ TypeGroup2** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c5705-109">The **UdpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="c5705-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5705-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5705-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5705-111">Properties</span></span>

<span data-ttu-id="c5705-112">Die **udpip- \_ TypeGroup2** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c5705-112">The **UdpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5705-113">nicht konform</span><span class="sxs-lookup"><span data-stu-id="c5705-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5705-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5705-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5705-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5705-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5705-116">Qualifizierer: wmidataid (8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="c5705-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c5705-117">Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.</span><span class="sxs-lookup"><span data-stu-id="c5705-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="c5705-118">daddr</span><span class="sxs-lookup"><span data-stu-id="c5705-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5705-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c5705-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c5705-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5705-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5705-121">Qualifizierer: wmidataid (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="c5705-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="c5705-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c5705-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c5705-123">dport</span><span class="sxs-lookup"><span data-stu-id="c5705-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5705-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c5705-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c5705-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5705-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5705-126">Qualifizierer: wmidataid (5), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="c5705-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="c5705-127">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="c5705-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="c5705-128">PID</span><span class="sxs-lookup"><span data-stu-id="c5705-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5705-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5705-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5705-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5705-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5705-131">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="c5705-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="c5705-132">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c5705-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="c5705-133">saddr</span><span class="sxs-lookup"><span data-stu-id="c5705-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5705-134">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c5705-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c5705-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5705-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5705-136">Qualifizierer: wmidataid (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="c5705-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="c5705-137">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c5705-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c5705-138">SEQNUM</span><span class="sxs-lookup"><span data-stu-id="c5705-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5705-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5705-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5705-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5705-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5705-141">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="c5705-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="c5705-142">Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="c5705-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="c5705-143">size</span><span class="sxs-lookup"><span data-stu-id="c5705-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5705-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5705-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5705-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5705-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5705-146">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="c5705-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c5705-147">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="c5705-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="c5705-148">Reit</span><span class="sxs-lookup"><span data-stu-id="c5705-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5705-149">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c5705-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c5705-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5705-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5705-151">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="c5705-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="c5705-152">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="c5705-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5705-153">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c5705-153">Requirements</span></span>



| <span data-ttu-id="c5705-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5705-154">Requirement</span></span> | <span data-ttu-id="c5705-155">Wert</span><span class="sxs-lookup"><span data-stu-id="c5705-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5705-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5705-156">Minimum supported client</span></span><br/> | <span data-ttu-id="c5705-157">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5705-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c5705-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5705-158">Minimum supported server</span></span><br/> | <span data-ttu-id="c5705-159">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5705-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5705-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c5705-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5705-161">**Udpip**</span><span class="sxs-lookup"><span data-stu-id="c5705-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




