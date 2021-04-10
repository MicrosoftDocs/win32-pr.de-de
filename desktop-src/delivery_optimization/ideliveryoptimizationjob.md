---
title: Ideliveryoptimizationjob-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie die ideliveryoptimizationjob-Schnittstelle, um Bereiche einer Datei herunterzuladen.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Ideliveryoptimizationjob-Schnittstelle
- Ideliveryoptimizationjob-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103653"
---
# <a name="ideliveryoptimizationjob-interface"></a><span data-ttu-id="27efe-105">Ideliveryoptimizationjob-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="27efe-105">IDeliveryOptimizationJob interface</span></span>

<span data-ttu-id="27efe-106">Verwenden Sie die **ideliveryoptimizationjob** -Schnittstelle, um Bereiche einer Datei herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="27efe-106">Use the **IDeliveryOptimizationJob** interface to download ranges of a file.</span></span>

## <a name="members"></a><span data-ttu-id="27efe-107">Member</span><span class="sxs-lookup"><span data-stu-id="27efe-107">Members</span></span>

<span data-ttu-id="27efe-108">Die **ideliveryoptimizationjob** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="27efe-108">The **IDeliveryOptimizationJob** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="27efe-109">**Ideliveryoptimizationjob** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="27efe-109">**IDeliveryOptimizationJob** also has these types of members:</span></span>

- [<span data-ttu-id="27efe-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="27efe-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="27efe-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="27efe-111">Methods</span></span>

<span data-ttu-id="27efe-112">Die **ideliveryoptimizationjob** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="27efe-112">The **IDeliveryOptimizationJob** interface has these methods.</span></span>



| <span data-ttu-id="27efe-113">Methode</span><span class="sxs-lookup"><span data-stu-id="27efe-113">Method</span></span>                                                                  | <span data-ttu-id="27efe-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27efe-114">Description</span></span>                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27efe-115">**ADDFILEWITHRANGES**</span><span class="sxs-lookup"><span data-stu-id="27efe-115">**AddFileWithRanges**</span></span>](ideliveryoptimizationjob-addfilewithranges.md) | <span data-ttu-id="27efe-116">Fügt einem Download Auftrag eine Datei hinzu und gibt die Bereiche der Datei an, die Sie herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="27efe-116">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="27efe-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27efe-117">Requirements</span></span>



| <span data-ttu-id="27efe-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27efe-118">Requirement</span></span> | <span data-ttu-id="27efe-119">Wert</span><span class="sxs-lookup"><span data-stu-id="27efe-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27efe-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27efe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="27efe-121">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27efe-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="27efe-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27efe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="27efe-123">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27efe-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="27efe-124">Header</span><span class="sxs-lookup"><span data-stu-id="27efe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="27efe-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="27efe-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="27efe-126">IDL</span><span class="sxs-lookup"><span data-stu-id="27efe-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27efe-127"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27efe-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="27efe-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="27efe-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="27efe-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27efe-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="27efe-130">DLL</span><span class="sxs-lookup"><span data-stu-id="27efe-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27efe-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27efe-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="27efe-132">IID</span><span class="sxs-lookup"><span data-stu-id="27efe-132">IID</span></span><br/>                      | <span data-ttu-id="27efe-133">IID_IDeliveryOptimizationJob ist als EE2584CF-A69C-4848-B633-2649962b3ef7 definiert.</span><span class="sxs-lookup"><span data-stu-id="27efe-133">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



 

