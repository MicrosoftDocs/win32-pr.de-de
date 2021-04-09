---
description: Konvertiert eine vorhandene Auflistungs Momentaufnahme in eine Verweis Punkt Auflistung. Die Momentaufnahme Auflistung wird als Nebeneffekt gelöscht. Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Converttoreferencepoint-Methode der Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869084"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="bc746-105">Converttoreferencepoint-Methode der MSVM \_ collectionsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="bc746-105">ConvertToReferencePoint method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="bc746-106">Konvertiert eine vorhandene Auflistungs Momentaufnahme in eine Verweis Punkt Auflistung.</span><span class="sxs-lookup"><span data-stu-id="bc746-106">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="bc746-107">Die Momentaufnahme Auflistung wird als Nebeneffekt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bc746-107">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="bc746-108">Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="bc746-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc746-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc746-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bc746-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc746-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc746-111">*Affectedsnapshotcollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc746-111">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc746-112">Verweis auf eine [**MSVM- \_ snapshotcollection**](msvm-snapshotcollection.md) , die die betroffene Sammlung virtueller System Momentaufnahmen enthält.</span><span class="sxs-lookup"><span data-stu-id="bc746-112">Reference to a [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) containing the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="bc746-113">*Resultingreferencepointcollection* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc746-113">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc746-114">Verweis auf eine [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) , die die resultierende Verweis Punkt Auflistung des virtuellen Systems enthält</span><span class="sxs-lookup"><span data-stu-id="bc746-114">Reference to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) containing the resulting virtual system reference point collection</span></span>

</dd> <dt>

<span data-ttu-id="bc746-115">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc746-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc746-116">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc746-116">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc746-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc746-117">Return value</span></span>

<span data-ttu-id="bc746-118">Bei Erfolg wird entweder 0 (abgeschlossen) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc746-118">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="bc746-119">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="bc746-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-120">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="bc746-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-121">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="bc746-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-122">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="bc746-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-123">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="bc746-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-124">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="bc746-124">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-125">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="bc746-125">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-126">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="bc746-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-127">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="bc746-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-128">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="bc746-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="bc746-129">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="bc746-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bc746-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc746-130">Requirements</span></span>



| <span data-ttu-id="bc746-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc746-131">Requirement</span></span> | <span data-ttu-id="bc746-132">Wert</span><span class="sxs-lookup"><span data-stu-id="bc746-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc746-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc746-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bc746-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc746-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bc746-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc746-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bc746-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bc746-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bc746-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc746-137">Namespace</span></span><br/>                | <span data-ttu-id="bc746-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bc746-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc746-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bc746-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc746-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bc746-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc746-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bc746-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc746-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc746-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc746-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc746-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc746-144">**MSVM \_ collectionsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="bc746-144">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




