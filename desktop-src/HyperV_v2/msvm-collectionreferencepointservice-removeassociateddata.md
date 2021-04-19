---
description: Entfernt das dem Bezugspunkt zugeordnete Datenprotokoll.
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Removeassociateddata-Methode der Msvm_CollectionReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aec1ac249616c08c6abf1f156ad5a3416c8afaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359491"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="789c5-103">Removeassociateddata-Methode der MSVM \_ collectionreferencepointservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="789c5-103">RemoveAssociatedData method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="789c5-104">Entfernt das dem Bezugspunkt zugeordnete Datenprotokoll.</span><span class="sxs-lookup"><span data-stu-id="789c5-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="789c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="789c5-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="789c5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="789c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="789c5-107">*Affectedreferencepointcollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="789c5-107">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="789c5-108">Verweis auf die betroffene Verweis Punkt Auflistung des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="789c5-108">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="789c5-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="789c5-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="789c5-110">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="789c5-110">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="789c5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="789c5-111">Return value</span></span>

<span data-ttu-id="789c5-112">Wenn erfolgreich, wird entweder 0 (kein Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="789c5-112">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="789c5-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="789c5-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="789c5-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-115">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="789c5-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="789c5-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-117">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="789c5-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-118">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="789c5-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-119">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="789c5-119">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-120">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="789c5-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-121">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="789c5-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-122">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="789c5-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="789c5-123">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="789c5-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="789c5-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="789c5-124">Requirements</span></span>



| <span data-ttu-id="789c5-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="789c5-125">Requirement</span></span> | <span data-ttu-id="789c5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="789c5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="789c5-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="789c5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="789c5-128">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="789c5-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="789c5-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="789c5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="789c5-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="789c5-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="789c5-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="789c5-131">Namespace</span></span><br/>                | <span data-ttu-id="789c5-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="789c5-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="789c5-133">MOF</span><span class="sxs-lookup"><span data-stu-id="789c5-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="789c5-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="789c5-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="789c5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="789c5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="789c5-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="789c5-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="789c5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="789c5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789c5-138">**MSVM \_ collectionreferencepointservice**</span><span class="sxs-lookup"><span data-stu-id="789c5-138">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




