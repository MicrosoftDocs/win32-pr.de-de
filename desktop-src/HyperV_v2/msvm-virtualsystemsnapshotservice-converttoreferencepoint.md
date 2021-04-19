---
description: Konvertieren einer vorhandenen Momentaufnahme eines virtuellen Systems in einen Referenzpunkt Die Momentaufnahme wird als Nebeneffekt gelöscht. Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Converttoreferencepoint-Methode der Msvm_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346491"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="71298-105">Converttoreferencepoint-Methode der MSVM \_ virtualsystemsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="71298-105">ConvertToReferencePoint method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="71298-106">Konvertieren einer vorhandenen Momentaufnahme eines virtuellen Systems in einen Referenzpunkt</span><span class="sxs-lookup"><span data-stu-id="71298-106">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="71298-107">Die Momentaufnahme wird als Nebeneffekt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="71298-107">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="71298-108">Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="71298-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="71298-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="71298-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="71298-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="71298-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71298-111">*Affectedsnapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71298-111">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71298-112">Verweis auf die betroffene virtuelle System Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="71298-112">Reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="71298-113">*Referencepointsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71298-113">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71298-114">Parameter Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="71298-114">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="71298-115">*Resultingreferencepoint* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="71298-115">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="71298-116">Resultierender virtueller System-Referenzpunkt</span><span class="sxs-lookup"><span data-stu-id="71298-116">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="71298-117">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="71298-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71298-118">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="71298-118">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71298-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71298-119">Return value</span></span>

<span data-ttu-id="71298-120">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird einer der folgenden Werte zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="71298-120">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="71298-121">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="71298-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="71298-122">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="71298-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="71298-123">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="71298-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="71298-124">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="71298-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="71298-125">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="71298-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="71298-126">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="71298-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="71298-127">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="71298-127">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="71298-128">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="71298-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="71298-129">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="71298-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="71298-130">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="71298-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="71298-131">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="71298-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="71298-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71298-132">Requirements</span></span>



| <span data-ttu-id="71298-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71298-133">Requirement</span></span> | <span data-ttu-id="71298-134">Wert</span><span class="sxs-lookup"><span data-stu-id="71298-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71298-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71298-135">Minimum supported client</span></span><br/> | <span data-ttu-id="71298-136">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71298-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="71298-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71298-137">Minimum supported server</span></span><br/> | <span data-ttu-id="71298-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="71298-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="71298-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="71298-139">Namespace</span></span><br/>                | <span data-ttu-id="71298-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="71298-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="71298-141">MOF</span><span class="sxs-lookup"><span data-stu-id="71298-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71298-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="71298-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71298-143">DLL</span><span class="sxs-lookup"><span data-stu-id="71298-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71298-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71298-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="71298-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71298-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71298-146">**MSVM \_ virtualsystemsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="71298-146">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




