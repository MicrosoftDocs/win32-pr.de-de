---
description: Wendet eine Momentaufnahme eines virtuellen Systems auf das virtuelle System an, aus dem die Momentaufnahme erstellt wurde.
ms.assetid: acd90ce0-7f82-48d9-9d23-903ba6815779
title: Applysnapshot-Methode der CIM_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 252f7d7d9a57b439ac00fa663fa0a0e816ebada0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352217"
---
# <a name="applysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="f2286-103">Applysnapshot-Methode der CIM \_ virtualsystemsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="f2286-103">ApplySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="f2286-104">Wendet eine Momentaufnahme eines virtuellen Systems auf das virtuelle System an, aus dem die Momentaufnahme erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2286-104">Applies a virtual system snapshot to the virtual system that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2286-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2286-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f2286-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2286-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2286-107">*Momentaufnahme* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2286-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2286-108">Ein [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Verweis auf die virtuelle System Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="f2286-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="f2286-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f2286-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2286-110">Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2286-110">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="f2286-111">Dieser Parameter war in Windows 8.1 mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f2286-111">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2286-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2286-112">Return value</span></span>

<span data-ttu-id="f2286-113">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2286-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f2286-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="f2286-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="f2286-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="f2286-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="f2286-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="f2286-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="f2286-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-120">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="f2286-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f2286-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-122">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="f2286-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-123">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="f2286-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f2286-124">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="f2286-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f2286-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2286-125">Requirements</span></span>



| <span data-ttu-id="f2286-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2286-126">Requirement</span></span> | <span data-ttu-id="f2286-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f2286-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2286-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2286-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f2286-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f2286-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f2286-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2286-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f2286-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f2286-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f2286-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2286-132">Namespace</span></span><br/>                | <span data-ttu-id="f2286-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f2286-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f2286-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f2286-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2286-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f2286-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2286-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f2286-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2286-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2286-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2286-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2286-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2286-139">**CIM \_ virtualsystemsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="f2286-139">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




