---
description: Ruft Informationen zu einer VHD-Momentaufnahme in einer VHD-Datei ab.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Getvhdsnapshotinformation-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347805"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="f16cc-103">Getvhdsnapshotinformation-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="f16cc-103">GetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="f16cc-104">Ruft Informationen zu einer VHD-Momentaufnahme in einer VHD-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="f16cc-104">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f16cc-105">Syntax</span></span>


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f16cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f16cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f16cc-107">*Vhdsetpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f16cc-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16cc-108">Ein voll qualifizierter Pfad, der den Speicherort der VHD-Satz Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="f16cc-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="f16cc-109">*Snapshotids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f16cc-109">*SnapshotIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16cc-110">Eine Liste von GUIDs, die die Momentaufnahme-IDs der einzelnen Momentaufnahmen darstellen, für die Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f16cc-110">A list of GUIDs representing the Snapshot Ids of each Snapshot for which information is being requested.</span></span> <span data-ttu-id="f16cc-111">Wenn dieser Parameter NULL ist, werden Informationen für alle Momentaufnahmen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f16cc-111">If this parameter is NULL, information for all Snapshots will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="f16cc-112">*AdditionalInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f16cc-112">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16cc-113">Ein Array, das angibt, welche zusätzlichen Informationen zu den einzelnen VHD-Momentaufnahmen gesammelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f16cc-113">An array specifying what additional information should be gathered about each VHD Snapshot.</span></span> <span data-ttu-id="f16cc-114">Jeder Eintrag im Array ist ein Typ zusätzlicher Informationen.</span><span class="sxs-lookup"><span data-stu-id="f16cc-114">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="f16cc-115">Wenn dieser Parameter NULL ist, werden keine zusätzlichen Informationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f16cc-115">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f16cc-116">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f16cc-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f16cc-117">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f16cc-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

<span data-ttu-id="f16cc-118">Über **geordnete Pfade** (2)</span><span class="sxs-lookup"><span data-stu-id="f16cc-118">**Parent Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f16cc-119">*Snapshotinformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f16cc-119">*SnapshotInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f16cc-120">Bei erfolgreicher Ausführung ein Array von Informationen über die einzelnen angeforderten Momentaufnahmen.</span><span class="sxs-lookup"><span data-stu-id="f16cc-120">If successful, an array of information about each requested snapshot.</span></span> <span data-ttu-id="f16cc-121">Jedes Element ist eine eingebettete Instanz von [**MSVM \_ vhdsnapshotinformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="f16cc-121">Each element is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="f16cc-122">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f16cc-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f16cc-123">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="f16cc-123">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f16cc-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f16cc-124">Return value</span></span>

<span data-ttu-id="f16cc-125">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="f16cc-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f16cc-126">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="f16cc-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-127">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="f16cc-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-128">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="f16cc-128">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-129">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="f16cc-129">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-130">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="f16cc-130">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-131">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="f16cc-131">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-132">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="f16cc-132">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-133">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="f16cc-133">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-134">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="f16cc-134">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-135">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="f16cc-135">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-136">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="f16cc-136">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-137">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="f16cc-137">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-138">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="f16cc-138">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f16cc-139">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="f16cc-139">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f16cc-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f16cc-140">Requirements</span></span>



| <span data-ttu-id="f16cc-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f16cc-141">Requirement</span></span> | <span data-ttu-id="f16cc-142">Wert</span><span class="sxs-lookup"><span data-stu-id="f16cc-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f16cc-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f16cc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f16cc-144">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f16cc-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f16cc-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f16cc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f16cc-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f16cc-146">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f16cc-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="f16cc-147">Namespace</span></span><br/>                | <span data-ttu-id="f16cc-148">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f16cc-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f16cc-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f16cc-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f16cc-150"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f16cc-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f16cc-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f16cc-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f16cc-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f16cc-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f16cc-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f16cc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16cc-154">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="f16cc-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




