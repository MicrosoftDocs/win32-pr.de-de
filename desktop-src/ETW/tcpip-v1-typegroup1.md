---
description: Diese Klasse ist die Ereignistyp Klasse für TCP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: TcpIp_V1_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V1_TypeGroup1
- TcpIp_V1_TypeGroup1.PID
- TcpIp_V1_TypeGroup1.size
- TcpIp_V1_TypeGroup1.daddr
- TcpIp_V1_TypeGroup1.saddr
- TcpIp_V1_TypeGroup1.dport
- TcpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: fcd5f19eafa5308ef369a211559c6c464427b168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978233"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="69f24-104">Tcpip \_ v1 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="69f24-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="69f24-105">Diese Klasse ist die Ereignistyp Klasse für TCP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="69f24-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="69f24-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="69f24-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f24-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="69f24-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept", "Reconnect"}]
class TcpIp_V1_TypeGroup1 : TcpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="69f24-108">Member</span><span class="sxs-lookup"><span data-stu-id="69f24-108">Members</span></span>

<span data-ttu-id="69f24-109">Die Klasse " **tcpip \_ v1 \_ TypeGroup1** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="69f24-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="69f24-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69f24-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69f24-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69f24-111">Properties</span></span>

<span data-ttu-id="69f24-112">Die Klasse **tcpip \_ v1 \_ TypeGroup1** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69f24-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69f24-113">daddr</span><span class="sxs-lookup"><span data-stu-id="69f24-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69f24-114">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="69f24-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="69f24-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69f24-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69f24-116">Qualifizierer: wmidataid (3), Erweiterung ("ipaddr")</span><span class="sxs-lookup"><span data-stu-id="69f24-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="69f24-117">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="69f24-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="69f24-118">dport</span><span class="sxs-lookup"><span data-stu-id="69f24-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69f24-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="69f24-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="69f24-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69f24-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69f24-121">Qualifizierer: wmidataid (5), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="69f24-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="69f24-122">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="69f24-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="69f24-123">PID</span><span class="sxs-lookup"><span data-stu-id="69f24-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69f24-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69f24-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69f24-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69f24-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69f24-126">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="69f24-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="69f24-127">Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="69f24-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="69f24-128">saddr</span><span class="sxs-lookup"><span data-stu-id="69f24-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69f24-129">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="69f24-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="69f24-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69f24-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69f24-131">Qualifizierer: wmidataid (4), Erweiterung ("ipaddr")</span><span class="sxs-lookup"><span data-stu-id="69f24-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="69f24-132">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="69f24-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="69f24-133">size</span><span class="sxs-lookup"><span data-stu-id="69f24-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69f24-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69f24-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69f24-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69f24-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69f24-136">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="69f24-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="69f24-137">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="69f24-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="69f24-138">Reit</span><span class="sxs-lookup"><span data-stu-id="69f24-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69f24-139">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="69f24-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="69f24-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69f24-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69f24-141">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="69f24-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="69f24-142">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="69f24-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69f24-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="69f24-143">Requirements</span></span>



| <span data-ttu-id="69f24-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69f24-144">Requirement</span></span> | <span data-ttu-id="69f24-145">Wert</span><span class="sxs-lookup"><span data-stu-id="69f24-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69f24-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69f24-146">Minimum supported client</span></span><br/> | <span data-ttu-id="69f24-147">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69f24-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="69f24-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69f24-148">Minimum supported server</span></span><br/> | <span data-ttu-id="69f24-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69f24-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69f24-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="69f24-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f24-151">**Tcpip \_ v1**</span><span class="sxs-lookup"><span data-stu-id="69f24-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




