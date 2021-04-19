---
description: In der folgenden Liste werden die Entlade Richtlinien Konstanten beschrieben.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Entlade Richtlinien Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349856"
---
# <a name="discharge-policy-constants"></a><span data-ttu-id="1fe27-103">Entlade Richtlinien Konstanten</span><span class="sxs-lookup"><span data-stu-id="1fe27-103">Discharge Policy Constants</span></span>

<span data-ttu-id="1fe27-104">In der folgenden Liste werden die Entlade Richtlinien Konstanten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1fe27-104">The following list describes the discharge policy constants.</span></span>



| <span data-ttu-id="1fe27-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="1fe27-105">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="1fe27-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fe27-106">Description</span></span>                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <span data-ttu-id="1fe27-107"><dt>**Entladen \_ Richtlinien \_ kritisch**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1fe27-107"><dt>**DISCHARGE\_POLICY\_CRITICAL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="1fe27-108">Welche der Einstellungen für die Akku Entlade Richtlinie [**( \_ Systemenergie \_ Pegel**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) -Strukturen) wird verwendet, wenn die Akkukapazität unter den kritischen Schwellenwert fällt.</span><span class="sxs-lookup"><span data-stu-id="1fe27-108">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the critical threshold.</span></span><br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <span data-ttu-id="1fe27-109"><dt>**Entladen \_ Richtlinie \_ niedrig**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1fe27-109"><dt>**DISCHARGE\_POLICY\_LOW**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="1fe27-110">Welche der Einstellungen für die Akku Entlade Richtlinie [**( \_ Systemenergie \_ Pegel**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) -Strukturen) wird verwendet, wenn der Akku unter den unteren Schwellenwert entladen wird.</span><span class="sxs-lookup"><span data-stu-id="1fe27-110">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the low threshold.</span></span><br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <span data-ttu-id="1fe27-111"><dt>**NUM \_ Entlade \_ Richtlinien**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1fe27-111"><dt>**NUM\_DISCHARGE\_POLICIES**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="1fe27-112">Anzahl der Einstellungen für die Akku Entlade Richtlinie ([**\_ \_ systemstromseenstrukturen**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ).</span><span class="sxs-lookup"><span data-stu-id="1fe27-112">Number of battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) specified.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="1fe27-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fe27-113">Requirements</span></span>



| <span data-ttu-id="1fe27-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fe27-114">Requirement</span></span> | <span data-ttu-id="1fe27-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe27-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe27-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fe27-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe27-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fe27-117">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1fe27-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fe27-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe27-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fe27-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1fe27-120">Header</span><span class="sxs-lookup"><span data-stu-id="1fe27-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fe27-121"><dt>WinNT. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fe27-121"><dt>WinNT.h (include Windows.h)</dt></span></span> </dl> |



 

 




