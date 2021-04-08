---
description: Enthält Informationen über die idständigkeit des Systems.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: SYSTEM_POWER_INFORMATION Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959734"
---
# <a name="system_power_information-structure"></a><span data-ttu-id="05e6b-103">Struktur der System \_ Energie \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="05e6b-103">SYSTEM\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="05e6b-104">Enthält Informationen über die idständigkeit des Systems.</span><span class="sxs-lookup"><span data-stu-id="05e6b-104">Contains information about the idleness of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="05e6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05e6b-105">Syntax</span></span>


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="05e6b-106">Member</span><span class="sxs-lookup"><span data-stu-id="05e6b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="05e6b-107">**Maxidleness Allowed**</span><span class="sxs-lookup"><span data-stu-id="05e6b-107">**MaxIdlenessAllowed**</span></span>
</dt> <dd>

<span data-ttu-id="05e6b-108">Der Leerlauf, bei dem das System als im Leerlauf befindlich betrachtet wird und das Leerlauf Timeout beginnt, wird als Prozentsatz ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="05e6b-108">The idleness at which the system is considered idle and the idle time-out begins counting, expressed as a percentage.</span></span> <span data-ttu-id="05e6b-109">Das Ablegen unterhalb dieser Zahl bewirkt, dass der Timer abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="05e6b-109">Dropping below this number causes the timer to be canceled.</span></span>

</dd> <dt>

<span data-ttu-id="05e6b-110">**Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="05e6b-110">**Idleness**</span></span>
</dt> <dd>

<span data-ttu-id="05e6b-111">Die aktuelle Leerlauf Ebene, ausgedrückt als Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="05e6b-111">The current idle level, expressed as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="05e6b-112">**TimeRemaining**</span><span class="sxs-lookup"><span data-stu-id="05e6b-112">**TimeRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="05e6b-113">Die verbleibende Zeit im Leerlaufzeit Geber in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="05e6b-113">The time remaining in the idle timer, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="05e6b-114">**Coolingmode**</span><span class="sxs-lookup"><span data-stu-id="05e6b-114">**CoolingMode**</span></span>
</dt> <dd>

<span data-ttu-id="05e6b-115">Der aktuelle systemkühlungs Modus.</span><span class="sxs-lookup"><span data-stu-id="05e6b-115">The current system cooling mode.</span></span> <span data-ttu-id="05e6b-116">Dieser Member muss einen der folgenden Werte haben.</span><span class="sxs-lookup"><span data-stu-id="05e6b-116">This member must one of the following values.</span></span>



| <span data-ttu-id="05e6b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="05e6b-117">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="05e6b-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="05e6b-118">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <span data-ttu-id="05e6b-119"><dt>**Po \_ TZ \_ aktiv**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05e6b-119"><dt>**PO\_TZ\_ACTIVE**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="05e6b-120">Das System befindet sich derzeit im aktiven kühl Modus.</span><span class="sxs-lookup"><span data-stu-id="05e6b-120">The system is currently in Active cooling mode.</span></span><br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <span data-ttu-id="05e6b-121"><dt>**Po \_ TZ \_ ungültiger \_ Modus**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="05e6b-121"><dt>**PO\_TZ\_INVALID\_MODE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="05e6b-122">Das System unterstützt keine CPU-Drosselung, oder im System ist keine thermische Zone definiert.</span><span class="sxs-lookup"><span data-stu-id="05e6b-122">The system does not support CPU throttling, or there is no thermal zone defined in the system.</span></span><br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <span data-ttu-id="05e6b-123"><dt>**Po \_ TZ \_ passiv**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="05e6b-123"><dt>**PO\_TZ\_PASSIVE**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="05e6b-124">Das System befindet sich zurzeit im passiven kühl Modus.</span><span class="sxs-lookup"><span data-stu-id="05e6b-124">The system is currently in Passive cooling mode.</span></span><br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05e6b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05e6b-125">Remarks</span></span>

<span data-ttu-id="05e6b-126">Beachten Sie, dass diese Struktur Definition versehentlich aus "Winnt. h" weggelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="05e6b-126">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="05e6b-127">Dieser Fehler wird in Zukunft korrigiert.</span><span class="sxs-lookup"><span data-stu-id="05e6b-127">This error will be corrected in the future.</span></span> <span data-ttu-id="05e6b-128">Fügen Sie in der Zwischenzeit die Struktur Definition, die in diesem Thema enthalten ist, in Ihren Quellcode ein, um die Anwendung zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="05e6b-128">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="05e6b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05e6b-129">Requirements</span></span>



| <span data-ttu-id="05e6b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05e6b-130">Requirement</span></span> | <span data-ttu-id="05e6b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="05e6b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05e6b-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05e6b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="05e6b-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05e6b-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="05e6b-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05e6b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="05e6b-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05e6b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05e6b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05e6b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e6b-137">**Callntpowerinformation**</span><span class="sxs-lookup"><span data-stu-id="05e6b-137">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




