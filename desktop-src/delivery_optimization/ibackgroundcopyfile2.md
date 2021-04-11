---
title: IBackgroundCopyFile2-Schnittstelle (deliveryoptimization. h)
description: Geben Sie mit der IBackgroundCopyFile2-Schnittstelle einen neuen Remote Namen für die Datei an, und rufen Sie die Liste der herunter zuladenden Bereiche ab.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- IBackgroundCopyFile2-Schnittstelle
- IBackgroundCopyFile2-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040520"
---
# <a name="ibackgroundcopyfile2-interface"></a><span data-ttu-id="a6cf8-105">IBackgroundCopyFile2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a6cf8-105">IBackgroundCopyFile2 interface</span></span>

<span data-ttu-id="a6cf8-106">Geben Sie mit der **IBackgroundCopyFile2** -Schnittstelle einen neuen Remote Namen für die Datei an, und rufen Sie die Liste der herunter zuladenden Bereiche ab.</span><span class="sxs-lookup"><span data-stu-id="a6cf8-106">Use the **IBackgroundCopyFile2** interface to specify a new remote name for the file and retrieve the list of ranges to download.</span></span>

<span data-ttu-id="a6cf8-107">Die **IBackgroundCopyFile2** -Schnittstelle erbt von der [**ibackgroundcopyfile**](ibackgroundcopyfile.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a6cf8-107">The **IBackgroundCopyFile2** interface inherits from the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface.</span></span>

<span data-ttu-id="a6cf8-108">Um einen **IBackgroundCopyFile2** -Schnittstellen Zeiger abzurufen, verwenden Sie die **ibackgroundcopyfile:: QueryInterface** -Methode mithilfe __uuidof (IBackgroundCopyFile2) für den Schnittstellen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a6cf8-108">To get an **IBackgroundCopyFile2** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile2) for the interface identifier.</span></span> <span data-ttu-id="a6cf8-109">Verwenden Sie den **IBackgroundCopyFile2** -Schnittstellen Zeiger, um die [**ibackgroundcopyfile**](ibackgroundcopyfile.md) -Methode und die **IBackgroundCopyFile2** -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a6cf8-109">Use the **IBackgroundCopyFile2** interface pointer to call both the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) and **IBackgroundCopyFile2** methods.</span></span>

## <a name="members"></a><span data-ttu-id="a6cf8-110">Member</span><span class="sxs-lookup"><span data-stu-id="a6cf8-110">Members</span></span>

<span data-ttu-id="a6cf8-111">Die **IBackgroundCopyFile2** -Schnittstelle erbt von [**ibackgroundcopyfile**](ibackgroundcopyfile.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf8-111">The **IBackgroundCopyFile2** interface inherits from [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span></span> <span data-ttu-id="a6cf8-112">**IBackgroundCopyFile2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a6cf8-112">**IBackgroundCopyFile2** also has these types of members:</span></span>

-   [<span data-ttu-id="a6cf8-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="a6cf8-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a6cf8-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="a6cf8-114">Methods</span></span>

<span data-ttu-id="a6cf8-115">Die **IBackgroundCopyFile2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a6cf8-115">The **IBackgroundCopyFile2** interface has these methods.</span></span>



| <span data-ttu-id="a6cf8-116">Methode</span><span class="sxs-lookup"><span data-stu-id="a6cf8-116">Method</span></span>                                                             | <span data-ttu-id="a6cf8-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6cf8-117">Description</span></span>                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="a6cf8-118">**Getfileranges**</span><span class="sxs-lookup"><span data-stu-id="a6cf8-118">**GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md) | <span data-ttu-id="a6cf8-119">Ruft das Array von Bereichen ab, die Sie aus der URL herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="a6cf8-119">Retrieves the array of ranges that you want to download from the URL.</span></span><br/> |
| [<span data-ttu-id="a6cf8-120">**Servername**</span><span class="sxs-lookup"><span data-stu-id="a6cf8-120">**SetRemoteName**</span></span>](ibackgroundcopyfile2-setremotename-method.md) | <span data-ttu-id="a6cf8-121">Ändert den Remote Namen in eine neue URL.</span><span class="sxs-lookup"><span data-stu-id="a6cf8-121">Changes the remote name to a new URL.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="a6cf8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6cf8-122">Requirements</span></span>



| <span data-ttu-id="a6cf8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6cf8-123">Requirement</span></span> | <span data-ttu-id="a6cf8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a6cf8-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cf8-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6cf8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a6cf8-126">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6cf8-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6cf8-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6cf8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a6cf8-128">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6cf8-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a6cf8-129">Header</span><span class="sxs-lookup"><span data-stu-id="a6cf8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6cf8-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6cf8-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6cf8-131">IDL</span><span class="sxs-lookup"><span data-stu-id="a6cf8-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6cf8-132"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6cf8-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a6cf8-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a6cf8-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6cf8-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6cf8-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a6cf8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a6cf8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6cf8-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6cf8-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a6cf8-137">IID</span><span class="sxs-lookup"><span data-stu-id="a6cf8-137">IID</span></span><br/>                      | <span data-ttu-id="a6cf8-138">IID_IBackgroundCopyFile2 ist als 83e81b93-0873-474d-8a8c-f 2018b1a939c definiert.</span><span class="sxs-lookup"><span data-stu-id="a6cf8-138">IID_IBackgroundCopyFile2 is defined as 83E81B93-0873-474D-8A8C-F2018B1A939C</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="a6cf8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6cf8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6cf8-140">**Ibackgroundcopyfile**</span><span class="sxs-lookup"><span data-stu-id="a6cf8-140">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> </dl>

 

 





