---
description: 'TcpIp_Fail Klasse: Diese Klasse ist die Ereignistypklasse für TCP/IP-Fehlerereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: TcpIp_Fail-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 897c42a1c2530d3e41d1f937d5d59356a2913e2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105848"
---
# <a name="tcpip_fail-class"></a><span data-ttu-id="9e664-104">TcpIp \_ Fail-Klasse</span><span class="sxs-lookup"><span data-stu-id="9e664-104">TcpIp\_Fail class</span></span>

<span data-ttu-id="9e664-105">Diese Klasse ist die Ereignistypklasse für TCP/IP-Fehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="9e664-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="9e664-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9e664-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e664-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e664-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="9e664-108">Member</span><span class="sxs-lookup"><span data-stu-id="9e664-108">Members</span></span>

<span data-ttu-id="9e664-109">Die **TcpIp \_ Fail-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="9e664-109">The **TcpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="9e664-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e664-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e664-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e664-111">Properties</span></span>

<span data-ttu-id="9e664-112">Die **TcpIp \_ Fail-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9e664-112">The **TcpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e664-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="9e664-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e664-114">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="9e664-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e664-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e664-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e664-116">Die Ursache für den Fehler.</span><span class="sxs-lookup"><span data-stu-id="9e664-116">Reason for the failure.</span></span> <span data-ttu-id="9e664-117">Kann einer der folgenden Codes sein:</span><span class="sxs-lookup"><span data-stu-id="9e664-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="9e664-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**FEHLER \_ UNZUREICHENDE \_ RESSOURCEN** (1)</span><span class="sxs-lookup"><span data-stu-id="9e664-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9e664-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**FEHLER \_ ZU \_ VIELE \_ ADRESSEN** (2)</span><span class="sxs-lookup"><span data-stu-id="9e664-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9e664-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**FEHLER \_ ADDRESS \_ EXISTS** (3)</span><span class="sxs-lookup"><span data-stu-id="9e664-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9e664-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**FEHLER \_ UNGÜLTIGE \_ ADRESSE** (4)</span><span class="sxs-lookup"><span data-stu-id="9e664-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9e664-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**FEHLER \_ OTHER** (5)</span><span class="sxs-lookup"><span data-stu-id="9e664-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9e664-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**FEHLER \_ TIMEWAIT \_ ADDRESS \_ EXIST** (6)</span><span class="sxs-lookup"><span data-stu-id="9e664-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9e664-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="9e664-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e664-125">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="9e664-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e664-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e664-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e664-127">Identifiziert das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="9e664-127">Identifies the protocol.</span></span> <span data-ttu-id="9e664-128">Folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="9e664-128">Can be one of the following values:</span></span>



| <span data-ttu-id="9e664-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9e664-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="9e664-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9e664-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="9e664-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9e664-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="9e664-132">Die IPv4-Adressfamilie (Internetprotokoll, Version 4).</span><span class="sxs-lookup"><span data-stu-id="9e664-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="9e664-133"><dt>**AF \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="9e664-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="9e664-134">Die IPv6-Adressfamilie (Internet Protocol Version 6).</span><span class="sxs-lookup"><span data-stu-id="9e664-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e664-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e664-135">Requirements</span></span>



| <span data-ttu-id="9e664-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e664-136">Requirement</span></span> | <span data-ttu-id="9e664-137">Wert</span><span class="sxs-lookup"><span data-stu-id="9e664-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e664-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e664-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9e664-139">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e664-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e664-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e664-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9e664-141">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e664-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e664-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9e664-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e664-143">**Tcpip**</span><span class="sxs-lookup"><span data-stu-id="9e664-143">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




