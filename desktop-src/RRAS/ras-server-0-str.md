---
title: RAS_SERVER_0 Struktur (rassapi. h)
description: Die Struktur des RAS- \_ Servers \_ 0 wird von der rasadminservergetinfo-Funktion verwendet, um Informationen zu den auf einem RAS-Server konfigurierten Ports zurückzugeben.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 Struktur-RAS
- PRAS_SERVER_0-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338778"
---
# <a name="ras_server_0-structure"></a><span data-ttu-id="7839d-105">RAS- \_ Server- \_ 0-Struktur</span><span class="sxs-lookup"><span data-stu-id="7839d-105">RAS\_SERVER\_0 structure</span></span>

<span data-ttu-id="7839d-106">\[Die Struktur des **RAS- \_ Servers \_ 0** wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="7839d-106">\[The **RAS\_SERVER\_0** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="7839d-107">Die Struktur des **RAS- \_ Servers \_ 0** wird von der [**rasadminservergetinfo**](rasadminservergetinfo.md) -Funktion verwendet, um Informationen zu den auf einem RAS-Server konfigurierten Ports zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="7839d-107">The **RAS\_SERVER\_0** structure is used by the [**RasAdminServerGetInfo**](rasadminservergetinfo.md) function to return information about the ports configured on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7839d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7839d-108">Syntax</span></span>


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a><span data-ttu-id="7839d-109">Member</span><span class="sxs-lookup"><span data-stu-id="7839d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7839d-110">**Totalports**</span><span class="sxs-lookup"><span data-stu-id="7839d-110">**TotalPorts**</span></span>
</dt> <dd>

<span data-ttu-id="7839d-111">Gibt die Gesamtanzahl der auf dem RAS-Server konfigurierten Ports an, die für Remote Clients zum Herstellen einer Verbindung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7839d-111">Specifies the total number of ports configured on the RAS server that are available for remote clients to connect to.</span></span> <span data-ttu-id="7839d-112">Wenn z. b. die Gesamtanzahl der Ports, die für die Einwahl eines Servers konfiguriert sind, vier beträgt, aber einer der Ports zurzeit für das Auschecken verwendet wird, beträgt **totalports** drei.</span><span class="sxs-lookup"><span data-stu-id="7839d-112">For example, if the total number of ports configured for dialing in to a server is four, but one of the ports is currently in use for dialing out, **TotalPorts** is three.</span></span>

</dd> <dt>

<span data-ttu-id="7839d-113">**Portsinuse**</span><span class="sxs-lookup"><span data-stu-id="7839d-113">**PortsInUse**</span></span>
</dt> <dd>

<span data-ttu-id="7839d-114">Gibt die Anzahl der Ports an, die zurzeit von Remote Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7839d-114">Specifies the number of ports currently in use by remote clients.</span></span>

</dd> <dt>

<span data-ttu-id="7839d-115">**Rasversion**</span><span class="sxs-lookup"><span data-stu-id="7839d-115">**RasVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7839d-116">Gibt die Version des RAS-Servers an.</span><span class="sxs-lookup"><span data-stu-id="7839d-116">Specifies the version of the RAS server.</span></span> <span data-ttu-id="7839d-117">Verwenden Sie diese Informationen, um versionsspezifische Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7839d-117">Use this information to take version-specific action.</span></span> <span data-ttu-id="7839d-118">Dieser Member ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="7839d-118">This member is one of the following values.</span></span>



| <span data-ttu-id="7839d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7839d-119">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="7839d-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7839d-120">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <span data-ttu-id="7839d-121"><dt>**Rasdownlevel**</dt></span><span class="sxs-lookup"><span data-stu-id="7839d-121"><dt>**RASDOWNLEVEL**</dt></span></span> </dl>              | <span data-ttu-id="7839d-122">Gibt einen RAS-Server der LAN-Manager-Version 1,0 an.</span><span class="sxs-lookup"><span data-stu-id="7839d-122">Indicates a LAN Manager version 1.0 RAS server.</span></span><br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <span data-ttu-id="7839d-123"><dt>**Rasadmin \_ 35**</dt></span><span class="sxs-lookup"><span data-stu-id="7839d-123"><dt>**RASADMIN\_35**</dt></span></span> </dl>                | <span data-ttu-id="7839d-124">Gibt einen RAS-Server oder-Client für Windows NT Server 3,51 und frühere Versionen an.</span><span class="sxs-lookup"><span data-stu-id="7839d-124">Indicates a Windows NT Server 3.51 and earlier RAS server or client.</span></span><br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <span data-ttu-id="7839d-125"><dt>**rasadmin \_ aktuell**</dt></span><span class="sxs-lookup"><span data-stu-id="7839d-125"><dt>**RASADMIN\_CURRENT**</dt></span></span> </dl> | <span data-ttu-id="7839d-126">Gibt einen Windows NT 4,0-RAS-Server oder-Client an.</span><span class="sxs-lookup"><span data-stu-id="7839d-126">Indicates a Windows NT 4.0 RAS server or client.</span></span><br/>                     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7839d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7839d-127">Requirements</span></span>



| <span data-ttu-id="7839d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7839d-128">Requirement</span></span> | <span data-ttu-id="7839d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7839d-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7839d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7839d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7839d-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7839d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7839d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7839d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7839d-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7839d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7839d-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7839d-134">End of client support</span></span><br/>    | <span data-ttu-id="7839d-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7839d-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="7839d-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7839d-136">End of server support</span></span><br/>    | <span data-ttu-id="7839d-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7839d-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="7839d-138">Header</span><span class="sxs-lookup"><span data-stu-id="7839d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7839d-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7839d-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7839d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7839d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7839d-141">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="7839d-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="7839d-142">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="7839d-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="7839d-143">**Rasadminservergetinfo**</span><span class="sxs-lookup"><span data-stu-id="7839d-143">**RasAdminServerGetInfo**</span></span>](rasadminservergetinfo.md)
</dt> </dl>

 

 





