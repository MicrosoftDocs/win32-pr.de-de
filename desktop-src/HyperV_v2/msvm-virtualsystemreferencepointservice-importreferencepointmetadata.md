---
description: Importiert Verweis Punkt Metadaten des virtuellen Systems.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Importreferencepointmetadata-Methode der Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961202"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="3e343-103">Importreferencepointmetadata-Methode der MSVM \_ virtualsystemreferencepointservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3e343-103">ImportReferencePointMetadata method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="3e343-104">Importiert Verweis Punkt Metadaten des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="3e343-104">Imports reference point metadata of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e343-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e343-105">Syntax</span></span>


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3e343-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e343-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e343-107">*Affectedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e343-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e343-108">Ein Verweis auf ein [**MSVM- \_ Computersystem**](msvm-computersystem.md) , das das betroffene System beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3e343-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) describing the affected system.</span></span>

</dd> <dt>

<span data-ttu-id="3e343-109">*Configfilepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e343-109">*ConfigFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e343-110">Der voll qualifizierte Pfad der Konfigurationsdatei, aus der die Verweis Punkt Metadaten importiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e343-110">The fully-qualified path of the config file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="3e343-111">*Runtimestatefilepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e343-111">*RuntimeStateFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e343-112">Der voll qualifizierte Pfad der Lauf Zeit Zustands Datei, von der die Verweis Punkt Metadaten importiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e343-112">The fully-qualified path of the runtime state file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="3e343-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3e343-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e343-114">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="3e343-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="3e343-115">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="3e343-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e343-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e343-116">Return value</span></span>

<span data-ttu-id="3e343-117">Gibt entweder 0 (kein Fehler) oder eine der folgenden Fehlermeldungen zurück:</span><span class="sxs-lookup"><span data-stu-id="3e343-117">Returns either 0 (no error) or one of the following error messages:</span></span>

<dl> <dt>

<span data-ttu-id="3e343-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3e343-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3e343-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="3e343-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3e343-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3e343-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="3e343-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3e343-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="3e343-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="3e343-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="3e343-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="3e343-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="3e343-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3e343-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="3e343-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3e343-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e343-131">Requirements</span></span>



| <span data-ttu-id="3e343-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e343-132">Requirement</span></span> | <span data-ttu-id="3e343-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3e343-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e343-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e343-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3e343-135">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e343-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3e343-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e343-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3e343-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3e343-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3e343-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e343-138">Namespace</span></span><br/>                | <span data-ttu-id="3e343-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3e343-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3e343-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3e343-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e343-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3e343-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e343-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3e343-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e343-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e343-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e343-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e343-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e343-145">**MSVM \_ virtualsystemreferencepointservice**</span><span class="sxs-lookup"><span data-stu-id="3e343-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




