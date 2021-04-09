---
description: Durchsucht den angegebenen Ordner nach allen Momentaufnahme Definitions Dateien, die dem angegebenen geplanten Computersystem zugeordnet sind, und erstellt eine neue Momentaufnahme auf dem geplanten Computersystem für jede zugeordnete Definitionsdatei an diesem Speicherort.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Importsnapshotdefinitions-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9ebb36b030786ab88eab899190afcc7f3022286a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863571"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7cbbf-103">Importsnapshotdefinitions-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="7cbbf-103">ImportSnapshotDefinitions method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7cbbf-104">Durchsucht den angegebenen Ordner nach allen Momentaufnahme Definitions Dateien, die dem angegebenen geplanten Computersystem zugeordnet sind, und erstellt eine neue Momentaufnahme auf dem geplanten Computersystem für jede zugeordnete Definitionsdatei an diesem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="7cbbf-104">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbbf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cbbf-105">Syntax</span></span>


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7cbbf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cbbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cbbf-107">*Plannedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cbbf-107">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbbf-108">Ein Verweis auf ein [**MSVM- \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Objekt, das die geplante virtuelle Maschine darstellt, die auf die zu importierenden Momentaufnahmen verweist.</span><span class="sxs-lookup"><span data-stu-id="7cbbf-108">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned virtual machine which references the snapshots to be imported.</span></span>

</dd> <dt>

<span data-ttu-id="7cbbf-109">*Snapshotfolder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cbbf-109">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbbf-110">Der voll qualifizierte Pfad zum Ordner, in dem die Momentaufnahme Konfigurationen für diesen virtuellen Computer gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="7cbbf-110">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span>

</dd> <dt>

<span data-ttu-id="7cbbf-111">*Importedmomentaufnahmen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7cbbf-111">*ImportedSnapshots* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbbf-112">Wenn der Vorgang synchron abgeschlossen wird, ein Array von Verweisen auf die [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Instanzen, die die Momentaufnahmen darstellen, die erfolgreich importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7cbbf-112">If the operation completes synchronously, an array of references to the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances representing the snapshots which were successfully imported.</span></span>

</dd> <dt>

<span data-ttu-id="7cbbf-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7cbbf-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbbf-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7cbbf-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cbbf-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7cbbf-115">Return value</span></span>

<span data-ttu-id="7cbbf-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7cbbf-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7cbbf-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="7cbbf-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="7cbbf-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="7cbbf-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="7cbbf-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="7cbbf-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="7cbbf-130">**Verwendete Datei** (32779)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-130">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7cbbf-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cbbf-131">Requirements</span></span>



| <span data-ttu-id="7cbbf-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cbbf-132">Requirement</span></span> | <span data-ttu-id="7cbbf-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7cbbf-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbbf-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7cbbf-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cbbf-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7cbbf-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7cbbf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7cbbf-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cbbf-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7cbbf-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="7cbbf-138">Namespace</span></span><br/>                | <span data-ttu-id="7cbbf-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7cbbf-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7cbbf-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7cbbf-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cbbf-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7cbbf-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cbbf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7cbbf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cbbf-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7cbbf-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7cbbf-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cbbf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cbbf-145">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="7cbbf-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

