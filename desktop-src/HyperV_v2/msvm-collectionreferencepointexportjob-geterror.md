---
description: Ruft einen Fehler ab.
ms.assetid: 7c47acae-d398-4698-81db-e3c8a812f339
title: GetError-Methode der Msvm_CollectionReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ea92bd08a2b65466d11e41bb459200610a89677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050398"
---
# <a name="geterror-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="3002a-103">GetError-Methode der MSVM \_ collectionreferencepointexportjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="3002a-103">GetError method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="3002a-104">Ruft einen Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="3002a-104">Retrieves an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="3002a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3002a-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="3002a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3002a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3002a-107">*Fehler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3002a-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3002a-108">Bei Erfolg enthält eine Beschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="3002a-108">On success, contains a description of the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3002a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3002a-109">Return value</span></span>

<span data-ttu-id="3002a-110">0 bei Erfolg; andernfalls ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="3002a-110">0 on success; otherwise, an error.</span></span>

<dl> <dt>

<span data-ttu-id="3002a-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3002a-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-112">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="3002a-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-113">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3002a-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-114">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3002a-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-115">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="3002a-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-116">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3002a-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-117">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="3002a-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-118">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="3002a-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-119">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="3002a-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-120">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="3002a-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-121">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="3002a-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3002a-122">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="3002a-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3002a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3002a-123">Requirements</span></span>



| <span data-ttu-id="3002a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3002a-124">Requirement</span></span> | <span data-ttu-id="3002a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3002a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3002a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3002a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3002a-127">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3002a-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3002a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3002a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3002a-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3002a-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3002a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="3002a-130">Namespace</span></span><br/>                | <span data-ttu-id="3002a-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3002a-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3002a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="3002a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3002a-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3002a-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3002a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3002a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3002a-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3002a-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3002a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3002a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3002a-137">**MSVM \_ collectionreferencepointexportjob**</span><span class="sxs-lookup"><span data-stu-id="3002a-137">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




