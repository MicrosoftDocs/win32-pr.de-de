---
title: Ivmtask waitforcompletion-Methode (vpccominterfaces. h)
description: Wartet, bis die Aufgabe beendet oder das angegebene Timeout Intervall abläuft.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Waitforcompletion-Methode Virtual PC
- Waitforcompletion-Methode Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, waitforcompletion-Methode
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341411"
---
# <a name="ivmtaskwaitforcompletion-method"></a><span data-ttu-id="7332c-106">Ivmtask:: waitforcompletion-Methode</span><span class="sxs-lookup"><span data-stu-id="7332c-106">IVMTask::WaitForCompletion method</span></span>

<span data-ttu-id="7332c-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7332c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7332c-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7332c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7332c-109">Wartet, bis die Aufgabe beendet oder das angegebene Timeout Intervall abläuft.</span><span class="sxs-lookup"><span data-stu-id="7332c-109">Waits for the task to complete or for the specified time-out interval to elapse.</span></span>

## <a name="syntax"></a><span data-ttu-id="7332c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7332c-110">Syntax</span></span>


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a><span data-ttu-id="7332c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7332c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7332c-112">*Timeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7332c-112">*timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7332c-113">Die Zeit in Millisekunden, die diese Methode auf den Abschluss der Aufgabe wartet, bevor die Steuerung an den Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7332c-113">The time, in milliseconds, that this method will wait for task completion before returning control to the caller.</span></span> <span data-ttu-id="7332c-114">Der Wert-1 gibt an, dass die Methode wartet, bis die Aufgabe abgeschlossen ist, ohne dass ein Timeout eintritt. Weitere gültige Timeout Werte liegen im Bereich von 0 bis 4 Millionen Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="7332c-114">A value of -1 specifies that method will wait until the task completes without timing out. Other valid timeout values range from 0 to 4,000,000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7332c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7332c-115">Return value</span></span>

<span data-ttu-id="7332c-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7332c-116">This method can return one of these values.</span></span>



| <span data-ttu-id="7332c-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="7332c-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="7332c-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7332c-118">Description</span></span>                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7332c-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7332c-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7332c-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7332c-120">The operation was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="7332c-121"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="7332c-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="7332c-122">Der *Timeout* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7332c-122">The *timeout* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="7332c-123"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7332c-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7332c-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7332c-124">An unexpected error has occurred.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="7332c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7332c-125">Remarks</span></span>

<span data-ttu-id="7332c-126">Die **waitforcompletion** -Methode versetzt den aktuellen Ausführungs Thread in den Standbymodus, bis er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7332c-126">The **WaitForCompletion** method puts the current execution thread to sleep until it returns.</span></span> <span data-ttu-id="7332c-127">Das Angeben einer unendlichen Wartezeit (Timeout =-1) wird nur empfohlen, wenn es absolut wichtig ist, dass die Aufgabe unter einem beliebigen Umstand abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7332c-127">Specifying an infinite wait (timeout = -1) is not recommended unless it is absolutely critical that the task completes under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="7332c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7332c-128">Requirements</span></span>



| <span data-ttu-id="7332c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7332c-129">Requirement</span></span> | <span data-ttu-id="7332c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7332c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7332c-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7332c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7332c-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7332c-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7332c-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7332c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7332c-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7332c-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7332c-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7332c-135">End of client support</span></span><br/>    | <span data-ttu-id="7332c-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7332c-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7332c-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="7332c-137">Product</span></span><br/>                  | <span data-ttu-id="7332c-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7332c-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7332c-139">Header</span><span class="sxs-lookup"><span data-stu-id="7332c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7332c-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7332c-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7332c-141">IID</span><span class="sxs-lookup"><span data-stu-id="7332c-141">IID</span></span><br/>                      | <span data-ttu-id="7332c-142">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="7332c-142">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="7332c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7332c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7332c-144">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="7332c-144">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

