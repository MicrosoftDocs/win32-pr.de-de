---
description: 'UdpIp_Fail Klasse: Diese Klasse ist die Ereignistypklasse für TCP/IP-Fehlerereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: UdpIp_Fail-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_Fail
- UdpIp_Fail.Proto
- UdpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: f923f26e1371d11e27bfd58bcb69c053bfb5f1a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105508"
---
# <a name="udpip_fail-class"></a><span data-ttu-id="16958-104">UdpIp \_ Fail-Klasse</span><span class="sxs-lookup"><span data-stu-id="16958-104">UdpIp\_Fail class</span></span>

<span data-ttu-id="16958-105">Diese Klasse ist die Ereignistypklasse für TCP/IP-Fehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="16958-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="16958-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="16958-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="16958-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="16958-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class UdpIp_Fail : UdpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="16958-108">Member</span><span class="sxs-lookup"><span data-stu-id="16958-108">Members</span></span>

<span data-ttu-id="16958-109">Die **UdpIp \_ Fail-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="16958-109">The **UdpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="16958-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16958-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16958-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16958-111">Properties</span></span>

<span data-ttu-id="16958-112">Die **UdpIp \_ Fail-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="16958-112">The **UdpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16958-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="16958-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16958-114">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="16958-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16958-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16958-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16958-116">Die Ursache für den Fehler.</span><span class="sxs-lookup"><span data-stu-id="16958-116">Reason for the failure.</span></span> <span data-ttu-id="16958-117">Kann einer der folgenden Codes sein:</span><span class="sxs-lookup"><span data-stu-id="16958-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="16958-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**FEHLER \_ UNZUREICHENDE \_ RESSOURCEN** (1)</span><span class="sxs-lookup"><span data-stu-id="16958-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="16958-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**FEHLER \_ ZU \_ VIELE \_ ADRESSEN** (2)</span><span class="sxs-lookup"><span data-stu-id="16958-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="16958-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**FEHLER \_ ADDRESS \_ EXISTS** (3)</span><span class="sxs-lookup"><span data-stu-id="16958-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="16958-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**FEHLER \_ UNGÜLTIGE \_ ADRESSE** (4)</span><span class="sxs-lookup"><span data-stu-id="16958-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="16958-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**FEHLER \_ OTHER** (5)</span><span class="sxs-lookup"><span data-stu-id="16958-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="16958-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**FEHLER \_ TIMEWAIT \_ ADDRESS \_ EXIST** (6)</span><span class="sxs-lookup"><span data-stu-id="16958-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="16958-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="16958-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16958-125">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="16958-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16958-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16958-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16958-127">Identifiziert das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="16958-127">Identifies the protocol.</span></span> <span data-ttu-id="16958-128">Folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="16958-128">Can be one of the following values:</span></span>



| <span data-ttu-id="16958-129">Wert</span><span class="sxs-lookup"><span data-stu-id="16958-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="16958-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="16958-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="16958-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="16958-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="16958-132">Die IPv4-Adressfamilie (Internetprotokoll, Version 4).</span><span class="sxs-lookup"><span data-stu-id="16958-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="16958-133"><dt>**AF \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="16958-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="16958-134">Die IPv6-Adressfamilie (Internet Protocol Version 6).</span><span class="sxs-lookup"><span data-stu-id="16958-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16958-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16958-135">Requirements</span></span>



| <span data-ttu-id="16958-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16958-136">Requirement</span></span> | <span data-ttu-id="16958-137">Wert</span><span class="sxs-lookup"><span data-stu-id="16958-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16958-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16958-138">Minimum supported client</span></span><br/> | <span data-ttu-id="16958-139">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16958-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="16958-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16958-140">Minimum supported server</span></span><br/> | <span data-ttu-id="16958-141">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16958-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16958-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="16958-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16958-143">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="16958-143">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




