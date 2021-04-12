---
description: Enthält Informationen über einen Prozessor.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: PROCESSOR_POWER_INFORMATION Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345488"
---
# <a name="processor_power_information-structure"></a><span data-ttu-id="f70bc-103">Struktur der Prozessor \_ Energie \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="f70bc-103">PROCESSOR\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="f70bc-104">Enthält Informationen über einen Prozessor.</span><span class="sxs-lookup"><span data-stu-id="f70bc-104">Contains information about a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f70bc-105">Syntax</span></span>


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="f70bc-106">Member</span><span class="sxs-lookup"><span data-stu-id="f70bc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f70bc-107">**Number**</span><span class="sxs-lookup"><span data-stu-id="f70bc-107">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="f70bc-108">Die System Prozessornummer.</span><span class="sxs-lookup"><span data-stu-id="f70bc-108">The system processor number.</span></span>

</dd> <dt>

<span data-ttu-id="f70bc-109">**Maxmhz**</span><span class="sxs-lookup"><span data-stu-id="f70bc-109">**MaxMhz**</span></span>
</dt> <dd>

<span data-ttu-id="f70bc-110">Die maximale angegebene Taktfrequenz des System Prozessors in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="f70bc-110">The maximum specified clock frequency of the system processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="f70bc-111">**Currentmhz**</span><span class="sxs-lookup"><span data-stu-id="f70bc-111">**CurrentMhz**</span></span>
</dt> <dd>

<span data-ttu-id="f70bc-112">Die Prozessor Taktfrequenz in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="f70bc-112">The processor clock frequency, in megahertz.</span></span> <span data-ttu-id="f70bc-113">Diese Zahl entspricht der maximalen angegebenen Prozessor Taktfrequenz, multipliziert mit der aktuellen Prozessor Drosselung.</span><span class="sxs-lookup"><span data-stu-id="f70bc-113">This number is the maximum specified processor clock frequency multiplied by the current processor throttle.</span></span>

</dd> <dt>

<span data-ttu-id="f70bc-114">**Mhzlimit**</span><span class="sxs-lookup"><span data-stu-id="f70bc-114">**MhzLimit**</span></span>
</dt> <dd>

<span data-ttu-id="f70bc-115">Der Grenzwert für die Prozessor Taktfrequenz in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="f70bc-115">The limit on the processor clock frequency, in megahertz.</span></span> <span data-ttu-id="f70bc-116">Diese Zahl entspricht der maximalen angegebenen Prozessor Taktfrequenz, multipliziert mit der aktuellen Prozessor-Grenzwert für die wärmedrosselung.</span><span class="sxs-lookup"><span data-stu-id="f70bc-116">This number is the maximum specified processor clock frequency multiplied by the current processor thermal throttle limit.</span></span>

</dd> <dt>

<span data-ttu-id="f70bc-117">**Maxidlestate**</span><span class="sxs-lookup"><span data-stu-id="f70bc-117">**MaxIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="f70bc-118">Der maximale Leerlauf Status dieses Prozessors.</span><span class="sxs-lookup"><span data-stu-id="f70bc-118">The maximum idle state of this processor.</span></span>

</dd> <dt>

<span data-ttu-id="f70bc-119">**"Ustidlestate"**</span><span class="sxs-lookup"><span data-stu-id="f70bc-119">**CurrentIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="f70bc-120">Der aktuelle Leerlauf Status dieses Prozessors.</span><span class="sxs-lookup"><span data-stu-id="f70bc-120">The current idle state of this processor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f70bc-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f70bc-121">Remarks</span></span>

<span data-ttu-id="f70bc-122">Beachten Sie, dass diese Struktur Definition versehentlich aus "Winnt. h" weggelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="f70bc-122">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="f70bc-123">Dieser Fehler wird in Zukunft korrigiert.</span><span class="sxs-lookup"><span data-stu-id="f70bc-123">This error will be corrected in the future.</span></span> <span data-ttu-id="f70bc-124">Fügen Sie in der Zwischenzeit die Struktur Definition, die in diesem Thema enthalten ist, in Ihren Quellcode ein, um die Anwendung zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="f70bc-124">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70bc-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f70bc-125">Requirements</span></span>



| <span data-ttu-id="f70bc-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f70bc-126">Requirement</span></span> | <span data-ttu-id="f70bc-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f70bc-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f70bc-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f70bc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f70bc-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f70bc-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f70bc-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f70bc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f70bc-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f70bc-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f70bc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f70bc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70bc-133">**Callntpowerinformation**</span><span class="sxs-lookup"><span data-stu-id="f70bc-133">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




