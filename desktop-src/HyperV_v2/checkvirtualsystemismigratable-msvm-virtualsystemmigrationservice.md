---
description: Bestimmt, ob das angegebene virtuelle System migriert werden kann.
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: CheckVirtualSystemIsMigratable-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1aed843f3f0f4c6c30eb6125cdd5859cdba902d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862079"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="0f7cb-103">CheckVirtualSystemIsMigratable-Methode der MSVM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0f7cb-103">CheckVirtualSystemIsMigratable method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="0f7cb-104">Bestimmt, ob das angegebene virtuelle System migriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f7cb-104">Determines whether the specified virtual system can be migrated.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f7cb-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0f7cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f7cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f7cb-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f7cb-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7cb-108">Ein Verweis auf eine Instanz der [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse, die den virtuellen Computer zum Testen der Migrations Fähigkeit von darstellt.</span><span class="sxs-lookup"><span data-stu-id="0f7cb-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="0f7cb-109">*Destinationhost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f7cb-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7cb-110">Der Name des Host Systems für die Migration.</span><span class="sxs-lookup"><span data-stu-id="0f7cb-110">The name of the host system for the migration.</span></span> <span data-ttu-id="0f7cb-111">Das Format dieses Namens wird von der **destinationhostformatssupported** -Eigenschaft der [**MSVM \_ virtualsystemmigrationfunktionalitäten**](msvm-virtualsystemmigrationcapabilities.md) -Klasse angegeben, die dieser Klasse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0f7cb-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="0f7cb-112">*Migrationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f7cb-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7cb-113">Eine eingebettete Instanz der [**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md) -Klasse, die Einstellungen für den Migrations Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="0f7cb-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="0f7cb-114">*Newsystemsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f7cb-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7cb-115">Eine eingebettete Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="0f7cb-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="0f7cb-116">*Newresourcesettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f7cb-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7cb-117">Ein Array von Zeichen folgen, die eine eingebettete Instanz der [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse enthalten, die die neuen Eigenschaften darstellt, die für virtuelle Ressourcen des virtuellen Systems nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="0f7cb-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="0f7cb-118">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0f7cb-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7cb-119">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0f7cb-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f7cb-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f7cb-120">Return value</span></span>

<span data-ttu-id="0f7cb-121">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0f7cb-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0f7cb-122">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="0f7cb-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-123">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="0f7cb-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-124">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="0f7cb-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-125">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="0f7cb-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-126">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="0f7cb-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-127">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="0f7cb-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-128">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="0f7cb-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-129">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="0f7cb-129">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-130">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="0f7cb-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-131">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="0f7cb-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-132">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="0f7cb-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0f7cb-133">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="0f7cb-133">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0f7cb-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f7cb-134">Requirements</span></span>



| <span data-ttu-id="0f7cb-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f7cb-135">Requirement</span></span> | <span data-ttu-id="0f7cb-136">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7cb-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7cb-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f7cb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0f7cb-138">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f7cb-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0f7cb-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f7cb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0f7cb-140">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f7cb-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f7cb-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f7cb-141">Namespace</span></span><br/>                | <span data-ttu-id="0f7cb-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0f7cb-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0f7cb-143">MOF</span><span class="sxs-lookup"><span data-stu-id="0f7cb-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f7cb-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0f7cb-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f7cb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0f7cb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f7cb-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f7cb-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f7cb-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f7cb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f7cb-148">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="0f7cb-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

