---
description: Ruft eine Liste der Änderungen im angegebenen Bereich eines virtuellen Datenträgers ab, die von der angegebenen robusten Änderungsnachverfolgung ID oder der vhdset-Momentaufnahme-ID bereitgestellt werden.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Getvirtualdiskchanges-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353118"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="6c377-103">Getvirtualdiskchanges-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="6c377-103">GetVirtualDiskChanges method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="6c377-104">Ruft eine Liste der Änderungen im angegebenen Bereich eines virtuellen Datenträgers ab, die von der angegebenen robusten Änderungsnachverfolgung ID oder der vhdset-Momentaufnahme-ID bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c377-104">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c377-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c377-105">Syntax</span></span>


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6c377-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c377-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c377-107">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c377-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c377-108">Ein voll qualifizierter Pfad, der den Speicherort der virtuellen Festplatten Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="6c377-108">A fully-qualified path that specifies the location of the Virtual Hard Disk file.</span></span>

</dd> <dt>

<span data-ttu-id="6c377-109">*Limitid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c377-109">*LimitId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c377-110">Eine robuste Änderungsnachverfolgung ID oder eine Momentaufnahme-ID des VHD-Satzes, die die Baseline für Änderungen auf dem virtuellen Datenträger angibt.</span><span class="sxs-lookup"><span data-stu-id="6c377-110">A Resilient Change Tracking Id or VHD Set Snapshot Id indicating the baseline for changes in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="6c377-111">*Targetinapshotid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c377-111">*TargetSnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c377-112">Eine vhdset-Momentaufnahme-ID, die die Momentaufnahme angibt, die beim determinimieren der virtuellen Festplatte mit der Baseline verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c377-112">A VHDSet Snapshot Id indicating the snapshot to compare to the baseline when determing changes in the virtual hard disk.</span></span> <span data-ttu-id="6c377-113">Dieser Parameter ist nur für VHD-Set-Dateien gültig.</span><span class="sxs-lookup"><span data-stu-id="6c377-113">This parameter is only valid for VHD Set files.</span></span>

</dd> <dt>

<span data-ttu-id="6c377-114">*Byteoffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c377-114">*ByteOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c377-115">Der Byte Offset der Region im virtuellen Datenträger, für die Änderungen abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c377-115">The byte offset of the region in the virtual disk to query changes for.</span></span>

</dd> <dt>

<span data-ttu-id="6c377-116">*ByteLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c377-116">*ByteLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c377-117">Die Byte Länge der Region im virtuellen Datenträger, für die Änderungen abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c377-117">The byte length of the region in the virtual disk to query changes for.</span></span> <span data-ttu-id="6c377-118">Diese muss kleiner als die Größe des virtuellen Datenträgers sein.</span><span class="sxs-lookup"><span data-stu-id="6c377-118">This must be less than the size of the Virtual Disk.</span></span>

</dd> <dt>

<span data-ttu-id="6c377-119">*Processedbytelength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c377-119">*ProcessedByteLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c377-120">Die gesamte Byte Länge, die verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="6c377-120">The total byte length that was processed.</span></span> <span data-ttu-id="6c377-121">Dieser Wert kann gleich ByteLength oder kleiner sein.</span><span class="sxs-lookup"><span data-stu-id="6c377-121">This may be equal to ByteLength or less.</span></span>

</dd> <dt>

<span data-ttu-id="6c377-122">*Changedbyteoffsets* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c377-122">*ChangedByteOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c377-123">Die Liste der Byte Offsets in der virtuellen Festplatte, die den Anfang jedes geänderten Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="6c377-123">The list of byte offsets into the virtual disk indicating the beginning of each changed range.</span></span>

</dd> <dt>

<span data-ttu-id="6c377-124">*Changedbytelengths* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c377-124">*ChangedByteLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c377-125">Die Liste der Byte Längen der geänderten Bereiche auf dem virtuellen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="6c377-125">The list of byte lengths of the changed ranges in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="6c377-126">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c377-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c377-127">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="6c377-127">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c377-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c377-128">Return value</span></span>

<span data-ttu-id="6c377-129">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="6c377-129">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6c377-130">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="6c377-130">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-131">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="6c377-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-132">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="6c377-132">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-133">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="6c377-133">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-134">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="6c377-134">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-135">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="6c377-135">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-136">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="6c377-136">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-137">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="6c377-137">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-138">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="6c377-138">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-139">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="6c377-139">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-140">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="6c377-140">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-141">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="6c377-141">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-142">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="6c377-142">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6c377-143">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="6c377-143">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6c377-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c377-144">Requirements</span></span>



| <span data-ttu-id="6c377-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c377-145">Requirement</span></span> | <span data-ttu-id="6c377-146">Wert</span><span class="sxs-lookup"><span data-stu-id="6c377-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c377-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c377-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6c377-148">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c377-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6c377-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c377-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6c377-150">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6c377-150">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6c377-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c377-151">Namespace</span></span><br/>                | <span data-ttu-id="6c377-152">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6c377-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6c377-153">MOF</span><span class="sxs-lookup"><span data-stu-id="6c377-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c377-154"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6c377-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c377-155">DLL</span><span class="sxs-lookup"><span data-stu-id="6c377-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c377-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c377-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c377-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c377-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c377-158">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="6c377-158">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




