---
description: Die pdhvbisgoodstatus-Funktion testet einen Statuswert, um zu bestimmen, ob es sich um einen Erfolgs-oder Fehlercode handelt. Wenn der Statuswert ein erfolgreicher Wert ist, ist der Rückgabewert ungleich 0 (null). Wenn es sich um einen Fehlerstatus Code handelt, ist der Rückgabewert 0 (null).
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: Pdhvbisgoodstatus-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349222"
---
# <a name="pdhvbisgoodstatus-function"></a><span data-ttu-id="a9d33-105">Pdhvbisgoodstatus-Funktion</span><span class="sxs-lookup"><span data-stu-id="a9d33-105">PdhVbIsGoodStatus function</span></span>

<span data-ttu-id="a9d33-106">Die **pdhvbisgoodstatus** -Funktion testet einen Statuswert, um zu bestimmen, ob es sich um einen Erfolgs-oder Fehlercode handelt.</span><span class="sxs-lookup"><span data-stu-id="a9d33-106">The **PdhVbIsGoodStatus** function tests a status value to determine if it is a success or failure code.</span></span> <span data-ttu-id="a9d33-107">Wenn der Statuswert ein erfolgreicher Wert ist, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a9d33-107">If the status value is a successful one, then the return value will be nonzero.</span></span> <span data-ttu-id="a9d33-108">Wenn es sich um einen Fehlerstatus Code handelt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a9d33-108">If it is a failure status code, the return value will be zero.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9d33-109">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a9d33-109">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="a9d33-110">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a9d33-110">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="a9d33-111">Funktion "pdhvbisgoodstatus" ( \_ ByVal statusvalue "Long" \_ )</span><span class="sxs-lookup"><span data-stu-id="a9d33-111">Function PdhVbIsGoodStatus( \_ ByVal StatusValue As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="a9d33-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9d33-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d33-113">*Statuswert*</span><span class="sxs-lookup"><span data-stu-id="a9d33-113">*StatusValue*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d33-114">Status Wert, der von einer anderen PDH-Funktion zurückgegeben wird, die getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9d33-114">Status value returned by another PDH function that is to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d33-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9d33-115">Return value</span></span>

<span data-ttu-id="a9d33-116">Die-Funktion gibt 0 (null) zurück, wenn der Statuscode ein Fehlerstatus Code ist.</span><span class="sxs-lookup"><span data-stu-id="a9d33-116">The function returns zero if the status code is a failure status code.</span></span> <span data-ttu-id="a9d33-117">Er gibt einen Wert ungleich 0 (null) zurück, wenn der Statuscode ein Erfolgsstatus Code ist</span><span class="sxs-lookup"><span data-stu-id="a9d33-117">It returns nonzero if the status code is a success status code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d33-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9d33-118">Requirements</span></span>



| <span data-ttu-id="a9d33-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9d33-119">Requirement</span></span> | <span data-ttu-id="a9d33-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a9d33-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d33-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9d33-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d33-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9d33-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9d33-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9d33-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d33-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9d33-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a9d33-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a9d33-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9d33-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9d33-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9d33-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a9d33-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9d33-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9d33-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d33-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9d33-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d33-130">**Pdhvbgetdoublecountervalue**</span><span class="sxs-lookup"><span data-stu-id="a9d33-130">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




