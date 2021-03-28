---
description: Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: SystemConfig_NIC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958961"
---
# <a name="systemconfig_nic-class"></a><span data-ttu-id="9a3d9-104">SystemConfig- \_ NIC-Klasse</span><span class="sxs-lookup"><span data-stu-id="9a3d9-104">SystemConfig\_NIC class</span></span>

<span data-ttu-id="9a3d9-105">Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-105">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="9a3d9-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a3d9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a3d9-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a><span data-ttu-id="9a3d9-108">Member</span><span class="sxs-lookup"><span data-stu-id="9a3d9-108">Members</span></span>

<span data-ttu-id="9a3d9-109">Die **\_ NIC** -Klasse von SystemConfig verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9a3d9-109">The **SystemConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="9a3d9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9a3d9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a3d9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9a3d9-111">Properties</span></span>

<span data-ttu-id="9a3d9-112">Die **SystemConfig- \_ NIC** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-112">The **SystemConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a3d9-113">Dnsserveradressen</span><span class="sxs-lookup"><span data-stu-id="9a3d9-113">DnsServerAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a3d9-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a3d9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-116">Qualifizierer: wmidataid (7), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="9a3d9-116">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="9a3d9-117">IP-Adressen, die zum Abfragen von DNS-Servern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-117">IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="9a3d9-118">Die Liste der Adressen ist durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-118">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="9a3d9-119">IpAddresses</span><span class="sxs-lookup"><span data-stu-id="9a3d9-119">IpAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a3d9-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a3d9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-122">Qualifizierer: wmidataid (6), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="9a3d9-122">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="9a3d9-123">IP-Adressen, die der Netzwerkschnittstellenkarte zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-123">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="9a3d9-124">Die Liste der Adressen ist durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-124">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="9a3d9-125">Ipv4Index</span><span class="sxs-lookup"><span data-stu-id="9a3d9-125">Ipv4Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a3d9-126">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a3d9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-128">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="9a3d9-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="9a3d9-129">Adapter Index für IPv4-NIC.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-129">Adapter index for IPv4 NIC.</span></span> <span data-ttu-id="9a3d9-130">Der Adapter Index kann sich ändern, wenn ein Adapter deaktiviert und dann aktiviert wird, oder unter anderen Umständen nicht als persistent eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-130">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="9a3d9-131">Ipv6Index</span><span class="sxs-lookup"><span data-stu-id="9a3d9-131">Ipv6Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a3d9-132">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a3d9-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-134">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="9a3d9-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="9a3d9-135">Adapter Index für IPv6-NIC.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-135">Adapter index for IPv6 NIC.</span></span> <span data-ttu-id="9a3d9-136">Der Adapter Index kann sich ändern, wenn ein Adapter deaktiviert und dann aktiviert wird, oder unter anderen Umständen nicht als persistent eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-136">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="9a3d9-137">Nicdescription</span><span class="sxs-lookup"><span data-stu-id="9a3d9-137">NICDescription</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a3d9-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a3d9-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-140">Qualifizierer: wmidataid (5), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="9a3d9-140">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="9a3d9-141">Die Beschreibung des Adapters.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-141">Description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9a3d9-142">Physicaladdr</span><span class="sxs-lookup"><span data-stu-id="9a3d9-142">PhysicalAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a3d9-143">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a3d9-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-145">Qualifizierer: wmidataid (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="9a3d9-145">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="9a3d9-146">Die Hardware Adresse für den Adapter.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-146">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9a3d9-147">Physicaladdrlen</span><span class="sxs-lookup"><span data-stu-id="9a3d9-147">PhysicalAddrLen</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a3d9-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a3d9-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a3d9-150">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="9a3d9-150">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9a3d9-151">Länge der Hardwareadresse für den Adapter.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-151">Length of the hardware address for the adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a3d9-152">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9a3d9-152">Requirements</span></span>



| <span data-ttu-id="9a3d9-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a3d9-153">Requirement</span></span> | <span data-ttu-id="9a3d9-154">Wert</span><span class="sxs-lookup"><span data-stu-id="9a3d9-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a3d9-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a3d9-155">Minimum supported client</span></span><br/> | <span data-ttu-id="9a3d9-156">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a3d9-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9a3d9-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a3d9-157">Minimum supported server</span></span><br/> | <span data-ttu-id="9a3d9-158">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a3d9-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a3d9-159">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a3d9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a3d9-160">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-160">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




