---
title: Ideliveryoptimizationfile-Schnittstelle
description: Implementieren Sie die ideliveryoptimizationfile-Schnittstelle, um den Status einer bestimmten Datei zu identifizieren.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Ideliveryoptimizationfile-Schnittstelle
- Ideliveryoptimizationfile-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341790"
---
# <a name="ideliveryoptimizationfile-interface"></a><span data-ttu-id="20ed5-105">Ideliveryoptimizationfile-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="20ed5-105">IDeliveryOptimizationFile interface</span></span>

<span data-ttu-id="20ed5-106">Implementieren Sie die **ideliveryoptimizationfile** -Schnittstelle, um den Status einer bestimmten Datei zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="20ed5-106">Implement the **IDeliveryOptimizationFile** interface to identify the status of a specific file.</span></span>

## <a name="members"></a><span data-ttu-id="20ed5-107">Member</span><span class="sxs-lookup"><span data-stu-id="20ed5-107">Members</span></span>

<span data-ttu-id="20ed5-108">Die **ideliveryoptimizationfile** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="20ed5-108">The **IDeliveryOptimizationFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="20ed5-109">**Ideliveryoptimizationfile** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="20ed5-109">**IDeliveryOptimizationFile** also has these types of members:</span></span>

-   [<span data-ttu-id="20ed5-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="20ed5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="20ed5-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="20ed5-111">Methods</span></span>

<span data-ttu-id="20ed5-112">Die **ideliveryoptimizationfile** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="20ed5-112">The **IDeliveryOptimizationFile** interface has these methods.</span></span>



| <span data-ttu-id="20ed5-113">Methode</span><span class="sxs-lookup"><span data-stu-id="20ed5-113">Method</span></span>                                                 | <span data-ttu-id="20ed5-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20ed5-114">Description</span></span>                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="20ed5-115">**GetStats**</span><span class="sxs-lookup"><span data-stu-id="20ed5-115">**GetStats**</span></span>](ideliveryoptimizationfile-getstats.md) | <span data-ttu-id="20ed5-116">Gibt die Statistiken zum herunterladen und Hochladen für eine bestimmte Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="20ed5-116">Returns download and upload stats for a specific file.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="20ed5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20ed5-117">Requirements</span></span>

| <span data-ttu-id="20ed5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20ed5-118">Requirement</span></span> | <span data-ttu-id="20ed5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="20ed5-119">Value</span></span> |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20ed5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20ed5-120">Minimum supported client</span></span>      | <span data-ttu-id="20ed5-121">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20ed5-121">Windows 10, version 1709 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="20ed5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20ed5-122">Minimum supported server</span></span>      | <span data-ttu-id="20ed5-123">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20ed5-123">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="20ed5-124">Header</span><span class="sxs-lookup"><span data-stu-id="20ed5-124">Header</span></span>                        | <span data-ttu-id="20ed5-125">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="20ed5-125">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="20ed5-126">IDL</span><span class="sxs-lookup"><span data-stu-id="20ed5-126">IDL</span></span>                           | <span data-ttu-id="20ed5-127">Deliveryoptimization. idl</span><span class="sxs-lookup"><span data-stu-id="20ed5-127">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="20ed5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="20ed5-128">Library</span></span>                       | <span data-ttu-id="20ed5-129">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="20ed5-129">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="20ed5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="20ed5-130">DLL</span></span>                           | <span data-ttu-id="20ed5-131">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="20ed5-131">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="20ed5-132">IID</span><span class="sxs-lookup"><span data-stu-id="20ed5-132">IID</span></span>                           | <span data-ttu-id="20ed5-133">IID_IDeliveryOptimizationFile ist als B76B9699-E99E-4101-803F-A20E325D93E2 definiert.</span><span class="sxs-lookup"><span data-stu-id="20ed5-133">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span> |
