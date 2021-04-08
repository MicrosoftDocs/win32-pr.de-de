---
description: Zerstört eine vorhandene Momentaufnahme eines virtuellen Computers.
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: Destroysnapshot-Methode der Msvm_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 91c2e59baa8bb22f5ea9f128130d7dc440e28ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868231"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="d615e-103">Destroysnapshot-Methode der MSVM \_ virtualsystemsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="d615e-103">DestroySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="d615e-104">Zerstört eine vorhandene Momentaufnahme eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d615e-104">Destroys an existing virtual machine snapshot.</span></span> <span data-ttu-id="d615e-105">Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d615e-105">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="d615e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d615e-106">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d615e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d615e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d615e-108">*Affectedsnapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d615e-108">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d615e-109">Ein [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Verweis, der die zu löschender Momentaufnahme des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="d615e-109">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="d615e-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d615e-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d615e-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="d615e-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d615e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d615e-112">Return value</span></span>

<span data-ttu-id="d615e-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="d615e-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d615e-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="d615e-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="d615e-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="d615e-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="d615e-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="d615e-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="d615e-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-120">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="d615e-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="d615e-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-122">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="d615e-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-123">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="d615e-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d615e-124">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="d615e-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d615e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d615e-125">Requirements</span></span>



| <span data-ttu-id="d615e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d615e-126">Requirement</span></span> | <span data-ttu-id="d615e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d615e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d615e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d615e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d615e-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d615e-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d615e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d615e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d615e-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d615e-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d615e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="d615e-132">Namespace</span></span><br/>                | <span data-ttu-id="d615e-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d615e-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d615e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d615e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d615e-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d615e-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d615e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d615e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d615e-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d615e-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d615e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d615e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d615e-139">**MSVM \_ virtualsystemsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="d615e-139">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="d615e-140">**Removevirtualsystemsnapshot (v1)**</span><span class="sxs-lookup"><span data-stu-id="d615e-140">**RemoveVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

