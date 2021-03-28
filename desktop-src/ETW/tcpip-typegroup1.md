---
description: Diese Klasse ist die Ereignistyp Klasse für IPv4-TCP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: ed835df8-6f53-46a3-abf2-c66a1f13f987
title: TcpIp_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup1
- TcpIp_TypeGroup1.PID
- TcpIp_TypeGroup1.size
- TcpIp_TypeGroup1.daddr
- TcpIp_TypeGroup1.saddr
- TcpIp_TypeGroup1.dport
- TcpIp_TypeGroup1.sport
- TcpIp_TypeGroup1.seqnum
- TcpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 70ac95d3d3de5a9bcef610607f3b5a9046b63ea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978264"
---
# <a name="tcpip_typegroup1-class"></a><span data-ttu-id="37117-104">Tcpip \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="37117-104">TcpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="37117-105">Diese Klasse ist die Ereignistyp Klasse für IPv4-TCP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="37117-105">This class is the event type class for IPv4 TCP/IP events.</span></span>

<span data-ttu-id="37117-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="37117-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="37117-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37117-107">Syntax</span></span>

``` syntax
[EventType{11, 13, 14, 16, 18}, EventTypeName{"RecvIPV4", "DisconnectIPV4", "RetransmitIPV4", "ReconnectIPV4", "TCPCopyIPV4"}]
class TcpIp_TypeGroup1 : TcpIp
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

## <a name="members"></a><span data-ttu-id="37117-108">Member</span><span class="sxs-lookup"><span data-stu-id="37117-108">Members</span></span>

<span data-ttu-id="37117-109">Die **tcpip- \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="37117-109">The **TcpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="37117-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37117-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37117-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37117-111">Properties</span></span>

<span data-ttu-id="37117-112">Die **tcpip- \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37117-112">The **TcpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37117-113">nicht konform</span><span class="sxs-lookup"><span data-stu-id="37117-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37117-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37117-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37117-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37117-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37117-116">Qualifizierer: wmidataid (8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="37117-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="37117-117">Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.</span><span class="sxs-lookup"><span data-stu-id="37117-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="37117-118">daddr</span><span class="sxs-lookup"><span data-stu-id="37117-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37117-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="37117-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="37117-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37117-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37117-121">Qualifizierer: wmidataid (3), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="37117-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="37117-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="37117-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="37117-123">dport</span><span class="sxs-lookup"><span data-stu-id="37117-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37117-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="37117-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="37117-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37117-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37117-126">Qualifizierer: wmidataid (5), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="37117-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="37117-127">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="37117-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="37117-128">PID</span><span class="sxs-lookup"><span data-stu-id="37117-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37117-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37117-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37117-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37117-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37117-131">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="37117-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="37117-132">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="37117-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="37117-133">saddr</span><span class="sxs-lookup"><span data-stu-id="37117-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37117-134">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="37117-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="37117-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37117-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37117-136">Qualifizierer: wmidataid (4), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="37117-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="37117-137">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="37117-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="37117-138">SEQNUM</span><span class="sxs-lookup"><span data-stu-id="37117-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37117-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37117-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37117-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37117-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37117-141">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="37117-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="37117-142">Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="37117-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="37117-143">size</span><span class="sxs-lookup"><span data-stu-id="37117-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37117-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37117-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37117-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37117-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37117-146">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="37117-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="37117-147">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="37117-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="37117-148">Reit</span><span class="sxs-lookup"><span data-stu-id="37117-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37117-149">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="37117-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="37117-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37117-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37117-151">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="37117-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="37117-152">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="37117-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37117-153">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="37117-153">Requirements</span></span>



| <span data-ttu-id="37117-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37117-154">Requirement</span></span> | <span data-ttu-id="37117-155">Wert</span><span class="sxs-lookup"><span data-stu-id="37117-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37117-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37117-156">Minimum supported client</span></span><br/> | <span data-ttu-id="37117-157">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37117-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="37117-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37117-158">Minimum supported server</span></span><br/> | <span data-ttu-id="37117-159">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37117-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37117-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="37117-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37117-161">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="37117-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




