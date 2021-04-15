---
title: IBackgroundCopyFile2-Methode "Setup-Servername" ("deliveryoptimization. h")
description: Ändert den Remote Namen in einen neuen URL in einem Download Auftrag.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Methode "Setup Name"
- Methode "Setup-webtename", IBackgroundCopyFile2-Schnittstelle
- IBackgroundCopyFile2 Interface, Methode "Setup Name"
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476365"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a><span data-ttu-id="2dd4c-106">IBackgroundCopyFile2:: Setup-Methode</span><span class="sxs-lookup"><span data-stu-id="2dd4c-106">IBackgroundCopyFile2::SetRemoteName method</span></span>

<span data-ttu-id="2dd4c-107">Ändert den Remote Namen in einen neuen URL in einem Download Auftrag.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-107">Changes the remote name to a new URL in a download job.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd4c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dd4c-108">Syntax</span></span>


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a><span data-ttu-id="2dd4c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dd4c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dd4c-110">*Remotename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dd4c-110">*RemoteName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd4c-111">Eine auf NULL endenden Zeichenfolge, die den Namen der Datei auf dem Server enthält.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-111">Null-terminated string that contains the name of the file on the server.</span></span> <span data-ttu-id="2dd4c-112">Weitere Informationen zum Angeben des Remote namens finden Sie unter dem **Remotename** -Member.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-112">For information on specifying the remote name, see the **RemoteName** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dd4c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2dd4c-113">Return value</span></span>

<span data-ttu-id="2dd4c-114">Diese Methode gibt sowohl die folgenden Rückgabewerte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-114">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="2dd4c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2dd4c-115">Return code</span></span>                                                                                  | <span data-ttu-id="2dd4c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dd4c-116">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2dd4c-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="2dd4c-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="2dd4c-118">Erfolg</span><span class="sxs-lookup"><span data-stu-id="2dd4c-118">Success</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="2dd4c-119"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2dd4c-119"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2dd4c-120">Der neue Remote Name ist eine ungültige URL, oder die neue URL ist zu lang (die URL darf 2.200 Zeichen nicht überschreiten).</span><span class="sxs-lookup"><span data-stu-id="2dd4c-120">The new remote name is an invalid URL or the new URL is too long (the URL cannot exceed 2,200 characters).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2dd4c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2dd4c-121">Remarks</span></span>

<span data-ttu-id="2dd4c-122">In der Regel wird diese Methode aufgerufen, wenn Sie die URL ändern möchten, die zum Übertragen der Datei verwendet wird, oder wenn Sie den Dateinamen oder den Pfad ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-122">Typically, you call this method if you want to change the URL used to transfer the file or if you want to change the file name or path.</span></span>

<span data-ttu-id="2dd4c-123">Diese Methode wird bei der Rückgabe nicht serialisiert.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-123">This method does not serialize when it returns.</span></span> <span data-ttu-id="2dd4c-124">Zum Serialisieren der Änderung unter [**brechen**](ibackgroundcopyjob-suspend.md) Sie den Auftrag, indem Sie diese Methode (wenn Sie mehrere Dateien im Auftrag ändern, [**eine-Schleife**](ibackgroundcopyjob-resume.md) verwenden) und den Auftrag fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-124">To serialize the change, [**suspend**](ibackgroundcopyjob-suspend.md) the job, call this method (if changing multiple files in the job, use a loop), and [**resume**](ibackgroundcopyjob-resume.md) the job.</span></span> <span data-ttu-id="2dd4c-125">Durch Aufrufen der Methode **ibackgroundcopyjob:: Resume** wird die Änderung serialisiert.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-125">Calling the **IBackgroundCopyJob::Resume** method serializes the change.</span></span>

<span data-ttu-id="2dd4c-126">Wenn sich der Zeitstempel oder die Dateigröße des neuen Remote namens vom vorherigen Remote Namen unterscheidet oder der neue Server die Prüf Punkt Fortsetzung (bei http-Remote Namen) nicht unterstützt, wird der Download neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-126">If the time stamp or file size of the new remote name is different from the previous remote name or the new server does not support checkpoint resume (for HTTP remote names), DO restarts the download.</span></span> <span data-ttu-id="2dd4c-127">Andernfalls wird die Übertragung von der gleichen Position auf dem neuen Server fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-127">Otherwise, the transfer resumes from the same position on the new server.</span></span> <span data-ttu-id="2dd4c-128">Führt keine Neustarts bereits übertragener Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-128">DO does not restart already transferred files.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd4c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2dd4c-129">Requirements</span></span>



| <span data-ttu-id="2dd4c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2dd4c-130">Requirement</span></span> | <span data-ttu-id="2dd4c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2dd4c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd4c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2dd4c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2dd4c-133">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2dd4c-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2dd4c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2dd4c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2dd4c-135">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2dd4c-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2dd4c-136">Header</span><span class="sxs-lookup"><span data-stu-id="2dd4c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dd4c-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dd4c-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2dd4c-138">IDL</span><span class="sxs-lookup"><span data-stu-id="2dd4c-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2dd4c-139"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2dd4c-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2dd4c-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2dd4c-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="2dd4c-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dd4c-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2dd4c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2dd4c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dd4c-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dd4c-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2dd4c-144">IID</span><span class="sxs-lookup"><span data-stu-id="2dd4c-144">IID</span></span><br/>                      | <span data-ttu-id="2dd4c-145">IID_IBackgroundCopyFile2 ist als 83e81b93-0873-474d-8a8c-f 2018b1a939c definiert.</span><span class="sxs-lookup"><span data-stu-id="2dd4c-145">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2dd4c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dd4c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd4c-147">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="2dd4c-147">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





