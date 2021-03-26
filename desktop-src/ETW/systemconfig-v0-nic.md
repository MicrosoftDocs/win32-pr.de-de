---
description: Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: SystemConfig_V0_NIC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980552"
---
# <a name="systemconfig_v0_nic-class"></a><span data-ttu-id="c6ce5-103">SystemConfig \_ v0- \_ NIC-Klasse</span><span class="sxs-lookup"><span data-stu-id="c6ce5-103">SystemConfig\_V0\_NIC class</span></span>

<span data-ttu-id="c6ce5-104">Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-104">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="c6ce5-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ce5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6ce5-106">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a><span data-ttu-id="c6ce5-107">Member</span><span class="sxs-lookup"><span data-stu-id="c6ce5-107">Members</span></span>

<span data-ttu-id="c6ce5-108">Die **System config \_ v0- \_ NIC** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c6ce5-108">The **SystemConfig\_V0\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="c6ce5-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6ce5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6ce5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6ce5-110">Properties</span></span>

<span data-ttu-id="c6ce5-111">Die **System config \_ v0- \_ NIC** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-111">The **SystemConfig\_V0\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6ce5-112">**Daten**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-115">Qualifizierer: **wmidataid** (16)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-115">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-116">Datenfeld.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-116">Data field.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-117">**DhcpServer**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-117">**DhcpServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-118">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-120">Qualifizierer: **wmidataid** (8)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-120">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-121">Die IP-Adresse des DHCP-Servers (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="c6ce5-121">IP address of the dynamic host configuration protocol (DHCP) server.</span></span> <span data-ttu-id="c6ce5-122">Der Wert 255.255.255.255 gibt an, dass der DHCP-Server nicht erreicht werden konnte oder gerade erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-122">A value of 255.255.255.255 indicates the DHCP server could not be reached, or is in the process of being reached.</span></span> <span data-ttu-id="c6ce5-123">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-123">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-124">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-124">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-125">**DnsServer1**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-125">**DnsServer1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-128">Qualifizierer: **wmidataid** (12)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-128">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-129">Die ersten Server-IP-Adressen, die zum Abfragen von DNS-Servern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-129">First server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="c6ce5-130">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-130">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-131">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-131">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-132">**DnsServer2**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-132">**DnsServer2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-133">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-135">Qualifizierer: **wmidataid** (13)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-135">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-136">Zweite Server-IP-Adressen, die zum Abfragen von DNS-Servern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-136">Second server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="c6ce5-137">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-137">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-138">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-138">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-139">**DnsServer3**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-139">**DnsServer3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-140">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-142">Qualifizierer: **wmidataid** (14)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-142">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-143">Dritte Server-IP-Adressen, die zum Abfragen von DNS-Servern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-143">Third server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="c6ce5-144">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-144">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-145">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-145">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-146">**DnsServer4**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-146">**DnsServer4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-149">Qualifizierer: **wmidataid** (15)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-149">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-150">Vierte Server-IP-Adressen, die beim Abfragen von DNS-Servern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-150">Fourth server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="c6ce5-151">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-151">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-152">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-152">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-153">**Gateway**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-153">**Gateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-154">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-156">Qualifizierer: **wmidataid** (9)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-156">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-157">Die IP-Adresse des Standard Gateways, das vom Computersystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-157">IP address of default gateway that the computer system uses.</span></span> <span data-ttu-id="c6ce5-158">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-158">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-159">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-159">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-160">**Index**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-160">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-161">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-163">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-163">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-164">Adapter Index.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-164">Adapter index.</span></span> <span data-ttu-id="c6ce5-165">Der Adapter Index kann sich ändern, wenn ein Adapter deaktiviert und dann aktiviert wird, oder unter anderen Umständen nicht als persistent eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-165">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-166">**IpAddress**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-166">**IpAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-167">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-167">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-169">Qualifizierer: **wmidataid** (6)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-169">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-170">IP-Adressen, die der Netzwerkschnittstellenkarte zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-170">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="c6ce5-171">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-171">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-172">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-172">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-173">**NICNAME**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-173">**NICName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-174">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="c6ce5-174">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-176">Qualifizierer: **wmidataid** (1), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-176">Qualifiers: **WmiDataId** (1), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-177">Der Name der Netzwerkschnittstellenkarte.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-177">Name of the network interface card.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-178">**Physicaladdr**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-178">**PhysicalAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-179">Datentyp: **char16**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-179">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-181">Qualifizierer: **wmidataid** (4), **Max** (8)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-181">Qualifiers: **WmiDataId** (4), **Max** (8)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-182">Die Hardware Adresse für den Adapter.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-182">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-183">**Physicaladdrlen**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-183">**PhysicalAddrLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-184">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-186">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-186">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-187">Länge der Hardwareadresse für den Adapter.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-187">Length of the hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-188">**Primarywinsserver**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-188">**PrimaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-189">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-191">Qualifizierer: **wmidataid** (10)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-191">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-192">Die IP-Adresse für den primären WINS-Server.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-192">IP address for the primary WINS server.</span></span> <span data-ttu-id="c6ce5-193">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-193">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-194">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-194">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-195">**Secondarywinsserver**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-195">**SecondaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-196">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-196">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-198">Qualifizierer: **wmidataid** (11)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-198">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-199">Die IP-Adresse für den sekundären WINS-Server.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-199">IP address for the secondary WINS server.</span></span> <span data-ttu-id="c6ce5-200">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-200">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-201">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-201">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-202">**Größe**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-202">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-203">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-205">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-205">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-206">Größe (in Bytes) der Dateneigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-206">Size, in bytes, of the Data property.</span></span>

</dd> <dt>

<span data-ttu-id="c6ce5-207">**SubnetMask**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-207">**SubnetMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ce5-208">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-208">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ce5-210">Qualifizierer: **wmidataid** (7)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-210">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="c6ce5-211">Die der Netzwerkschnittstellenkarte zugeordnete Subnetzmaske.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-211">Subnet mask associated with the network interface card.</span></span> <span data-ttu-id="c6ce5-212">Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-212">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c6ce5-213">Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.</span><span class="sxs-lookup"><span data-stu-id="c6ce5-213">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6ce5-214">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-214">Requirements</span></span>



| <span data-ttu-id="c6ce5-215">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6ce5-215">Requirement</span></span> | <span data-ttu-id="c6ce5-216">Wert</span><span class="sxs-lookup"><span data-stu-id="c6ce5-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6ce5-217">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-217">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ce5-218">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c6ce5-218">None supported</span></span><br/>                            |
| <span data-ttu-id="c6ce5-219">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6ce5-219">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ce5-220">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6ce5-220">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6ce5-221">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6ce5-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ce5-222">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="c6ce5-222">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




