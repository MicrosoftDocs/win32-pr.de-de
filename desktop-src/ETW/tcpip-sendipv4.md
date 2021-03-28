---
description: Diese Klasse ist die Ereignistyp Klasse für IPv4-TCP/IP-Sende Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 51a61257-fcbf-4724-80e4-12bdf45b359e
title: TcpIp_SendIPV4-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV4
- TcpIp_SendIPV4.PID
- TcpIp_SendIPV4.size
- TcpIp_SendIPV4.daddr
- TcpIp_SendIPV4.saddr
- TcpIp_SendIPV4.dport
- TcpIp_SendIPV4.sport
- TcpIp_SendIPV4.startime
- TcpIp_SendIPV4.endtime
- TcpIp_SendIPV4.seqnum
- TcpIp_SendIPV4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: a255c8a262c53e6dad4654946171fc19a43c6f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959282"
---
# <a name="tcpip_sendipv4-class"></a><span data-ttu-id="5578f-104">Tcpip \_ SendIPV4-Klasse</span><span class="sxs-lookup"><span data-stu-id="5578f-104">TcpIp\_SendIPV4 class</span></span>

<span data-ttu-id="5578f-105">Diese Klasse ist die Ereignistyp Klasse für IPv4-TCP/IP-Sende Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="5578f-105">This class is the event type class for IPv4 TCP/IP send events.</span></span>

<span data-ttu-id="5578f-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="5578f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5578f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5578f-107">Syntax</span></span>

``` syntax
[EventType{10}, EventTypeName{"SendIPV4"}]
class TcpIp_SendIPV4 : TcpIp
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

## <a name="members"></a><span data-ttu-id="5578f-108">Member</span><span class="sxs-lookup"><span data-stu-id="5578f-108">Members</span></span>

<span data-ttu-id="5578f-109">Die **tcpip- \_ SendIPV4** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5578f-109">The **TcpIp\_SendIPV4** class has these types of members:</span></span>

-   [<span data-ttu-id="5578f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5578f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5578f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5578f-111">Properties</span></span>

<span data-ttu-id="5578f-112">Die **tcpip- \_ SendIPV4** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5578f-112">The **TcpIp\_SendIPV4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5578f-113">nicht konform</span><span class="sxs-lookup"><span data-stu-id="5578f-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5578f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-116">Qualifizierer: wmidataid (10), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5578f-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5578f-117">Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.</span><span class="sxs-lookup"><span data-stu-id="5578f-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="5578f-118">daddr</span><span class="sxs-lookup"><span data-stu-id="5578f-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="5578f-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-121">Qualifizierer: wmidataid (3), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="5578f-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="5578f-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5578f-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5578f-123">dport</span><span class="sxs-lookup"><span data-stu-id="5578f-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="5578f-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-126">Qualifizierer: wmidataid (5), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="5578f-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="5578f-127">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="5578f-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="5578f-128">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="5578f-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5578f-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-131">Qualifizierer: wmidataid (8)</span><span class="sxs-lookup"><span data-stu-id="5578f-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="5578f-132">Sende Anforderungs Zeit beenden.</span><span class="sxs-lookup"><span data-stu-id="5578f-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="5578f-133">PID</span><span class="sxs-lookup"><span data-stu-id="5578f-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5578f-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-136">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="5578f-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="5578f-137">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5578f-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="5578f-138">saddr</span><span class="sxs-lookup"><span data-stu-id="5578f-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-139">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="5578f-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-141">Qualifizierer: wmidataid (4), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="5578f-141">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="5578f-142">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5578f-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5578f-143">SEQNUM</span><span class="sxs-lookup"><span data-stu-id="5578f-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5578f-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-146">Qualifizierer: wmidataid (9)</span><span class="sxs-lookup"><span data-stu-id="5578f-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="5578f-147">Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="5578f-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="5578f-148">size</span><span class="sxs-lookup"><span data-stu-id="5578f-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5578f-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-151">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="5578f-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="5578f-152">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="5578f-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="5578f-153">Reit</span><span class="sxs-lookup"><span data-stu-id="5578f-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-154">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="5578f-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-156">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="5578f-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="5578f-157">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="5578f-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="5578f-158">**Startzeit**</span><span class="sxs-lookup"><span data-stu-id="5578f-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5578f-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5578f-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5578f-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5578f-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5578f-161">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="5578f-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="5578f-162">Sende Anforderungs Zeit starten.</span><span class="sxs-lookup"><span data-stu-id="5578f-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5578f-163">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5578f-163">Requirements</span></span>



| <span data-ttu-id="5578f-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5578f-164">Requirement</span></span> | <span data-ttu-id="5578f-165">Wert</span><span class="sxs-lookup"><span data-stu-id="5578f-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5578f-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5578f-166">Minimum supported client</span></span><br/> | <span data-ttu-id="5578f-167">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5578f-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5578f-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5578f-168">Minimum supported server</span></span><br/> | <span data-ttu-id="5578f-169">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5578f-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5578f-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5578f-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5578f-171">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="5578f-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




