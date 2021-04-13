---
title: Vmtaskresult-Enumeration (vpccominterfaces. h)
description: Gibt das Ergebnis einer Aufgabe an.
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- Vmtaskresult-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903425ca8036e1862df7042f16946fc0f2e9cc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518908"
---
# <a name="vmtaskresult-enumeration"></a><span data-ttu-id="7207c-104">Vmtaskresult-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7207c-104">VMTaskResult enumeration</span></span>

<span data-ttu-id="7207c-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7207c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7207c-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7207c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7207c-107">Gibt das Ergebnis einer Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="7207c-107">Specifies the result of a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="7207c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7207c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a><span data-ttu-id="7207c-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7207c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7207c-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmtaskresult \_ erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="7207c-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult\_Success**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-111">Der Task wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7207c-111">The task was successful.</span></span>

</dd> <dt>

<span data-ttu-id="7207c-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmtaskresult \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="7207c-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult\_Cancelled**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-113">Der Task wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="7207c-113">The task was canceled.</span></span>

</dd> <dt>

<span data-ttu-id="7207c-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmtaskresult \_ unexpectederror**</span><span class="sxs-lookup"><span data-stu-id="7207c-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult\_UnexpectedError**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-115">Unerwarteter Fehler bei der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="7207c-115">The task had an unexpected error.</span></span>

</dd> <dt>

<span data-ttu-id="7207c-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmtaskresult \_ outo-MemoryError**</span><span class="sxs-lookup"><span data-stu-id="7207c-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult\_OutOfMemoryError**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-117">Es war nicht genügend Arbeitsspeicher vorhanden, um den Task abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7207c-117">There was not enough memory for the task to complete.</span></span>

</dd> <dt>

<span data-ttu-id="7207c-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmtaskresult \_ diskrelatederror**</span><span class="sxs-lookup"><span data-stu-id="7207c-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult\_DiskRelatedError**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-119">Fehler bei der Aufgabe beim Schreiben auf den Datenträger (stellen Sie sicher, dass genügend Speicherplatz vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="7207c-119">The task had an error while writing to disk (make sure there is enough disk space).</span></span>

</dd> <dt>

<span data-ttu-id="7207c-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmtaskresult \_ incompatiblesavedstateerror**</span><span class="sxs-lookup"><span data-stu-id="7207c-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult\_IncompatibleSavedStateError**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-121">Die virtuelle Maschine konnte nicht wieder hergestellt werden, da der gespeicherte Zustand nicht kompatibel war.</span><span class="sxs-lookup"><span data-stu-id="7207c-121">The virtual machine could not restore because the saved state was incompatible.</span></span>

</dd> <dt>

<span data-ttu-id="7207c-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmtaskresult \_ timeouterror**</span><span class="sxs-lookup"><span data-stu-id="7207c-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult\_TimeOutError**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-123">Timeout beim Task.</span><span class="sxs-lookup"><span data-stu-id="7207c-123">The task timed out.</span></span>

</dd> <dt>

<span data-ttu-id="7207c-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmtaskresult \_ illegalvalueerror**</span><span class="sxs-lookup"><span data-stu-id="7207c-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult\_IllegalValueError**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-125">Beim Verarbeiten der Aufgabe wurde ein unzulässiger Einstellungs Wert gelesen.</span><span class="sxs-lookup"><span data-stu-id="7207c-125">An illegal preference value was read while the task was processing.</span></span>

</dd> <dt>

<span data-ttu-id="7207c-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmtaskresult \_ threadcrasherror**</span><span class="sxs-lookup"><span data-stu-id="7207c-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult\_ThreadCrashError**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-127">Ein dem Task zugeordneter Thread ist abgestürzt.</span><span class="sxs-lookup"><span data-stu-id="7207c-127">A thread associated with the task crashed.</span></span>

</dd> <dt>

<span data-ttu-id="7207c-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmtaskresult \_ shutdownabort**</span><span class="sxs-lookup"><span data-stu-id="7207c-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult\_ShutdownAbort**</span></span>
</dt> <dd>

<span data-ttu-id="7207c-129">Das angeforderte Herunterfahren wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="7207c-129">The shutdown requested was aborted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7207c-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7207c-130">Requirements</span></span>



| <span data-ttu-id="7207c-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7207c-131">Requirement</span></span> | <span data-ttu-id="7207c-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7207c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7207c-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7207c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7207c-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7207c-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7207c-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7207c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7207c-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7207c-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7207c-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7207c-137">End of client support</span></span><br/>    | <span data-ttu-id="7207c-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7207c-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7207c-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="7207c-139">Product</span></span><br/>                  | <span data-ttu-id="7207c-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7207c-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7207c-141">Header</span><span class="sxs-lookup"><span data-stu-id="7207c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7207c-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7207c-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7207c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7207c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7207c-144">**Ivmtask:: result**</span><span class="sxs-lookup"><span data-stu-id="7207c-144">**IVMTask::Result**</span></span>](ivmtask-result.md)
</dt> </dl>

 

