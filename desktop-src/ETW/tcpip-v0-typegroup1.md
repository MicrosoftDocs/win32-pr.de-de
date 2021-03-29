---
description: Diese Klasse ist die Ereignistyp Klasse für TCP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: TcpIp_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c21025990fe3e21cd5322b651e543472fa8d48c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344549"
---
# <a name="tcpip_v0_typegroup1-class"></a><span data-ttu-id="8c2a7-104">Tcpip \_ v0 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="8c2a7-104">TcpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="8c2a7-105">Diese Klasse ist die Ereignistyp Klasse für TCP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="8c2a7-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2a7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c2a7-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a><span data-ttu-id="8c2a7-108">Member</span><span class="sxs-lookup"><span data-stu-id="8c2a7-108">Members</span></span>

<span data-ttu-id="8c2a7-109">Die Klasse " **tcpip \_ v0 \_ TypeGroup1** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8c2a7-109">The **TcpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="8c2a7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c2a7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c2a7-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c2a7-111">Properties</span></span>

<span data-ttu-id="8c2a7-112">Die **tcpip \_ v0 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-112">The **TcpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c2a7-113">daddr</span><span class="sxs-lookup"><span data-stu-id="8c2a7-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2a7-114">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="8c2a7-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c2a7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-116">Qualifizierer: wmidataid (1), Erweiterung ("ipaddr")</span><span class="sxs-lookup"><span data-stu-id="8c2a7-116">Qualifiers: WmiDataId(1), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="8c2a7-117">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8c2a7-118">dport</span><span class="sxs-lookup"><span data-stu-id="8c2a7-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2a7-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="8c2a7-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c2a7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-121">Qualifizierer: wmidataid (3), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="8c2a7-121">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="8c2a7-122">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="8c2a7-123">PID</span><span class="sxs-lookup"><span data-stu-id="8c2a7-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2a7-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c2a7-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c2a7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-126">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="8c2a7-126">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="8c2a7-127">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="8c2a7-128">saddr</span><span class="sxs-lookup"><span data-stu-id="8c2a7-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2a7-129">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="8c2a7-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c2a7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-131">Qualifizierer: wmidataid (2), Erweiterung ("ipaddr")</span><span class="sxs-lookup"><span data-stu-id="8c2a7-131">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="8c2a7-132">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8c2a7-133">size</span><span class="sxs-lookup"><span data-stu-id="8c2a7-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2a7-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c2a7-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c2a7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-136">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="8c2a7-136">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="8c2a7-137">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="8c2a7-138">Reit</span><span class="sxs-lookup"><span data-stu-id="8c2a7-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2a7-139">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="8c2a7-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c2a7-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2a7-141">Qualifizierer: wmidataid (4), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="8c2a7-141">Qualifiers: WmiDataId(4), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="8c2a7-142">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c2a7-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8c2a7-143">Requirements</span></span>



| <span data-ttu-id="8c2a7-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c2a7-144">Requirement</span></span> | <span data-ttu-id="8c2a7-145">Wert</span><span class="sxs-lookup"><span data-stu-id="8c2a7-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="8c2a7-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c2a7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2a7-147">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c2a7-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8c2a7-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c2a7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2a7-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8c2a7-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="8c2a7-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8c2a7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2a7-151">**Tcpip \_ v0**</span><span class="sxs-lookup"><span data-stu-id="8c2a7-151">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> </dl>

 

 




