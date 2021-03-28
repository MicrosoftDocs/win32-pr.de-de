---
description: Diese Klasse ist die Ereignistyp Klasse für IPv6-TCP/IP-Sende Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 231ef62f-e3a5-497d-b10a-79449dc73c71
title: TcpIp_SendIPV6-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV6
- TcpIp_SendIPV6.PID
- TcpIp_SendIPV6.size
- TcpIp_SendIPV6.daddr
- TcpIp_SendIPV6.saddr
- TcpIp_SendIPV6.dport
- TcpIp_SendIPV6.sport
- TcpIp_SendIPV6.startime
- TcpIp_SendIPV6.endtime
- TcpIp_SendIPV6.seqnum
- TcpIp_SendIPV6.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190b7d4fc64660b1e12240b6461e73066102b6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978257"
---
# <a name="tcpip_sendipv6-class"></a><span data-ttu-id="f52b4-104">Tcpip \_ SendIPV6-Klasse</span><span class="sxs-lookup"><span data-stu-id="f52b4-104">TcpIp\_SendIPV6 class</span></span>

<span data-ttu-id="f52b4-105">Diese Klasse ist die Ereignistyp Klasse für IPv6-TCP/IP-Sende Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f52b4-105">This class is the event type class for IPv6 TCP/IP send events.</span></span>

<span data-ttu-id="f52b4-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f52b4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f52b4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f52b4-107">Syntax</span></span>

``` syntax
[EventType{26}, EventTypeName{"SendIPV6"}]
class TcpIp_SendIPV6 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="f52b4-108">Member</span><span class="sxs-lookup"><span data-stu-id="f52b4-108">Members</span></span>

<span data-ttu-id="f52b4-109">Die **tcpip- \_ SendIPV6** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f52b4-109">The **TcpIp\_SendIPV6** class has these types of members:</span></span>

-   [<span data-ttu-id="f52b4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f52b4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f52b4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f52b4-111">Properties</span></span>

<span data-ttu-id="f52b4-112">Die **tcpip- \_ SendIPV6** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f52b4-112">The **TcpIp\_SendIPV6** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f52b4-113">nicht konform</span><span class="sxs-lookup"><span data-stu-id="f52b4-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f52b4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-116">Qualifizierer: wmidataid (10), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f52b4-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-117">Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.</span><span class="sxs-lookup"><span data-stu-id="f52b4-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="f52b4-118">daddr</span><span class="sxs-lookup"><span data-stu-id="f52b4-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="f52b4-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-121">Qualifizierer: wmidataid (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="f52b4-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f52b4-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f52b4-123">dport</span><span class="sxs-lookup"><span data-stu-id="f52b4-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="f52b4-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-126">Qualifizierer: wmidataid (5), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="f52b4-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-127">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="f52b4-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="f52b4-128">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="f52b4-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f52b4-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-131">Qualifizierer: wmidataid (8)</span><span class="sxs-lookup"><span data-stu-id="f52b4-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-132">Sende Anforderungs Zeit beenden.</span><span class="sxs-lookup"><span data-stu-id="f52b4-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="f52b4-133">PID</span><span class="sxs-lookup"><span data-stu-id="f52b4-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f52b4-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-136">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="f52b4-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-137">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f52b4-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="f52b4-138">saddr</span><span class="sxs-lookup"><span data-stu-id="f52b4-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-139">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="f52b4-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-141">Qualifizierer: wmidataid (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="f52b4-141">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-142">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f52b4-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f52b4-143">SEQNUM</span><span class="sxs-lookup"><span data-stu-id="f52b4-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f52b4-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-146">Qualifizierer: wmidataid (9)</span><span class="sxs-lookup"><span data-stu-id="f52b4-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-147">Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="f52b4-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="f52b4-148">size</span><span class="sxs-lookup"><span data-stu-id="f52b4-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f52b4-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-151">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="f52b4-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-152">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="f52b4-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="f52b4-153">Reit</span><span class="sxs-lookup"><span data-stu-id="f52b4-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-154">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="f52b4-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-156">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="f52b4-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-157">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="f52b4-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="f52b4-158">**Startzeit**</span><span class="sxs-lookup"><span data-stu-id="f52b4-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f52b4-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f52b4-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f52b4-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f52b4-161">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="f52b4-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="f52b4-162">Sende Anforderungs Zeit starten.</span><span class="sxs-lookup"><span data-stu-id="f52b4-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f52b4-163">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f52b4-163">Requirements</span></span>



| <span data-ttu-id="f52b4-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f52b4-164">Requirement</span></span> | <span data-ttu-id="f52b4-165">Wert</span><span class="sxs-lookup"><span data-stu-id="f52b4-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f52b4-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f52b4-166">Minimum supported client</span></span><br/> | <span data-ttu-id="f52b4-167">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f52b4-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f52b4-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f52b4-168">Minimum supported server</span></span><br/> | <span data-ttu-id="f52b4-169">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f52b4-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f52b4-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f52b4-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52b4-171">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="f52b4-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




