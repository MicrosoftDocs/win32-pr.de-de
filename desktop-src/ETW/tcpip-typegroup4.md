---
description: Diese Klasse ist die Ereignistyp Klasse für IPv6-TCP/IP Connect-und Accept-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: c6c0463a-0058-47cf-9235-d2b621f30fb4
title: TcpIp_TypeGroup4-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup4
- TcpIp_TypeGroup4.PID
- TcpIp_TypeGroup4.size
- TcpIp_TypeGroup4.daddr
- TcpIp_TypeGroup4.saddr
- TcpIp_TypeGroup4.dport
- TcpIp_TypeGroup4.sport
- TcpIp_TypeGroup4.mss
- TcpIp_TypeGroup4.sackopt
- TcpIp_TypeGroup4.tsopt
- TcpIp_TypeGroup4.wsopt
- TcpIp_TypeGroup4.rcvwin
- TcpIp_TypeGroup4.rcvwinscale
- TcpIp_TypeGroup4.sndwinscale
- TcpIp_TypeGroup4.seqnum
- TcpIp_TypeGroup4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 942e5897db6771c0c3a9df965e5e889eaf71c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754249"
---
# <a name="tcpip_typegroup4-class"></a><span data-ttu-id="b6c60-104">Tcpip \_ TypeGroup4-Klasse</span><span class="sxs-lookup"><span data-stu-id="b6c60-104">TcpIp\_TypeGroup4 class</span></span>

<span data-ttu-id="b6c60-105">Diese Klasse ist die Ereignistyp Klasse für IPv6-TCP/IP Connect-und Accept-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b6c60-105">This class is the event type class for IPv6 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="b6c60-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="b6c60-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c60-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6c60-107">Syntax</span></span>

``` syntax
[EventType{28, 31}, EventTypeName{"ConnectIPV6", "AcceptIPV6"}]
class TcpIp_TypeGroup4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="b6c60-108">Member</span><span class="sxs-lookup"><span data-stu-id="b6c60-108">Members</span></span>

<span data-ttu-id="b6c60-109">Die **tcpip- \_ TypeGroup4** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b6c60-109">The **TcpIp\_TypeGroup4** class has these types of members:</span></span>

-   [<span data-ttu-id="b6c60-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6c60-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6c60-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6c60-111">Properties</span></span>

<span data-ttu-id="b6c60-112">Die **tcpip- \_ TypeGroup4** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b6c60-112">The **TcpIp\_TypeGroup4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6c60-113">nicht konform</span><span class="sxs-lookup"><span data-stu-id="b6c60-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6c60-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-116">Qualifizierer: wmidataid (15), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b6c60-116">Qualifiers: WmiDataId(15), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-117">Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.</span><span class="sxs-lookup"><span data-stu-id="b6c60-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-118">daddr</span><span class="sxs-lookup"><span data-stu-id="b6c60-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="b6c60-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-121">Qualifizierer: wmidataid (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="b6c60-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b6c60-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-123">dport</span><span class="sxs-lookup"><span data-stu-id="b6c60-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="b6c60-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-126">Qualifizierer: wmidataid (5), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="b6c60-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-127">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="b6c60-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="b6c60-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6c60-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-131">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="b6c60-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-132">Maximale Segmentgröße.</span><span class="sxs-lookup"><span data-stu-id="b6c60-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-133">PID</span><span class="sxs-lookup"><span data-stu-id="b6c60-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6c60-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-136">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="b6c60-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-137">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b6c60-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="b6c60-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6c60-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-141">Qualifizierer: wmidataid (11)</span><span class="sxs-lookup"><span data-stu-id="b6c60-141">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-142">TCP-Empfangs Fenstergröße.</span><span class="sxs-lookup"><span data-stu-id="b6c60-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="b6c60-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-144">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="b6c60-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-146">Qualifizierer: wmidataid (12)</span><span class="sxs-lookup"><span data-stu-id="b6c60-146">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-147">Skalierungsfaktor für TCP-Empfangs Fenster.</span><span class="sxs-lookup"><span data-stu-id="b6c60-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="b6c60-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6c60-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-151">Qualifizierer: **wmidataid** (8)</span><span class="sxs-lookup"><span data-stu-id="b6c60-151">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-152">Die Option für die selektive Bestätigung (ACK) im TCP-Header.</span><span class="sxs-lookup"><span data-stu-id="b6c60-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-153">saddr</span><span class="sxs-lookup"><span data-stu-id="b6c60-153">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-154">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="b6c60-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-156">Qualifizierer: wmidataid (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="b6c60-156">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-157">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b6c60-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-158">SEQNUM</span><span class="sxs-lookup"><span data-stu-id="b6c60-158">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6c60-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-161">Qualifizierer: wmidataid (14)</span><span class="sxs-lookup"><span data-stu-id="b6c60-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-162">Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="b6c60-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-163">size</span><span class="sxs-lookup"><span data-stu-id="b6c60-163">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-164">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6c60-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-166">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="b6c60-166">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-167">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="b6c60-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="b6c60-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-169">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="b6c60-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-171">Qualifizierer: wmidataid (13)</span><span class="sxs-lookup"><span data-stu-id="b6c60-171">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-172">Skalierungsfaktor für TCP-Sendefenster.</span><span class="sxs-lookup"><span data-stu-id="b6c60-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-173">Reit</span><span class="sxs-lookup"><span data-stu-id="b6c60-173">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-174">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="b6c60-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-176">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="b6c60-176">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-177">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="b6c60-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-178">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="b6c60-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-179">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6c60-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-181">Qualifizierer: wmidataid (9)</span><span class="sxs-lookup"><span data-stu-id="b6c60-181">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-182">Zeitstempel Option im TCP-Header.</span><span class="sxs-lookup"><span data-stu-id="b6c60-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="b6c60-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="b6c60-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c60-184">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6c60-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6c60-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c60-186">Qualifizierer: wmidataid (10)</span><span class="sxs-lookup"><span data-stu-id="b6c60-186">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="b6c60-187">Fenster Skalierungs Option im TCP-Header.</span><span class="sxs-lookup"><span data-stu-id="b6c60-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6c60-188">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b6c60-188">Requirements</span></span>



| <span data-ttu-id="b6c60-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6c60-189">Requirement</span></span> | <span data-ttu-id="b6c60-190">Wert</span><span class="sxs-lookup"><span data-stu-id="b6c60-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6c60-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6c60-191">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c60-192">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6c60-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b6c60-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6c60-193">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c60-194">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6c60-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6c60-195">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b6c60-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c60-196">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="b6c60-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




