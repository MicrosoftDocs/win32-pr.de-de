---
description: 'TcpIp_V0_TypeGroup1-Klasse: Diese Klasse ist die Ereignistypklasse für TCP/IP-Ereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
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
ms.openlocfilehash: 96df2214aff9b5be6f10a1f08f6e6ea2e015c6b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105788"
---
# <a name="tcpip_v0_typegroup1-class"></a><span data-ttu-id="b1365-104">TcpIp \_ V0 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="b1365-104">TcpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="b1365-105">Diese Klasse ist die Ereignistypklasse für TCP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b1365-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="b1365-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="b1365-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1365-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1365-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b1365-108">Member</span><span class="sxs-lookup"><span data-stu-id="b1365-108">Members</span></span>

<span data-ttu-id="b1365-109">Die **TcpIp \_ V0 \_ TypeGroup1-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b1365-109">The **TcpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="b1365-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1365-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1365-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1365-111">Properties</span></span>

<span data-ttu-id="b1365-112">Die **TcpIp \_ V0 \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1365-112">The **TcpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1365-113">daddr</span><span class="sxs-lookup"><span data-stu-id="b1365-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1365-114">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="b1365-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b1365-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1365-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1365-116">Qualifizierer: WmiDataId(1), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="b1365-116">Qualifiers: WmiDataId(1), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="b1365-117">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b1365-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b1365-118">dport</span><span class="sxs-lookup"><span data-stu-id="b1365-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1365-119">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="b1365-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b1365-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1365-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1365-121">Qualifizierer: WmiDataId(3), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="b1365-121">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="b1365-122">Zielportnummer.</span><span class="sxs-lookup"><span data-stu-id="b1365-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="b1365-123">PID</span><span class="sxs-lookup"><span data-stu-id="b1365-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1365-124">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b1365-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1365-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1365-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1365-126">Qualifizierer: WmiDataId(6)</span><span class="sxs-lookup"><span data-stu-id="b1365-126">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="b1365-127">Bezeichner des Prozesses, der der Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b1365-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="b1365-128">saddr</span><span class="sxs-lookup"><span data-stu-id="b1365-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1365-129">Datentyp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="b1365-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b1365-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1365-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1365-131">Qualifizierer: WmiDataId(2), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="b1365-131">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="b1365-132">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b1365-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b1365-133">Größe</span><span class="sxs-lookup"><span data-stu-id="b1365-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1365-134">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b1365-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1365-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1365-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1365-136">Qualifizierer: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="b1365-136">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="b1365-137">Größe des Pakets.</span><span class="sxs-lookup"><span data-stu-id="b1365-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="b1365-138">Sport</span><span class="sxs-lookup"><span data-stu-id="b1365-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1365-139">Datentyp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="b1365-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b1365-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1365-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1365-141">Qualifizierer: WmiDataId(4), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="b1365-141">Qualifiers: WmiDataId(4), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="b1365-142">Quellportnummer.</span><span class="sxs-lookup"><span data-stu-id="b1365-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1365-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1365-143">Requirements</span></span>



| <span data-ttu-id="b1365-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1365-144">Requirement</span></span> | <span data-ttu-id="b1365-145">Wert</span><span class="sxs-lookup"><span data-stu-id="b1365-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="b1365-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1365-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b1365-147">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1365-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b1365-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1365-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b1365-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b1365-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="b1365-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1365-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1365-151">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="b1365-151">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> </dl>

 

 




