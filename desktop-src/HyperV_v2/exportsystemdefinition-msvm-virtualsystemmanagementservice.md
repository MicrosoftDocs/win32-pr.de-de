---
description: Exportiert einen virtuellen Computer oder eine Momentaufnahme eines virtuellen Computers in eine Datei.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Exportsystemdefinition-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749640"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="87a4d-103">Exportsystemdefinition-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="87a4d-103">ExportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="87a4d-104">Exportiert einen virtuellen Computer oder eine Momentaufnahme eines virtuellen Computers in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="87a4d-104">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span> <span data-ttu-id="87a4d-105">Der virtuelle Computer muss sich im Zustand "ausgeschaltet" oder "gespeichert" befinden, um exportiert werden zu können.</span><span class="sxs-lookup"><span data-stu-id="87a4d-105">The virtual machine must be in the "powered off" or "saved" state to be exported.</span></span> <span data-ttu-id="87a4d-106">Der virtuelle Computer, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen werden in der resultierenden Datei beibehalten.</span><span class="sxs-lookup"><span data-stu-id="87a4d-106">The virtual machine, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a4d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="87a4d-107">Syntax</span></span>


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="87a4d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="87a4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a4d-109">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87a4d-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87a4d-110">Ein Verweis auf ein [**CIM- \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , das den zu exportierenden virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="87a4d-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="87a4d-111">*Exportdirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87a4d-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87a4d-112">Der voll qualifizierte Pfad des Verzeichnisses, in das der virtuelle Computer exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="87a4d-112">The fully qualified path of the directory to which the virtual machine is to be exported.</span></span> <span data-ttu-id="87a4d-113">Wenn die Eigenschaft " **kreatevmexportsubdirectory** " der [**MSVM-Klasse " \_ virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md) " im Parameter " *exportsettingdata* " auf " **true**" festgelegt ist, kann dieses Verzeichnis für den Export mehrerer virtueller Computer wieder verwendet werden, und diese Methode platziert die Definitionen der virtuellen Maschinen in einem separaten Unterverzeichnis unter diesem Pfad.</span><span class="sxs-lookup"><span data-stu-id="87a4d-113">If the **CreateVmExportSubdirectory** property of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class in the *ExportSettingData* parameter is set to **True**, then this directory can be reused for exporting multiple virtual machines and this method places each virtual machine definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="87a4d-114">*Exportsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87a4d-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87a4d-115">Eine eingebettete Instanz der [**MSVM \_ virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md) -Klasse, die die Einstellungen für den Export Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="87a4d-115">An embedded instance of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="87a4d-116">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="87a4d-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87a4d-117">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="87a4d-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a4d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87a4d-118">Return value</span></span>

<span data-ttu-id="87a4d-119">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="87a4d-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="87a4d-120">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="87a4d-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-121">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="87a4d-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-122">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="87a4d-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-123">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="87a4d-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-124">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="87a4d-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-125">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="87a4d-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-126">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="87a4d-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-127">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="87a4d-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-128">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="87a4d-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-129">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="87a4d-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-130">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="87a4d-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-131">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="87a4d-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="87a4d-132">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="87a4d-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="87a4d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87a4d-133">Requirements</span></span>



| <span data-ttu-id="87a4d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87a4d-134">Requirement</span></span> | <span data-ttu-id="87a4d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="87a4d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a4d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87a4d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="87a4d-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87a4d-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="87a4d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87a4d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="87a4d-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87a4d-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87a4d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="87a4d-140">Namespace</span></span><br/>                | <span data-ttu-id="87a4d-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="87a4d-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="87a4d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="87a4d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87a4d-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="87a4d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87a4d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="87a4d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87a4d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87a4d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87a4d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87a4d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a4d-147">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="87a4d-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

