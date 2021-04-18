---
description: Beschreibt die Modi der sicheren Modi für ein Windows-Gerät.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: WLDP_WINDOWS_LOCKDOWN_MODE-Enumeration (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361466"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a><span data-ttu-id="7d82f-103">Wldp \_ Windows \_ Lockdown \_ Mode-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7d82f-103">WLDP\_WINDOWS\_LOCKDOWN\_MODE enumeration</span></span>

<span data-ttu-id="7d82f-104">Beschreibt die Modi der sicheren Modi für ein Windows-Gerät.</span><span class="sxs-lookup"><span data-stu-id="7d82f-104">Describes the secure modes (S modes) for a Windows device.</span></span> <span data-ttu-id="7d82f-105">Wird hauptsächlich in [**wldpquerywindowslockdownmode**](wldpquerywindowslockdownmode.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d82f-105">Used primarily in [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d82f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d82f-106">Syntax</span></span>


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a><span data-ttu-id="7d82f-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7d82f-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7d82f-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**wldp- \_ Windows- \_ \_ \_ Sperrmodus gesperrt**</span><span class="sxs-lookup"><span data-stu-id="7d82f-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_UNLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="7d82f-109">Geschaltet.</span><span class="sxs-lookup"><span data-stu-id="7d82f-109">Unlocked.</span></span> <span data-ttu-id="7d82f-110">Wird hauptsächlich für Windows-Geräte ohne den S-Modus verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d82f-110">Used primarily for Windows devices without the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="7d82f-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**wldp- \_ Windows- \_ Sperrmodus- \_ \_ Testversion**</span><span class="sxs-lookup"><span data-stu-id="7d82f-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_TRIAL**</span></span>
</dt> <dd>

<span data-ttu-id="7d82f-112">Versuchten.</span><span class="sxs-lookup"><span data-stu-id="7d82f-112">Trial.</span></span> <span data-ttu-id="7d82f-113">Wird hauptsächlich für ein Windows 10-Testgerät mit dem S-Modus verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d82f-113">Used primarily for a Windows 10 trial device with the S mode.</span></span> <span data-ttu-id="7d82f-114">Der Test Modus ist ein Sonderfall für Windows 10-Geräte mit dem S-Modus: Richtlinien werden erzwungen, aber es gibt keinen Schutz vor der Durchsetzung der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="7d82f-114">Trial mode is a special case for Windows 10 devices with the S mode: policies are enforced, but there is no anti-rollback protection for the enforcement of the policy.</span></span>

</dd> <dt>

<span data-ttu-id="7d82f-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**wldp- \_ Windows- \_ \_ \_ Sperrmodus gesperrt**</span><span class="sxs-lookup"><span data-stu-id="7d82f-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_LOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="7d82f-116">Ene.</span><span class="sxs-lookup"><span data-stu-id="7d82f-116">Locked.</span></span> <span data-ttu-id="7d82f-117">Wird hauptsächlich für ein Windows 10-Gerät mit dem S-Modus verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d82f-117">Used primarily for a Windows 10 device with the S mode.</span></span> <span data-ttu-id="7d82f-118">Ein gesperrtes Gerät erzwingt die signierten Device Guard-Richtlinien, die mit dem Windows 10-Betriebssystem Image im S-Modus ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="7d82f-118">A device that is locked will enforce the signed Device Guard policies shipped with the Windows 10 OS image with the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="7d82f-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**wldp- \_ Windows- \_ \_ Sperrmodus ( \_ max)**</span><span class="sxs-lookup"><span data-stu-id="7d82f-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="7d82f-120">Der maximale Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="7d82f-120">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d82f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d82f-121">Requirements</span></span>



| <span data-ttu-id="7d82f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d82f-122">Requirement</span></span> | <span data-ttu-id="7d82f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7d82f-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7d82f-124">Header</span><span class="sxs-lookup"><span data-stu-id="7d82f-124">Header</span></span><br/> | <dl> <span data-ttu-id="7d82f-125"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d82f-125"><dt>Wldp.h</dt></span></span> </dl> |



 

 




