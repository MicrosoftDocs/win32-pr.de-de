---
description: Diese Klasse ist die Ereignistyp Klasse für UDP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: UdpIp_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2813476bc2c820d1872e787dc047fafccd3b7d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960359"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="a5a42-104">Udpip \_ v0 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="a5a42-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="a5a42-105">Diese Klasse ist die Ereignistyp Klasse für UDP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="a5a42-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="a5a42-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="a5a42-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a42-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5a42-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a><span data-ttu-id="a5a42-108">Member</span><span class="sxs-lookup"><span data-stu-id="a5a42-108">Members</span></span>

<span data-ttu-id="a5a42-109">Die **udpip \_ v0 \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a5a42-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a5a42-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5a42-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5a42-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5a42-111">Properties</span></span>

<span data-ttu-id="a5a42-112">Die **udpip \_ v0 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a5a42-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5a42-113">context</span><span class="sxs-lookup"><span data-stu-id="a5a42-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a42-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5a42-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5a42-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-116">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="a5a42-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="a5a42-117">Prozess Bezeichner für das Adress Objekt, von dem die Anforderung stammt oder empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a5a42-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="a5a42-118">daddr</span><span class="sxs-lookup"><span data-stu-id="a5a42-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a42-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="a5a42-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5a42-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-121">Qualifizierer: wmidataid (5), Erweiterung ("ipaddr")</span><span class="sxs-lookup"><span data-stu-id="a5a42-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="a5a42-122">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a5a42-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a5a42-123">dport</span><span class="sxs-lookup"><span data-stu-id="a5a42-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a42-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="a5a42-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5a42-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-126">Qualifizierer: wmidataid (6), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="a5a42-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a5a42-127">Die Ziel Portnummer.</span><span class="sxs-lookup"><span data-stu-id="a5a42-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="a5a42-128">dsize</span><span class="sxs-lookup"><span data-stu-id="a5a42-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a42-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5a42-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5a42-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-131">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="a5a42-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="a5a42-132">Größe des Ziel Pakets.</span><span class="sxs-lookup"><span data-stu-id="a5a42-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="a5a42-133">saddr</span><span class="sxs-lookup"><span data-stu-id="a5a42-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a42-134">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="a5a42-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5a42-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-136">Qualifizierer: wmidataid (2), Erweiterung ("ipaddr")</span><span class="sxs-lookup"><span data-stu-id="a5a42-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="a5a42-137">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a5a42-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a5a42-138">size</span><span class="sxs-lookup"><span data-stu-id="a5a42-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a42-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5a42-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5a42-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-141">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="a5a42-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a5a42-142">Größe des Quellpakets.</span><span class="sxs-lookup"><span data-stu-id="a5a42-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="a5a42-143">Reit</span><span class="sxs-lookup"><span data-stu-id="a5a42-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a42-144">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="a5a42-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5a42-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a42-146">Qualifizierer: wmidataid (3), Erweiterung ("Port")</span><span class="sxs-lookup"><span data-stu-id="a5a42-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a5a42-147">Quell Portnummer.</span><span class="sxs-lookup"><span data-stu-id="a5a42-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5a42-148">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a5a42-148">Requirements</span></span>



| <span data-ttu-id="a5a42-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5a42-149">Requirement</span></span> | <span data-ttu-id="a5a42-150">Wert</span><span class="sxs-lookup"><span data-stu-id="a5a42-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="a5a42-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5a42-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a5a42-152">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5a42-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a5a42-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5a42-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a5a42-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a5a42-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="a5a42-155">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a5a42-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a42-156">**Udpip \_ v0**</span><span class="sxs-lookup"><span data-stu-id="a5a42-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




