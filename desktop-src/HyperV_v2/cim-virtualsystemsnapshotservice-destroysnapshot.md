---
description: Zerstört eine vorhandene Momentaufnahme eines virtuellen Systems. Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Destroysnapshot-Methode der CIM_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80d618374d2da4a12f2ce31284d7b3fa36ba65ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526774"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="5af73-104">Destroysnapshot-Methode der CIM \_ virtualsystemsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="5af73-104">DestroySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="5af73-105">Zerstört eine vorhandene Momentaufnahme eines virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="5af73-105">Destroy an existing virtual system snapshot.</span></span> <span data-ttu-id="5af73-106">Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5af73-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af73-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5af73-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5af73-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5af73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af73-109">*Affectedsnapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5af73-109">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af73-110">Ein [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Verweis auf die betroffene virtuelle System Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="5af73-110">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5af73-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5af73-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5af73-112">Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="5af73-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="5af73-113">Dieser Parameter war in Windows 8.1 mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5af73-113">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af73-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5af73-114">Return value</span></span>

<span data-ttu-id="5af73-115">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5af73-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5af73-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="5af73-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="5af73-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-118">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="5af73-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="5af73-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-120">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="5af73-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-121">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="5af73-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-122">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="5af73-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="5af73-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="5af73-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="5af73-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5af73-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="5af73-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5af73-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5af73-127">Requirements</span></span>



| <span data-ttu-id="5af73-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5af73-128">Requirement</span></span> | <span data-ttu-id="5af73-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5af73-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af73-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5af73-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5af73-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5af73-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5af73-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5af73-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5af73-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5af73-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5af73-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="5af73-134">Namespace</span></span><br/>                | <span data-ttu-id="5af73-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5af73-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5af73-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5af73-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5af73-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5af73-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5af73-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5af73-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af73-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5af73-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5af73-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5af73-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af73-141">**CIM \_ virtualsystemsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="5af73-141">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




