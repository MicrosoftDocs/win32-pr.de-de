---
description: 'TcpIp_V1_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für TCP/IP-Ereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
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
ms.openlocfilehash: 831dfdc228e2c8e128f328784046e833b0b45a39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105758"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="f44b9-104">TcpIp \_ V1 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="f44b9-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="f44b9-105">Diese Klasse ist die Ereignistypklasse für TCP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f44b9-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="f44b9-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f44b9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f44b9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f44b9-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f44b9-108">Member</span><span class="sxs-lookup"><span data-stu-id="f44b9-108">Members</span></span>

<span data-ttu-id="f44b9-109">Die **Klasse TcpIp \_ V1 \_ TypeGroup1** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="f44b9-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f44b9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f44b9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f44b9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f44b9-111">Properties</span></span>

<span data-ttu-id="f44b9-112">Die **Klasse TcpIp \_ V1 \_ TypeGroup1** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f44b9-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f44b9-113">daddr</span><span class="sxs-lookup"><span data-stu-id="f44b9-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f44b9-114">Datentyp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="f44b9-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f44b9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-116">Qualifizierer: WmiDataId(3), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="f44b9-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="f44b9-117">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f44b9-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f44b9-118">dport</span><span class="sxs-lookup"><span data-stu-id="f44b9-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f44b9-119">Datentyp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="f44b9-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f44b9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-121">Qualifizierer: WmiDataId(5), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="f44b9-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f44b9-122">Zielportnummer.</span><span class="sxs-lookup"><span data-stu-id="f44b9-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="f44b9-123">PID</span><span class="sxs-lookup"><span data-stu-id="f44b9-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f44b9-124">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f44b9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f44b9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-126">Qualifizierer: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="f44b9-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f44b9-127">Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f44b9-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="f44b9-128">saddr</span><span class="sxs-lookup"><span data-stu-id="f44b9-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f44b9-129">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="f44b9-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f44b9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-131">Qualifizierer: WmiDataId(4), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="f44b9-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="f44b9-132">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f44b9-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f44b9-133">Größe</span><span class="sxs-lookup"><span data-stu-id="f44b9-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f44b9-134">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f44b9-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f44b9-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-136">Qualifizierer: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="f44b9-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f44b9-137">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="f44b9-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="f44b9-138">Sport</span><span class="sxs-lookup"><span data-stu-id="f44b9-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f44b9-139">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="f44b9-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f44b9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f44b9-141">Qualifizierer: WmiDataId(6), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="f44b9-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f44b9-142">Quellportnummer.</span><span class="sxs-lookup"><span data-stu-id="f44b9-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f44b9-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f44b9-143">Requirements</span></span>



| <span data-ttu-id="f44b9-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f44b9-144">Requirement</span></span> | <span data-ttu-id="f44b9-145">Wert</span><span class="sxs-lookup"><span data-stu-id="f44b9-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f44b9-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f44b9-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f44b9-147">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f44b9-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f44b9-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f44b9-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f44b9-149">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f44b9-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f44b9-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f44b9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44b9-151">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f44b9-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




