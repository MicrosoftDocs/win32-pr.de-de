---
description: Diese Klasse ist die Ereignistyp Klasse für IPv6-TCP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: d24e667e-ec7f-492a-989e-a02ff4c8ac10
title: TcpIp_TypeGroup3-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup3
- TcpIp_TypeGroup3.PID
- TcpIp_TypeGroup3.size
- TcpIp_TypeGroup3.daddr
- TcpIp_TypeGroup3.saddr
- TcpIp_TypeGroup3.dport
- TcpIp_TypeGroup3.sport
- TcpIp_TypeGroup3.seqnum
- TcpIp_TypeGroup3.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 82aa119c0d770a26060b1e8d6ab74433146bb3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978248"
---
# <a name="tcpip_typegroup3-class"></a><span data-ttu-id="2cc0f-104">Tcpip \_ TypeGroup3-Klasse</span><span class="sxs-lookup"><span data-stu-id="2cc0f-104">TcpIp\_TypeGroup3 class</span></span>

<span data-ttu-id="2cc0f-105">Diese Klasse ist die Ereignistyp Klasse für IPv6-TCP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-105">This class is the event type class for IPv6 TCP/IP events.</span></span>

<span data-ttu-id="2cc0f-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc0f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cc0f-107">Syntax</span></span>

``` syntax
[EventType{27, 29, 30, 32, 34}, EventTypeName{"RecvIPV6", "DisconnectIPV6", "RetransmitIPV6", "ReconnectIPV6", "TCPCopyIPV6"}]
class TcpIp_TypeGroup3 : TcpIp
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

## <a name="members"></a><span data-ttu-id="2cc0f-108">Member</span><span class="sxs-lookup"><span data-stu-id="2cc0f-108">Members</span></span>

<span data-ttu-id="2cc0f-109">Die **tcpip- \_ TypeGroup3** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2cc0f-109">The **TcpIp\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="2cc0f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2cc0f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2cc0f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2cc0f-111">Properties</span></span>

<span data-ttu-id="2cc0f-112">Die **tcpip- \_ TypeGroup3** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-112">The **TcpIp\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2cc0f-113">nicht konform</span><span class="sxs-lookup"><span data-stu-id="2cc0f-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc0f-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2cc0f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2cc0f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-116">Qualifizierer: wmidataid (6), Zeiger</span><span class="sxs-lookup"><span data-stu-id="2cc0f-116">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2cc0f-117">Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0f-118">daddr</span><span class="sxs-lookup"><span data-stu-id="2cc0f-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc0f-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="2cc0f-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2cc0f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-121">Qualifizierer: wmidataid (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="2cc0f-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="2cc0f-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0f-123">dport</span><span class="sxs-lookup"><span data-stu-id="2cc0f-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc0f-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="2cc0f-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2cc0f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-126">Qualifizierer: wmidataid (5), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="2cc0f-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="2cc0f-127">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0f-128">PID</span><span class="sxs-lookup"><span data-stu-id="2cc0f-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc0f-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2cc0f-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2cc0f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-131">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="2cc0f-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="2cc0f-132">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0f-133">saddr</span><span class="sxs-lookup"><span data-stu-id="2cc0f-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc0f-134">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="2cc0f-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2cc0f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-136">Qualifizierer: wmidataid (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="2cc0f-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="2cc0f-137">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0f-138">SEQNUM</span><span class="sxs-lookup"><span data-stu-id="2cc0f-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc0f-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2cc0f-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2cc0f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-141">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="2cc0f-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="2cc0f-142">Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0f-143">size</span><span class="sxs-lookup"><span data-stu-id="2cc0f-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc0f-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2cc0f-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2cc0f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-146">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="2cc0f-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2cc0f-147">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0f-148">Reit</span><span class="sxs-lookup"><span data-stu-id="2cc0f-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc0f-149">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="2cc0f-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2cc0f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc0f-151">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="2cc0f-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="2cc0f-152">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cc0f-153">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2cc0f-153">Requirements</span></span>



| <span data-ttu-id="2cc0f-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cc0f-154">Requirement</span></span> | <span data-ttu-id="2cc0f-155">Wert</span><span class="sxs-lookup"><span data-stu-id="2cc0f-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2cc0f-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cc0f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc0f-157">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cc0f-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2cc0f-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cc0f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc0f-159">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cc0f-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cc0f-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2cc0f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc0f-161">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="2cc0f-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




