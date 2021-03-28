---
description: Diese Klasse ist die Ereignistyp Klasse für IPv4-TCP/IP Connect-und Accept-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: TcpIp_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528220"
---
# <a name="tcpip_typegroup2-class"></a><span data-ttu-id="44a01-104">Tcpip \_ TypeGroup2-Klasse</span><span class="sxs-lookup"><span data-stu-id="44a01-104">TcpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="44a01-105">Diese Klasse ist die Ereignistyp Klasse für IPv4-TCP/IP Connect-und Accept-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="44a01-105">This class is the event type class for IPv4 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="44a01-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="44a01-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a01-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="44a01-107">Syntax</span></span>

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
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

## <a name="members"></a><span data-ttu-id="44a01-108">Member</span><span class="sxs-lookup"><span data-stu-id="44a01-108">Members</span></span>

<span data-ttu-id="44a01-109">Die **tcpip- \_ TypeGroup2** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="44a01-109">The **TcpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="44a01-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44a01-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44a01-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44a01-111">Properties</span></span>

<span data-ttu-id="44a01-112">Die **tcpip- \_ TypeGroup2** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="44a01-112">The **TcpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44a01-113">**nicht konform**</span><span class="sxs-lookup"><span data-stu-id="44a01-113">**connid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44a01-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-116">Qualifizierer: **wmidataid (15)**, **Zeiger**</span><span class="sxs-lookup"><span data-stu-id="44a01-116">Qualifiers: **WmiDataId(15)**, **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-117">Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.</span><span class="sxs-lookup"><span data-stu-id="44a01-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-118">**daddr**</span><span class="sxs-lookup"><span data-stu-id="44a01-118">**daddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="44a01-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-121">Qualifizierer: **wmidataid (3)**, **Extension ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="44a01-121">Qualifiers: **WmiDataId(3)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="44a01-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-123">**dport**</span><span class="sxs-lookup"><span data-stu-id="44a01-123">**dport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="44a01-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-126">Qualifizierer: **wmidataid (5)**, **Erweiterung ("Port")**</span><span class="sxs-lookup"><span data-stu-id="44a01-126">Qualifiers: **WmiDataId(5)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-127">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="44a01-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="44a01-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44a01-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-131">Qualifizierer: **wmidataid (7)**</span><span class="sxs-lookup"><span data-stu-id="44a01-131">Qualifiers: **WmiDataId(7)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-132">Maximale Segmentgröße.</span><span class="sxs-lookup"><span data-stu-id="44a01-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-133">**Lauer**</span><span class="sxs-lookup"><span data-stu-id="44a01-133">**PID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44a01-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-136">Qualifizierer: **wmidataid (1)**</span><span class="sxs-lookup"><span data-stu-id="44a01-136">Qualifiers: **WmiDataId(1)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-137">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="44a01-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="44a01-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44a01-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-141">Qualifizierer: **wmidataid (11)**</span><span class="sxs-lookup"><span data-stu-id="44a01-141">Qualifiers: **WmiDataId(11)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-142">TCP-Empfangs Fenstergröße.</span><span class="sxs-lookup"><span data-stu-id="44a01-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="44a01-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-144">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="44a01-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-146">Qualifizierer: **wmidataid (12)**</span><span class="sxs-lookup"><span data-stu-id="44a01-146">Qualifiers: **WmiDataId(12)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-147">Skalierungsfaktor für TCP-Empfangs Fenster.</span><span class="sxs-lookup"><span data-stu-id="44a01-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="44a01-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44a01-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-151">Qualifizierer: **wmidataid (8)**</span><span class="sxs-lookup"><span data-stu-id="44a01-151">Qualifiers: **WmiDataId(8)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-152">Die Option für die selektive Bestätigung (ACK) im TCP-Header.</span><span class="sxs-lookup"><span data-stu-id="44a01-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-153">**saddr**</span><span class="sxs-lookup"><span data-stu-id="44a01-153">**saddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-154">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="44a01-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-156">Qualifizierer: **wmidataid (4)**, **Extension ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="44a01-156">Qualifiers: **WmiDataId(4)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-157">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="44a01-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-158">**SEQNUM**</span><span class="sxs-lookup"><span data-stu-id="44a01-158">**seqnum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44a01-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-161">Qualifizierer: **wmidataid (14)**</span><span class="sxs-lookup"><span data-stu-id="44a01-161">Qualifiers: **WmiDataId(14)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-162">Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="44a01-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-163">**size**</span><span class="sxs-lookup"><span data-stu-id="44a01-163">**size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-164">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44a01-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-166">Qualifizierer: **wmidataid (2)**</span><span class="sxs-lookup"><span data-stu-id="44a01-166">Qualifiers: **WmiDataId(2)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-167">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="44a01-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="44a01-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-169">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="44a01-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-171">Qualifizierer: **wmidataid (13)**</span><span class="sxs-lookup"><span data-stu-id="44a01-171">Qualifiers: **WmiDataId(13)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-172">Skalierungsfaktor für TCP-Sendefenster.</span><span class="sxs-lookup"><span data-stu-id="44a01-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-173">**Reit**</span><span class="sxs-lookup"><span data-stu-id="44a01-173">**sport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-174">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="44a01-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-176">Qualifizierer: **wmidataid (6)**, **Erweiterung ("Port")**</span><span class="sxs-lookup"><span data-stu-id="44a01-176">Qualifiers: **WmiDataId(6)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-177">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="44a01-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-178">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="44a01-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-179">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44a01-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-181">Qualifizierer: **wmidataid (9)**</span><span class="sxs-lookup"><span data-stu-id="44a01-181">Qualifiers: **WmiDataId(9)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-182">Zeitstempel Option im TCP-Header.</span><span class="sxs-lookup"><span data-stu-id="44a01-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="44a01-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="44a01-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a01-184">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44a01-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44a01-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44a01-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a01-186">Qualifizierer: **wmidataid (10)**</span><span class="sxs-lookup"><span data-stu-id="44a01-186">Qualifiers: **WmiDataId(10)**</span></span>
</dt> </dl>

<span data-ttu-id="44a01-187">Fenster Skalierungs Option im TCP-Header.</span><span class="sxs-lookup"><span data-stu-id="44a01-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44a01-188">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="44a01-188">Requirements</span></span>



| <span data-ttu-id="44a01-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44a01-189">Requirement</span></span> | <span data-ttu-id="44a01-190">Wert</span><span class="sxs-lookup"><span data-stu-id="44a01-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44a01-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44a01-191">Minimum supported client</span></span><br/> | <span data-ttu-id="44a01-192">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44a01-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44a01-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44a01-193">Minimum supported server</span></span><br/> | <span data-ttu-id="44a01-194">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44a01-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44a01-195">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="44a01-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a01-196">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="44a01-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




