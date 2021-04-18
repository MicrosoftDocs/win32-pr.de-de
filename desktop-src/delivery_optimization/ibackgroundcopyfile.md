---
title: Ibackgroundcopyfile-Schnittstelle (deliveryoptimization. h)
description: Ibackgroundcopyfile enthält Informationen zu einer Datei, die Teil eines Auftrags ist. Beispielsweise können Sie die ibackgroundcopyfile-Methoden verwenden, um die lokalen und Remote Namen der Datei abzurufen und Statusinformationen zu übertragen.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Ibackgroundcopyfile-Schnittstelle
- Ibackgroundcopyfile-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337506"
---
# <a name="ibackgroundcopyfile-interface"></a><span data-ttu-id="95db2-106">Ibackgroundcopyfile-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="95db2-106">IBackgroundCopyFile interface</span></span>

<span data-ttu-id="95db2-107">**Ibackgroundcopyfile** enthält Informationen zu einer Datei, die Teil eines Auftrags ist.</span><span class="sxs-lookup"><span data-stu-id="95db2-107">**IBackgroundCopyFile** contains information about a file that is part of a job.</span></span> <span data-ttu-id="95db2-108">Beispielsweise können Sie die **ibackgroundcopyfile** -Methoden verwenden, um die lokalen und Remote Namen der Datei abzurufen und Statusinformationen zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="95db2-108">For example, you can use **IBackgroundCopyFile** methods to retrieve the local and remote names of the file and transfer progress information.</span></span>

<span data-ttu-id="95db2-109">Um einen **ibackgroundcopyfile** -Schnittstellen Zeiger abzurufen, müssen Sie die [**ibackgroundcopyerror:: GetFile**](ibackgroundcopyerror-getfile-method.md) -Methode oder die [**ienumbackgroundcopyfiles:: Next**](ienumbackgroundcopyfiles-next.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="95db2-109">To get an **IBackgroundCopyFile** interface pointer, call the [**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md) method or the [**IEnumBackgroundCopyFiles::Next**](ienumbackgroundcopyfiles-next.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="95db2-110">Member</span><span class="sxs-lookup"><span data-stu-id="95db2-110">Members</span></span>

<span data-ttu-id="95db2-111">Die **ibackgroundcopyfile** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="95db2-111">The **IBackgroundCopyFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="95db2-112">**Ibackgroundcopyfile** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="95db2-112">**IBackgroundCopyFile** also has these types of members:</span></span>

-   [<span data-ttu-id="95db2-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="95db2-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="95db2-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="95db2-114">Methods</span></span>

<span data-ttu-id="95db2-115">Die **ibackgroundcopyfile** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="95db2-115">The **IBackgroundCopyFile** interface has these methods.</span></span>



| <span data-ttu-id="95db2-116">Methode</span><span class="sxs-lookup"><span data-stu-id="95db2-116">Method</span></span>                                                            | <span data-ttu-id="95db2-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95db2-117">Description</span></span>                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="95db2-118">**GetLocalName**</span><span class="sxs-lookup"><span data-stu-id="95db2-118">**GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)   | <span data-ttu-id="95db2-119">Ruft den lokalen Namen der Datei ab.</span><span class="sxs-lookup"><span data-stu-id="95db2-119">Retrieves the local name of the file.</span></span><br/>        |
| [<span data-ttu-id="95db2-120">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="95db2-120">**GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)     | <span data-ttu-id="95db2-121">Ruft den Fortschritt der Dateiübertragung ab.</span><span class="sxs-lookup"><span data-stu-id="95db2-121">Retrieves the progress of the file transfer.</span></span><br/> |
| [<span data-ttu-id="95db2-122">**Getremutename**</span><span class="sxs-lookup"><span data-stu-id="95db2-122">**GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md) | <span data-ttu-id="95db2-123">Ruft den Remote Namen der Datei ab.</span><span class="sxs-lookup"><span data-stu-id="95db2-123">Retrieves the remote name of the file.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="95db2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95db2-124">Requirements</span></span>



| <span data-ttu-id="95db2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95db2-125">Requirement</span></span> | <span data-ttu-id="95db2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="95db2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95db2-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95db2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="95db2-128">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95db2-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="95db2-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95db2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="95db2-130">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95db2-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="95db2-131">Header</span><span class="sxs-lookup"><span data-stu-id="95db2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="95db2-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="95db2-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="95db2-133">IDL</span><span class="sxs-lookup"><span data-stu-id="95db2-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95db2-134"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95db2-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="95db2-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95db2-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="95db2-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95db2-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="95db2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="95db2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95db2-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95db2-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="95db2-139">IID</span><span class="sxs-lookup"><span data-stu-id="95db2-139">IID</span></span><br/>                      | <span data-ttu-id="95db2-140">IID_IBackgroundCopyFile ist als 01b7bd23-B88-4a77-8490-5891d3e4653a definiert.</span><span class="sxs-lookup"><span data-stu-id="95db2-140">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="95db2-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95db2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95db2-142">**Ibackgroundcopyerror**</span><span class="sxs-lookup"><span data-stu-id="95db2-142">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="95db2-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="95db2-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> <dt>

[<span data-ttu-id="95db2-144">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="95db2-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="95db2-145">**Ienumbackgroundcopyfiles**</span><span class="sxs-lookup"><span data-stu-id="95db2-145">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

