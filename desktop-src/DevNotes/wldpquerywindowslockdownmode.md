---
description: Ruft den aktuellen sicheren Windows-Modus ab. Fenster können sich im gesperrten Modus befinden, nicht im normalen Modus oder im Testmodus.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Wldpquerywindowslockdownmode-Funktion (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214242"
---
# <a name="wldpquerywindowslockdownmode-function"></a><span data-ttu-id="43591-104">Wldpquerywindowslockdownmode-Funktion</span><span class="sxs-lookup"><span data-stu-id="43591-104">WldpQueryWindowsLockdownMode function</span></span>

<span data-ttu-id="43591-105">Ruft den aktuellen sicheren Windows-Modus ab.</span><span class="sxs-lookup"><span data-stu-id="43591-105">Retrieves the current Windows secure mode.</span></span> <span data-ttu-id="43591-106">Fenster können sich im gesperrten Modus befinden, nicht im normalen Modus oder im Testmodus.</span><span class="sxs-lookup"><span data-stu-id="43591-106">Windows can be in locked mode, unlocked normal mode, or trial mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="43591-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="43591-107">Syntax</span></span>


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a><span data-ttu-id="43591-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43591-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43591-109">*lockdownmode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43591-109">*lockdownMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43591-110">Bei Erfolg wird der [**Modus "pwldp \_ Windows \_ Lockdown \_**](wldp-windows-lockdown-mode.md) " zurückgegeben, der den sicheren Modus für das aktuelle Windows 10-Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="43591-110">On success, returns a [**PWLDP\_WINDOWS\_LOCKDOWN\_MODE**](wldp-windows-lockdown-mode.md) that indicates the secure mode for the current Windows 10 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43591-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43591-111">Return value</span></span>

<span data-ttu-id="43591-112">Diese Methode gibt bei Erfolg **S \_ OK** zurück oder andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="43591-112">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="43591-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43591-113">Requirements</span></span>



| <span data-ttu-id="43591-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43591-114">Requirement</span></span> | <span data-ttu-id="43591-115">Wert</span><span class="sxs-lookup"><span data-stu-id="43591-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="43591-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43591-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43591-117">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43591-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="43591-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43591-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43591-119">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43591-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="43591-120">Header</span><span class="sxs-lookup"><span data-stu-id="43591-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="43591-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="43591-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="43591-122">DLL</span><span class="sxs-lookup"><span data-stu-id="43591-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43591-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43591-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




