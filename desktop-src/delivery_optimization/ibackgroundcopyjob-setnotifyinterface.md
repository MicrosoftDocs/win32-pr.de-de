---
title: Ibackgroundcopyjob setnotifyinterface-Methode (deliveryoptimization. h)
description: Gibt die Implementierung der ibackgroundcopycallback-Schnittstelle an. Verwenden Sie die ibackgroundcopycallback-Schnittstelle zum Empfangen von Benachrichtigungen über auftragsbezogene Ereignisse.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Setnotifyinterface-Methode
- Setnotifyinterface-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, setnotifyinterface-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340618"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a><span data-ttu-id="4851e-107">Ibackgroundcopyjob:: setnotifyinterface-Methode</span><span class="sxs-lookup"><span data-stu-id="4851e-107">IBackgroundCopyJob::SetNotifyInterface method</span></span>

<span data-ttu-id="4851e-108">Gibt die Implementierung der [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="4851e-108">Identifies your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to DO.</span></span> <span data-ttu-id="4851e-109">Verwenden Sie die **ibackgroundcopycallback** -Schnittstelle zum Empfangen von Benachrichtigungen über auftragsbezogene Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="4851e-109">Use the **IBackgroundCopyCallback** interface to receive notification of job-related events.</span></span>

## <a name="syntax"></a><span data-ttu-id="4851e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4851e-110">Syntax</span></span>


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="4851e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4851e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4851e-112">*pnotifyinterface*</span><span class="sxs-lookup"><span data-stu-id="4851e-112">*pNotifyInterface*</span></span> 
</dt> <dd>

<span data-ttu-id="4851e-113">Ein [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4851e-113">An [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface pointer.</span></span> <span data-ttu-id="4851e-114">Legen Sie diesen Parameter auf **null** fest, um den aktuellen Rückruf Schnittstellen Zeiger zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4851e-114">To remove the current callback interface pointer, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4851e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4851e-115">Return value</span></span>

<span data-ttu-id="4851e-116">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="4851e-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="4851e-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4851e-117">Return code</span></span>                                                                              | <span data-ttu-id="4851e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4851e-118">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4851e-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="4851e-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="4851e-120">Der Benachrichtigungs Schnittstellen Zeiger wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4851e-120">Notification interface pointer was successfully set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4851e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4851e-121">Remarks</span></span>

<span data-ttu-id="4851e-122">Rufen Sie diese Methode nur auf, wenn Sie die [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="4851e-122">Call this method only if you implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="4851e-123">Verwenden Sie die **setnotifyinterface** -Methode in Verbindung mit der [**setnotifyflags**](ibackgroundcopyjob-setnotifyflags.md) -Methode, um den Typ der Benachrichtigung anzugeben, die Sie empfangen möchten.</span><span class="sxs-lookup"><span data-stu-id="4851e-123">Use the **SetNotifyInterface** method in conjunction with the [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to specify the type of notification that you want to receive.</span></span>

<span data-ttu-id="4851e-124">Die Benachrichtigungs Schnittstelle wird ungültig, wenn die Anwendung beendet wird. Behält die Benachrichtigungs Schnittstelle nicht bei.</span><span class="sxs-lookup"><span data-stu-id="4851e-124">The notification interface becomes invalid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="4851e-125">Folglich sollte der Initialisierungs Prozess ihrer Anwendung die **setnotifyinterface** -Methode für die vorhandenen Aufträge aufrufen, für die Sie eine Benachrichtigung erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="4851e-125">As a result, your application's initialization process should call the **SetNotifyInterface** method on those existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="4851e-126">Wenn Sie Zustands-und Statusinformationen erfassen müssen, die seit der letzten Ausführung der Anwendung aufgetreten sind, rufen Sie während der Anwendungs Initialisierung Informationen zum Status und zum Fortschritt ab.</span><span class="sxs-lookup"><span data-stu-id="4851e-126">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="4851e-127">Nur der Auftrags Besitzer/-Ersteller oder ein Administrator kann sich für Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="4851e-127">Only the job owner/creator or an administrator can register for notifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="4851e-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4851e-128">Requirements</span></span>



| <span data-ttu-id="4851e-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4851e-129">Requirement</span></span> | <span data-ttu-id="4851e-130">Wert</span><span class="sxs-lookup"><span data-stu-id="4851e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4851e-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4851e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4851e-132">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4851e-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4851e-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4851e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4851e-134">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4851e-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4851e-135">Header</span><span class="sxs-lookup"><span data-stu-id="4851e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4851e-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4851e-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4851e-137">IDL</span><span class="sxs-lookup"><span data-stu-id="4851e-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4851e-138"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4851e-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4851e-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4851e-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="4851e-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4851e-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4851e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4851e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4851e-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4851e-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4851e-143">IID</span><span class="sxs-lookup"><span data-stu-id="4851e-143">IID</span></span><br/>                      | <span data-ttu-id="4851e-144">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="4851e-144">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4851e-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4851e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4851e-146">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="4851e-146">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="4851e-147">**Ibackgroundcopycallback**</span><span class="sxs-lookup"><span data-stu-id="4851e-147">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="4851e-148">**Ibackgroundcopyjob:: getnotifyinterface**</span><span class="sxs-lookup"><span data-stu-id="4851e-148">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="4851e-149">**Ibackgroundcopyjob:: setnotifyflags**</span><span class="sxs-lookup"><span data-stu-id="4851e-149">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





