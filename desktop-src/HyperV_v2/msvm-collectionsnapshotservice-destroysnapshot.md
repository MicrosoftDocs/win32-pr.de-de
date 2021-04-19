---
description: Zerstört eine vorhandene Momentaufnahme der virtuellen System Auflistung. Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Destroysnapshot-Methode der Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 399737a95db7725718b2e0ec620d2b6b7a7ae93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345855"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="12bec-104">Destroysnapshot-Methode der MSVM \_ collectionsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="12bec-104">DestroySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="12bec-105">Zerstört eine vorhandene Momentaufnahme der virtuellen System Auflistung.</span><span class="sxs-lookup"><span data-stu-id="12bec-105">Destroys an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="12bec-106">Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="12bec-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="12bec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="12bec-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="12bec-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="12bec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12bec-109">*Affectedsnapshotcollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12bec-109">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12bec-110">Verweis auf eine [**CIM \_**](cim-collection.md) -Auflistung, die die betroffene Sammlung virtueller System Momentaufnahmen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="12bec-110">Reference to a [**CIM\_Collection**](cim-collection.md) that describes the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="12bec-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12bec-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12bec-112">Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12bec-112">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="12bec-113">Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ concretejob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="12bec-113">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12bec-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12bec-114">Return value</span></span>

<span data-ttu-id="12bec-115">Bei Erfolg wird entweder 0 (abgeschlossen) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="12bec-115">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="12bec-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="12bec-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="12bec-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-118">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="12bec-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="12bec-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-120">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="12bec-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-121">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="12bec-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-122">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="12bec-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="12bec-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="12bec-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="12bec-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="12bec-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="12bec-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="12bec-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12bec-127">Requirements</span></span>



| <span data-ttu-id="12bec-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12bec-128">Requirement</span></span> | <span data-ttu-id="12bec-129">Wert</span><span class="sxs-lookup"><span data-stu-id="12bec-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12bec-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12bec-130">Minimum supported client</span></span><br/> | <span data-ttu-id="12bec-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12bec-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="12bec-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12bec-132">Minimum supported server</span></span><br/> | <span data-ttu-id="12bec-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="12bec-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="12bec-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="12bec-134">Namespace</span></span><br/>                | <span data-ttu-id="12bec-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="12bec-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="12bec-136">MOF</span><span class="sxs-lookup"><span data-stu-id="12bec-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12bec-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="12bec-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12bec-138">DLL</span><span class="sxs-lookup"><span data-stu-id="12bec-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12bec-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12bec-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12bec-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12bec-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12bec-141">**MSVM \_ collectionsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="12bec-141">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




