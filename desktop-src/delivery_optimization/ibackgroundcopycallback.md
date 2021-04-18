---
title: Ibackgroundcopycallback-Schnittstelle (deliveryoptimization. h)
description: Implementieren Sie die ibackgroundcopycallback-Schnittstelle, um eine Benachrichtigung zu erhalten, dass ein Auftrag abgeschlossen ist, geändert wurde oder fehlerhaft ist. Clients verwenden diese Schnittstelle, anstatt den Status des Auftrags abzufragen.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Ibackgroundcopycallback-Schnittstelle
- Ibackgroundcopycallback-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340326"
---
# <a name="ibackgroundcopycallback-interface"></a><span data-ttu-id="9a90c-106">Ibackgroundcopycallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9a90c-106">IBackgroundCopyCallback interface</span></span>

<span data-ttu-id="9a90c-107">Implementieren Sie die **ibackgroundcopycallback** -Schnittstelle, um eine Benachrichtigung zu erhalten, dass ein Auftrag abgeschlossen ist, geändert wurde oder fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="9a90c-107">Implement the **IBackgroundCopyCallback** interface to receive notification that a job is complete, has been modified, or is in error.</span></span> <span data-ttu-id="9a90c-108">Clients verwenden diese Schnittstelle, anstatt den Status des Auftrags abzufragen.</span><span class="sxs-lookup"><span data-stu-id="9a90c-108">Clients use this interface instead of polling for the status of the job.</span></span>

## <a name="members"></a><span data-ttu-id="9a90c-109">Member</span><span class="sxs-lookup"><span data-stu-id="9a90c-109">Members</span></span>

<span data-ttu-id="9a90c-110">Die **ibackgroundcopycallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9a90c-110">The **IBackgroundCopyCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9a90c-111">**Ibackgroundcopycallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9a90c-111">**IBackgroundCopyCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="9a90c-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="9a90c-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9a90c-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="9a90c-113">Methods</span></span>

<span data-ttu-id="9a90c-114">Die **ibackgroundcopycallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9a90c-114">The **IBackgroundCopyCallback** interface has these methods.</span></span>



| <span data-ttu-id="9a90c-115">Methode</span><span class="sxs-lookup"><span data-stu-id="9a90c-115">Method</span></span>                                                                    | <span data-ttu-id="9a90c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a90c-116">Description</span></span>                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="9a90c-117">**Joberror**</span><span class="sxs-lookup"><span data-stu-id="9a90c-117">**JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)               | <span data-ttu-id="9a90c-118">Wird aufgerufen, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="9a90c-118">Called when an error occurs.</span></span><br/>                                           |
| [<span data-ttu-id="9a90c-119">**Jobmodifizierung**</span><span class="sxs-lookup"><span data-stu-id="9a90c-119">**JobModification**</span></span>](ibackgroundcopycallback-jobmodification-method.md) | <span data-ttu-id="9a90c-120">Wird aufgerufen, wenn ein Auftrag geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9a90c-120">Called when a job is modified.</span></span><br/>                                         |
| [<span data-ttu-id="9a90c-121">**Jobübertragene**</span><span class="sxs-lookup"><span data-stu-id="9a90c-121">**JobTransferred**</span></span>](ibackgroundcopycallback-jobtransferred.md)          | <span data-ttu-id="9a90c-122">Wird aufgerufen, wenn alle Dateien im Auftrag erfolgreich übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="9a90c-122">Called when all of the files in the job have successfully transferred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a90c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a90c-123">Remarks</span></span>

<span data-ttu-id="9a90c-124">Um Benachrichtigungen zu empfangen, rufen Sie die [**ibackgroundcopyjob:: setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md) -Methode auf, um den Schnittstellen Zeiger auf die **ibackgroundcopycallback** -Implementierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9a90c-124">To receive notifications, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to specify the interface pointer to your **IBackgroundCopyCallback** implementation.</span></span> <span data-ttu-id="9a90c-125">Um anzugeben, welche Benachrichtigungen Sie empfangen möchten, müssen Sie die [**ibackgroundcopyjob:: setnotifyflags**](ibackgroundcopyjob-setnotifyflags.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9a90c-125">To specify which notifications you want to receive, call the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method.</span></span>

<span data-ttu-id="9a90c-126">Ruft ihre Rückrufe auf, solange der Schnittstellen Zeiger gültig ist.</span><span class="sxs-lookup"><span data-stu-id="9a90c-126">DO will call your callbacks as long as the interface pointer is valid.</span></span> <span data-ttu-id="9a90c-127">Die Benachrichtigungs Schnittstelle ist nicht mehr gültig, wenn die Anwendung beendet wird. Behält die Benachrichtigungs Schnittstelle nicht bei.</span><span class="sxs-lookup"><span data-stu-id="9a90c-127">The notification interface is no longer valid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="9a90c-128">Folglich sollte der Initialisierungs Prozess ihrer Anwendung die [**setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md) -Methode für die vorhandenen Aufträge aufrufen, für die Sie eine Benachrichtigung erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="9a90c-128">As a result, your application's initialization process should call the [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method on those existing jobs for which you want to receive notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a90c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a90c-129">Requirements</span></span>



| <span data-ttu-id="9a90c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a90c-130">Requirement</span></span> | <span data-ttu-id="9a90c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9a90c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a90c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a90c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9a90c-133">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a90c-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9a90c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a90c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9a90c-135">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a90c-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9a90c-136">Header</span><span class="sxs-lookup"><span data-stu-id="9a90c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a90c-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a90c-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a90c-138">IDL</span><span class="sxs-lookup"><span data-stu-id="9a90c-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a90c-139"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a90c-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9a90c-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a90c-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a90c-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a90c-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9a90c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9a90c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a90c-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a90c-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9a90c-144">IID</span><span class="sxs-lookup"><span data-stu-id="9a90c-144">IID</span></span><br/>                      | <span data-ttu-id="9a90c-145">IID_IBackgroundCopyCallback ist als 97ea99c7-0186-4ad4-8df9-c5b4e0ed6b22 definiert.</span><span class="sxs-lookup"><span data-stu-id="9a90c-145">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="9a90c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a90c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a90c-147">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="9a90c-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="9a90c-148">**Ibackgroundcopyjob:: setnotifyflags**</span><span class="sxs-lookup"><span data-stu-id="9a90c-148">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="9a90c-149">**Ibackgroundcopyjob:: setnotifyinterface**</span><span class="sxs-lookup"><span data-stu-id="9a90c-149">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

