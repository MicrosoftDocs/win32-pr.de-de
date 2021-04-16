---
description: Die networkstatus-Struktur beschreibt den aktuellen Status des NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Networkstatus-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530227"
---
# <a name="networkstatus-structure"></a><span data-ttu-id="8528e-103">Networkstatus-Struktur</span><span class="sxs-lookup"><span data-stu-id="8528e-103">NETWORKSTATUS structure</span></span>

<span data-ttu-id="8528e-104">Die **networkstatus** -Struktur beschreibt den aktuellen Status des NPP.</span><span class="sxs-lookup"><span data-stu-id="8528e-104">The **NETWORKSTATUS** structure describes the current status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="8528e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8528e-105">Syntax</span></span>


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a><span data-ttu-id="8528e-106">Member</span><span class="sxs-lookup"><span data-stu-id="8528e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8528e-107">**State**</span><span class="sxs-lookup"><span data-stu-id="8528e-107">**State**</span></span>
</dt> <dd>

<span data-ttu-id="8528e-108">Gibt den aktuellen Zustand des NPP an.</span><span class="sxs-lookup"><span data-stu-id="8528e-108">Indicates the current state of the NPP.</span></span>



| <span data-ttu-id="8528e-109">Wert</span><span class="sxs-lookup"><span data-stu-id="8528e-109">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="8528e-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8528e-110">Meaning</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <span data-ttu-id="8528e-111"><dt>**networkstatus- \_ Zustand ist \_ ungültig.**</dt></span><span class="sxs-lookup"><span data-stu-id="8528e-111"><dt>**NETWORKSTATUS\_STATE\_VOID**</dt></span></span> </dl>                | <span data-ttu-id="8528e-112">Der npp ist nicht verbunden, oder er ist verbunden, und die Erfassung wird nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="8528e-112">The NPP is not connected, or it is connected and the capture is not started.</span></span><br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <span data-ttu-id="8528e-113"><dt>**networkstatus- \_ Zustands \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="8528e-113"><dt>**NETWORKSTATUS\_STATE\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="8528e-114">Der NPP erfasst Daten.</span><span class="sxs-lookup"><span data-stu-id="8528e-114">The NPP is capturing data.</span></span><br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <span data-ttu-id="8528e-115"><dt>**der networkstatus-Zustand wurde angehalten. \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8528e-115"><dt>**NETWORKSTATUS\_STATE\_PAUSED**</dt></span></span> </dl>          | <span data-ttu-id="8528e-116">Der NPP wurde während der Datenerfassung angehalten.</span><span class="sxs-lookup"><span data-stu-id="8528e-116">The NPP has paused while capturing data.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="8528e-117">**Flags**</span><span class="sxs-lookup"><span data-stu-id="8528e-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="8528e-118">Flags, die den aktuellen Zustand des NPP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8528e-118">Flags that describe the current state of the NPP.</span></span>



| <span data-ttu-id="8528e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8528e-119">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="8528e-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8528e-120">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <span data-ttu-id="8528e-121"><dt>**netzwerkstatusflags-Auslösung \_ \_ \_ Ausstehend**</dt></span><span class="sxs-lookup"><span data-stu-id="8528e-121"><dt>**NETWORKSTATUS\_FLAGS\_TRIGGER\_PENDING**</dt></span></span> </dl> | <span data-ttu-id="8528e-122">Für den npp ist ein ausstehender Auslösung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8528e-122">There is a trigger pending for the NPP.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8528e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8528e-123">Remarks</span></span>

<span data-ttu-id="8528e-124">Wenn Sie diese Struktur verwenden, müssen Sie den Arbeitsspeicher für die Struktur zuordnen, bevor Sie verwendet werden kann, und den Arbeitsspeicher freigeben, wenn die Struktur nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="8528e-124">When using this structure, you must allocate the memory for the structure before it can be used and free the memory when the structure is no longer needed.</span></span>

<span data-ttu-id="8528e-125">Die Liste "Siehe auch" am Ende dieses Themas listet alle Methoden auf, die diese Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="8528e-125">The See Also list at the bottom of this topic lists all the methods that use this structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8528e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8528e-126">Requirements</span></span>



| <span data-ttu-id="8528e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8528e-127">Requirement</span></span> | <span data-ttu-id="8528e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8528e-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8528e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8528e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8528e-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8528e-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8528e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8528e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8528e-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8528e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8528e-133">Header</span><span class="sxs-lookup"><span data-stu-id="8528e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8528e-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8528e-134"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8528e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8528e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8528e-136">Idelta-DC:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="8528e-136">IDelaydC::QueryStatus</span></span>](idelaydc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="8528e-137">IESP:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="8528e-137">IESP::QueryStatus</span></span>](iesp-querystatus.md)
</dt> <dt>

[<span data-ttu-id="8528e-138">"Iran:: QueryStatus"</span><span class="sxs-lookup"><span data-stu-id="8528e-138">IRTC::QueryStatus</span></span>](irtc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="8528e-139">IStats:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="8528e-139">IStats::QueryStatus</span></span>](istats-querystatus.md)
</dt> </dl>

 

 




