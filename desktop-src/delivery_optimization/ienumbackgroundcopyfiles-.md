---
title: Ienumbackgroundcopyfiles-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie die ienumbackgroundcopyfiles-Schnittstelle zum Auflisten der Dateien, die in einem Auftrag enthalten sind. Um einen ienumbackgroundcopyfiles-Schnittstellen Zeiger abzurufen, nennen Sie die ibackgroundcopyjob-EnumFiles-Methode.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Ienumbackgroundcopyfiles-Schnittstelle
- Ienumbackgroundcopyfiles-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340330"
---
# <a name="ienumbackgroundcopyfiles-interface"></a><span data-ttu-id="d57fa-106">Ienumbackgroundcopyfiles-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d57fa-106">IEnumBackgroundCopyFiles interface</span></span>

<span data-ttu-id="d57fa-107">Verwenden Sie die **ienumbackgroundcopyfiles** -Schnittstelle zum Auflisten der Dateien, die in einem Auftrag enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d57fa-107">Use the **IEnumBackgroundCopyFiles** interface to enumerate the files that a job contains.</span></span> <span data-ttu-id="d57fa-108">Um einen **ienumbackgroundcopyfiles** -Schnittstellen Zeiger abzurufen, nennen Sie die [**ibackgroundcopyjob:: EnumFiles**](ibackgroundcopyjob-enumfiles.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d57fa-108">To get an **IEnumBackgroundCopyFiles** interface pointer, call the [**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="d57fa-109">Member</span><span class="sxs-lookup"><span data-stu-id="d57fa-109">Members</span></span>

<span data-ttu-id="d57fa-110">Die **ienumbackgroundcopyfiles** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d57fa-110">The **IEnumBackgroundCopyFiles** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d57fa-111">**Ienumbackgroundcopyfiles** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d57fa-111">**IEnumBackgroundCopyFiles** also has these types of members:</span></span>

-   [<span data-ttu-id="d57fa-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="d57fa-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d57fa-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d57fa-113">Methods</span></span>

<span data-ttu-id="d57fa-114">Die **ienumbackgroundcopyfiles** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d57fa-114">The **IEnumBackgroundCopyFiles** interface has these methods.</span></span>



| <span data-ttu-id="d57fa-115">Methode</span><span class="sxs-lookup"><span data-stu-id="d57fa-115">Method</span></span>                                                | <span data-ttu-id="d57fa-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d57fa-116">Description</span></span>                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="d57fa-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="d57fa-117">**GetCount**</span></span>](ienumbackgroundcopyfiles-getcount.md) | <span data-ttu-id="d57fa-118">Ruft die Anzahl der Elemente in der-Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="d57fa-118">Retrieves the number of items in the enumeration.</span></span><br/>                  |
| [<span data-ttu-id="d57fa-119">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="d57fa-119">**Next**</span></span>](ienumbackgroundcopyfiles-next.md)         | <span data-ttu-id="d57fa-120">Ruft eine angegebene Anzahl von Elementen in der Enumerationsfolge ab.</span><span class="sxs-lookup"><span data-stu-id="d57fa-120">Retrieves a specified number of items in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="d57fa-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="d57fa-121">**Reset**</span></span>](ienumbackgroundcopyfiles-reset.md)       | <span data-ttu-id="d57fa-122">Setzt die Enumerationsfolge auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="d57fa-122">Resets the enumeration sequence to the beginning.</span></span><br/>                  |
| [<span data-ttu-id="d57fa-123">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="d57fa-123">**Skip**</span></span>](ienumbackgroundcopyfiles-skip.md)         | <span data-ttu-id="d57fa-124">Überspringt eine angegebene Anzahl von Elementen in der Enumerationsfolge.</span><span class="sxs-lookup"><span data-stu-id="d57fa-124">Skips a specified number of items in the enumeration sequence.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="d57fa-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d57fa-125">Requirements</span></span>



| <span data-ttu-id="d57fa-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d57fa-126">Requirement</span></span> | <span data-ttu-id="d57fa-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d57fa-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d57fa-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d57fa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d57fa-129">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d57fa-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d57fa-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d57fa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d57fa-131">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d57fa-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d57fa-132">Header</span><span class="sxs-lookup"><span data-stu-id="d57fa-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d57fa-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57fa-133"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d57fa-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d57fa-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d57fa-135"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d57fa-135"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d57fa-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d57fa-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="d57fa-137"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d57fa-137"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d57fa-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d57fa-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d57fa-139"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d57fa-139"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d57fa-140">IID</span><span class="sxs-lookup"><span data-stu-id="d57fa-140">IID</span></span><br/>                      | <span data-ttu-id="d57fa-141">IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.</span><span class="sxs-lookup"><span data-stu-id="d57fa-141">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d57fa-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d57fa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57fa-143">**Ibackgroundcopyjob:: EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="d57fa-143">**IBackgroundCopyJob::EnumFiles**</span></span>](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

