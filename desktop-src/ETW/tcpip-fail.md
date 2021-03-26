---
description: Diese Klasse ist die Ereignistyp Klasse für TCP/IP-Fehlerereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: a89d882509ea766e62c8b78e6c2a5fa769fbcca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978272"
---
# <a name="tcpip_fail-class"></a><span data-ttu-id="de684-104">Tcpip-Fehler \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="de684-104">TcpIp\_Fail class</span></span>

<span data-ttu-id="de684-105">Diese Klasse ist die Ereignistyp Klasse für TCP/IP-Fehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="de684-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="de684-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="de684-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="de684-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="de684-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="de684-108">Member</span><span class="sxs-lookup"><span data-stu-id="de684-108">Members</span></span>

<span data-ttu-id="de684-109">Die **tcpip \_ Fail** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="de684-109">The **TcpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="de684-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de684-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de684-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de684-111">Properties</span></span>

<span data-ttu-id="de684-112">Die **tcpip \_ Fail** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="de684-112">The **TcpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de684-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="de684-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de684-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="de684-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de684-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de684-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de684-116">Die Ursache für den Fehler.</span><span class="sxs-lookup"><span data-stu-id="de684-116">Reason for the failure.</span></span> <span data-ttu-id="de684-117">Kann einen der folgenden Codes aufweisen:</span><span class="sxs-lookup"><span data-stu-id="de684-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="de684-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Fehler \_ Unzureichende \_ Ressourcen** (1)</span><span class="sxs-lookup"><span data-stu-id="de684-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="de684-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Fehler \_ Zu \_ viele \_ Adressen** (2)</span><span class="sxs-lookup"><span data-stu-id="de684-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="de684-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Fehler \_ Adresse ist \_ vorhanden** (3)</span><span class="sxs-lookup"><span data-stu-id="de684-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="de684-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Fehler \_ Ungültige \_ Adresse** (4)</span><span class="sxs-lookup"><span data-stu-id="de684-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="de684-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**Fehler \_ Sonstige** (5)</span><span class="sxs-lookup"><span data-stu-id="de684-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="de684-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Fehler \_ Timewait- \_ Adresse ist \_ vorhanden** (6)</span><span class="sxs-lookup"><span data-stu-id="de684-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de684-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="de684-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de684-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="de684-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de684-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de684-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de684-127">Identifiziert das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="de684-127">Identifies the protocol.</span></span> <span data-ttu-id="de684-128">Folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="de684-128">Can be one of the following values:</span></span>



| <span data-ttu-id="de684-129">Wert</span><span class="sxs-lookup"><span data-stu-id="de684-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="de684-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="de684-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="de684-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="de684-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="de684-132">Die IPv4-Adressfamilie (Internet Protokollversion 4).</span><span class="sxs-lookup"><span data-stu-id="de684-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="de684-133"><dt>**AF \_ Inet6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="de684-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="de684-134">Die IPv6-Adressfamilie (Internet Protokollversion 6).</span><span class="sxs-lookup"><span data-stu-id="de684-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de684-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="de684-135">Requirements</span></span>



| <span data-ttu-id="de684-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de684-136">Requirement</span></span> | <span data-ttu-id="de684-137">Wert</span><span class="sxs-lookup"><span data-stu-id="de684-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de684-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de684-138">Minimum supported client</span></span><br/> | <span data-ttu-id="de684-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de684-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de684-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de684-140">Minimum supported server</span></span><br/> | <span data-ttu-id="de684-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de684-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de684-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="de684-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de684-143">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="de684-143">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




