---
description: Erstellt ein neues geplantes Computersystem basierend auf der angegebenen Definition der virtuellen Maschine.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Importsystemdefinition-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354596"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="10f84-103">Importsystemdefinition-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="10f84-103">ImportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="10f84-104">Erstellt ein neues geplantes Computersystem basierend auf der angegebenen Definition der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="10f84-104">Creates a new planned computer system based on the specified virtual machine definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10f84-105">Syntax</span></span>


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="10f84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10f84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10f84-107">*SystemDefinitionFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10f84-107">*SystemDefinitionFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10f84-108">Der voll qualifizierte Pfad zur System Definitionsdatei (. XML oder. exp), die den zu importierenden virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="10f84-108">The fully qualified path to the system definition file (.xml or .exp) representing the virtual machine which is to be imported.</span></span> <span data-ttu-id="10f84-109">Die Definitionsdatei darf nicht bereits vom Host System oder der Virtualisierungsplattform verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10f84-109">The definition file must not already be in use by the host system or the virtualization platform.</span></span>

</dd> <dt>

<span data-ttu-id="10f84-110">*Snapshotfolder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10f84-110">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10f84-111">Der voll qualifizierte Pfad zum Ordner, in dem die Momentaufnahme Konfigurationen für diesen virtuellen Computer gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="10f84-111">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span> <span data-ttu-id="10f84-112">Dieser Ordner wird durchsucht, um Momentaufnahmen zu finden, auf die in der Definition der virtuellen Maschine verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="10f84-112">This folder will be searched in order to locate any snapshots referenced by the virtual machine definition.</span></span> <span data-ttu-id="10f84-113">Alle referenzierten Momentaufnahmen, die an diesem Speicherort nicht gefunden werden, müssen mithilfe der [**destroysnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) -Methode gelöscht oder mithilfe der [**importsnapshotdefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) -Methode importiert werden, bevor das geplante Computersystem erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="10f84-113">Any referenced snapshots not found in this location must be deleted using the [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) method, or imported using the [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) method prior to realizing the planned computer system.</span></span>

</dd> <dt>

<span data-ttu-id="10f84-114">*Generatenewsystematidentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10f84-114">*GenerateNewSystemIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10f84-115">Gibt an, ob der eindeutige Bezeichner für den virtuellen Computer wieder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10f84-115">Indicates whether to reuse the unique identifier for the virtual machine.</span></span> <span data-ttu-id="10f84-116">Wenn dieser Parameter **true** ist, wird ein neuer System Bezeichner generiert.</span><span class="sxs-lookup"><span data-stu-id="10f84-116">If this parameter is **True**, then a new system identifier is generated.</span></span> <span data-ttu-id="10f84-117">Wenn dieser Parameter **false** ist, wird der vorhandene System Bezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="10f84-117">If this parameter is **False**, then the existing system identifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="10f84-118">*Importedsystem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="10f84-118">*ImportedSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10f84-119">Wenn der Vorgang synchron abgeschlossen wird, ein Verweis auf ein [**MSVM \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Objekt, das den importierten virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="10f84-119">If the operation completes synchronously, a reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the imported virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="10f84-120">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="10f84-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10f84-121">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="10f84-121">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10f84-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10f84-122">Return value</span></span>

<span data-ttu-id="10f84-123">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="10f84-123">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="10f84-124">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="10f84-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-125">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="10f84-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-126">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="10f84-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-127">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="10f84-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-128">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="10f84-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-129">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="10f84-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-130">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="10f84-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-131">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="10f84-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-132">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="10f84-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-133">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="10f84-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-134">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="10f84-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-135">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="10f84-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-136">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="10f84-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="10f84-137">**Verwendete Datei** (32779)</span><span class="sxs-lookup"><span data-stu-id="10f84-137">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="10f84-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10f84-138">Requirements</span></span>



| <span data-ttu-id="10f84-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10f84-139">Requirement</span></span> | <span data-ttu-id="10f84-140">Wert</span><span class="sxs-lookup"><span data-stu-id="10f84-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f84-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10f84-141">Minimum supported client</span></span><br/> | <span data-ttu-id="10f84-142">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10f84-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="10f84-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10f84-143">Minimum supported server</span></span><br/> | <span data-ttu-id="10f84-144">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10f84-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10f84-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="10f84-145">Namespace</span></span><br/>                | <span data-ttu-id="10f84-146">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="10f84-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="10f84-147">MOF</span><span class="sxs-lookup"><span data-stu-id="10f84-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10f84-148"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="10f84-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10f84-149">DLL</span><span class="sxs-lookup"><span data-stu-id="10f84-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10f84-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10f84-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="10f84-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10f84-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f84-152">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="10f84-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

