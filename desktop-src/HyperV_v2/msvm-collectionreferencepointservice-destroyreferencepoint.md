---
description: Zerstört eine vorhandene Verweis Punkt Auflistung. Diese Methode kann als Nebeneffekt andere Verweis Punkte zerstören, die von der betroffenen Verweis Punkt Auflistung abhängig sind.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Destroyreferencepoint-Methode der Msvm_CollectionReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132016"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="3554a-104">Destroyreferencepoint-Methode der MSVM \_ collectionreferencepointservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3554a-104">DestroyReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="3554a-105">Zerstört eine vorhandene Verweis Punkt Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3554a-105">Destroys an existing reference point collection.</span></span> <span data-ttu-id="3554a-106">Diese Methode kann als Nebeneffekt andere Verweis Punkte zerstören, die von der betroffenen Verweis Punkt Auflistung abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="3554a-106">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3554a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3554a-107">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3554a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3554a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3554a-109">*Affectedreferencepointcollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3554a-109">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3554a-110">Verweis auf die betroffene Verweis Punkt Auflistung des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="3554a-110">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="3554a-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3554a-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3554a-112">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3554a-112">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3554a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3554a-113">Return value</span></span>

<span data-ttu-id="3554a-114">Wenn erfolgreich, wird entweder 0 (kein Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3554a-114">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="3554a-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3554a-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-116">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="3554a-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-117">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="3554a-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="3554a-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-119">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="3554a-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-120">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="3554a-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-121">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="3554a-121">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3554a-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3554a-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-124">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="3554a-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3554a-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="3554a-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3554a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3554a-126">Requirements</span></span>



| <span data-ttu-id="3554a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3554a-127">Requirement</span></span> | <span data-ttu-id="3554a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3554a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3554a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3554a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3554a-130">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3554a-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3554a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3554a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3554a-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3554a-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3554a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="3554a-133">Namespace</span></span><br/>                | <span data-ttu-id="3554a-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3554a-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3554a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="3554a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3554a-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3554a-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3554a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3554a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3554a-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3554a-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3554a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3554a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3554a-140">**MSVM \_ collectionreferencepointservice**</span><span class="sxs-lookup"><span data-stu-id="3554a-140">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




