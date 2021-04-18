---
title: IDeliveryOptimizationJob2-Schnittstelle
description: 'Weitere Informationen finden Sie hier: IDeliveryOptimizationJob2-Schnittstelle'
keywords:
- IDeliveryOptimizationJob2-Schnittstelle
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344835"
---
# <a name="ideliveryoptimizationjob2-interface"></a><span data-ttu-id="13f0a-104">IDeliveryOptimizationJob2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="13f0a-104">IDeliveryOptimizationJob2 interface</span></span>

<span data-ttu-id="13f0a-105">Der IDeliveryOptimizationJob2 ermöglicht das Hinzufügen einer einzelnen Datei zum Download Auftrag und das sofortige Abrufen der Datei.</span><span class="sxs-lookup"><span data-stu-id="13f0a-105">The IDeliveryOptimizationJob2 enables adding a single file to the download job, and retrieving the file immediately.</span></span> <span data-ttu-id="13f0a-106">Diese Schnittstelle unterstützt auch das Festlegen und das erhalten Optionaler Auftrags Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13f0a-106">This interface also supports setting and getting optional job properties.</span></span>

## <a name="members"></a><span data-ttu-id="13f0a-107">Member</span><span class="sxs-lookup"><span data-stu-id="13f0a-107">Members</span></span>

<span data-ttu-id="13f0a-108">Die **IDeliveryOptimizationJob2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="13f0a-108">The **IDeliveryOptimizationJob2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="13f0a-109">**IDeliveryOptimizationJob2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="13f0a-109">**IDeliveryOptimizationJob2** also has these types of members:</span></span>

- [<span data-ttu-id="13f0a-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="13f0a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="13f0a-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="13f0a-111">Methods</span></span>

<span data-ttu-id="13f0a-112">Die **IDeliveryOptimizationJob2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="13f0a-112">The **IDeliveryOptimizationJob2** interface has these methods.</span></span>

| <span data-ttu-id="13f0a-113">Methode</span><span class="sxs-lookup"><span data-stu-id="13f0a-113">Method</span></span>                                              | <span data-ttu-id="13f0a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13f0a-114">Description</span></span>                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="13f0a-115">**AddFile**</span><span class="sxs-lookup"><span data-stu-id="13f0a-115">**AddFile**</span></span>](ideliveryoptimizationjob2-addfile.md) | <span data-ttu-id="13f0a-116">Die AddFile-Methode fügt einem vorhandenen do-Auftrag eine einzelne Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="13f0a-116">The AddFile method adds a single file to an existing DO job.</span></span>         |
| [<span data-ttu-id="13f0a-117">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="13f0a-117">**GetProperty**</span></span>](ideliveryoptimizationjob2-getproperty.md) | <span data-ttu-id="13f0a-118">Die AddFile-Methode fügt einem vorhandenen do-Auftrag eine einzelne Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="13f0a-118">The AddFile method adds a single file to an existing DO job.</span></span> |
| [<span data-ttu-id="13f0a-119">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="13f0a-119">**SetProperty**</span></span>](ideliveryoptimizationjob2-setproperty.md) | <span data-ttu-id="13f0a-120">Diese Methode wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="13f0a-120">This method is unused.</span></span>                                       |

## <a name="requirements"></a><span data-ttu-id="13f0a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13f0a-121">Requirements</span></span>

| <span data-ttu-id="13f0a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13f0a-122">Requirement</span></span> | <span data-ttu-id="13f0a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="13f0a-123">Value</span></span> |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="13f0a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13f0a-124">Minimum supported client</span></span> | <span data-ttu-id="13f0a-125">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13f0a-125">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="13f0a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13f0a-126">Minimum supported server</span></span> | <span data-ttu-id="13f0a-127">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13f0a-127">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="13f0a-128">Header</span><span class="sxs-lookup"><span data-stu-id="13f0a-128">Header</span></span>                   | <span data-ttu-id="13f0a-129">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="13f0a-129">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="13f0a-130">IDL</span><span class="sxs-lookup"><span data-stu-id="13f0a-130">IDL</span></span>                      | <span data-ttu-id="13f0a-131">Deliveryoptimization. idl</span><span class="sxs-lookup"><span data-stu-id="13f0a-131">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="13f0a-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13f0a-132">Library</span></span>                  | <span data-ttu-id="13f0a-133">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="13f0a-133">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="13f0a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="13f0a-134">DLL</span></span>                      | <span data-ttu-id="13f0a-135">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="13f0a-135">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="13f0a-136">IID</span><span class="sxs-lookup"><span data-stu-id="13f0a-136">IID</span></span>                      | <span data-ttu-id="13f0a-137">IID_IDeliveryOptimizationJob2 ist als 18995a26-BF 59-4abe-9B-d5092d5a2405 definiert.</span><span class="sxs-lookup"><span data-stu-id="13f0a-137">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |
