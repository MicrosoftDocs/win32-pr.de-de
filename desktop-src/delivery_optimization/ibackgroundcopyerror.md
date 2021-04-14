---
title: Ibackgroundcopyerror-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie die ibackgroundcopyerror-Schnittstelle, um die Ursache eines Fehlers zu ermitteln, und, wenn der Übertragungsprozess fortgesetzt werden kann.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Ibackgroundcopyerror-Schnittstelle
- Ibackgroundcopyerror-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476371"
---
# <a name="ibackgroundcopyerror-interface"></a><span data-ttu-id="1438a-105">Ibackgroundcopyerror-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1438a-105">IBackgroundCopyError interface</span></span>

<span data-ttu-id="1438a-106">Verwenden Sie die **ibackgroundcopyerror** -Schnittstelle, um die Ursache eines Fehlers zu ermitteln, und, wenn der Übertragungsprozess fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1438a-106">Use the **IBackgroundCopyError** interface to determine the cause of an error and if the transfer process can proceed.</span></span>

<span data-ttu-id="1438a-107">Erstellt nur dann ein Fehler Objekt, wenn der Status des Auftrags BG_JOB_STATE_ERROR oder BG_JOB_STATE_TRANSIENT_ERROR ist.</span><span class="sxs-lookup"><span data-stu-id="1438a-107">DO creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="1438a-108">Erstellt kein Fehler Objekt, wenn eine **ibackgroundcopyxxxx** -Schnittstellen Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="1438a-108">DO does not create an error object when an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="1438a-109">Das Error-Objekt ist verfügbar, bis die Daten übertragen werden (der Status des Auftrags ändert sich in BG_JOB_STATE_TRANSFERRING) für den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="1438a-109">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job.</span></span>

<span data-ttu-id="1438a-110">Zum Abrufen eines **ibackgroundcopyerror** -Objekts müssen Sie die [**ibackgroundcopyjob:: getError**](ibackgroundcopyjob-geterror.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1438a-110">To get an **IBackgroundCopyError** object, call the [**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="1438a-111">Member</span><span class="sxs-lookup"><span data-stu-id="1438a-111">Members</span></span>

<span data-ttu-id="1438a-112">Die **ibackgroundcopyerror** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1438a-112">The **IBackgroundCopyError** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1438a-113">**Ibackgroundcopyerror** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1438a-113">**IBackgroundCopyError** also has these types of members:</span></span>

-   [<span data-ttu-id="1438a-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="1438a-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1438a-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="1438a-115">Methods</span></span>

<span data-ttu-id="1438a-116">Die **ibackgroundcopyerror** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1438a-116">The **IBackgroundCopyError** interface has these methods.</span></span>



| <span data-ttu-id="1438a-117">Methode</span><span class="sxs-lookup"><span data-stu-id="1438a-117">Method</span></span>                                                   | <span data-ttu-id="1438a-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1438a-118">Description</span></span>                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1438a-119">**GetError**</span><span class="sxs-lookup"><span data-stu-id="1438a-119">**GetError**</span></span>](ibackgroundcopyerror-geterror-method.md) | <span data-ttu-id="1438a-120">Ruft den Fehlercode ab und identifiziert den Kontext, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1438a-120">Retrieves the error code and identifies the context in which the error occurred.</span></span><br/> |
| [<span data-ttu-id="1438a-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="1438a-121">**GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)   | <span data-ttu-id="1438a-122">Ruft einen Schnittstellen Zeiger auf das File-Objekt ab, das dem Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1438a-122">Retrieves an interface pointer to the file object associated with the error.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="1438a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1438a-123">Requirements</span></span>



| <span data-ttu-id="1438a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1438a-124">Requirement</span></span> | <span data-ttu-id="1438a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1438a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1438a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1438a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1438a-127">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1438a-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1438a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1438a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1438a-129">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1438a-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1438a-130">Header</span><span class="sxs-lookup"><span data-stu-id="1438a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1438a-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1438a-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="1438a-132">IDL</span><span class="sxs-lookup"><span data-stu-id="1438a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1438a-133"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1438a-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="1438a-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1438a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="1438a-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1438a-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="1438a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1438a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1438a-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1438a-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="1438a-138">IID</span><span class="sxs-lookup"><span data-stu-id="1438a-138">IID</span></span><br/>                      | <span data-ttu-id="1438a-139">IID_IBackgroundCopyError ist als 19c613a0-fcb8-4f 28-81ae-897c3d078-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="1438a-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="1438a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1438a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1438a-141">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="1438a-141">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="1438a-142">**Ibackgroundcopyjob:: getError**</span><span class="sxs-lookup"><span data-stu-id="1438a-142">**IBackgroundCopyJob::GetError**</span></span>](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[<span data-ttu-id="1438a-143">**Ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="1438a-143">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[<span data-ttu-id="1438a-144">**Ibackgroundcopycallback:: joberror**</span><span class="sxs-lookup"><span data-stu-id="1438a-144">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

