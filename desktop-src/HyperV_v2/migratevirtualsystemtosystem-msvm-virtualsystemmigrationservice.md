---
description: Verschieben, migrieren oder Verschieben eines virtuellen Systems in ein Zielsystem.
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: MigrateVirtualSystemToSystem-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a346596b094b60456af8e2b63865bec1171d99ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344969"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="71f9c-103">MigrateVirtualSystemToSystem-Methode der MSVM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="71f9c-103">MigrateVirtualSystemToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="71f9c-104">Verschieben, migrieren oder Verschieben eines virtuellen Systems in ein Zielsystem.</span><span class="sxs-lookup"><span data-stu-id="71f9c-104">Moves, migrates, or relocates a virtual system to a target system.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f9c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71f9c-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="71f9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71f9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f9c-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f9c-108">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die das zu migrierende virtuelle Computersystem darstellt.</span><span class="sxs-lookup"><span data-stu-id="71f9c-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="71f9c-109">*DestinationSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f9c-110">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die das System darstellt, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="71f9c-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system to be migrated to.</span></span>

</dd> <dt>

<span data-ttu-id="71f9c-111">*Migrationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f9c-112">Eine eingebettete Instanz der [**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md) -Klasse, die Einstellungen für den Migrations Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="71f9c-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="71f9c-113">*Newsystemsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f9c-114">Eine eingebettete Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="71f9c-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="71f9c-115">*Newresourcesettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f9c-116">Ein Array von Zeichen folgen, die eine eingebettete Instanz der [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse enthalten, die die neuen Eigenschaften darstellt, die für virtuelle Ressourcen des virtuellen Systems nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="71f9c-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="71f9c-117">*Newcomputersystem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-117">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71f9c-118">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die das neue migrierte System darstellt.</span><span class="sxs-lookup"><span data-stu-id="71f9c-118">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the new migrated system.</span></span>

</dd> <dt>

<span data-ttu-id="71f9c-119">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71f9c-120">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="71f9c-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f9c-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71f9c-121">Return value</span></span>

<span data-ttu-id="71f9c-122">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="71f9c-122">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="71f9c-123">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="71f9c-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-124">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="71f9c-124">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-125">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="71f9c-125">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-126">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="71f9c-126">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-127">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="71f9c-127">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-128">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="71f9c-128">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-129">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="71f9c-129">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-130">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="71f9c-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-131">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="71f9c-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-132">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="71f9c-132">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="71f9c-133">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="71f9c-133">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="71f9c-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71f9c-134">Requirements</span></span>



| <span data-ttu-id="71f9c-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71f9c-135">Requirement</span></span> | <span data-ttu-id="71f9c-136">Wert</span><span class="sxs-lookup"><span data-stu-id="71f9c-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f9c-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71f9c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="71f9c-138">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="71f9c-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71f9c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="71f9c-140">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71f9c-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="71f9c-141">Namespace</span></span><br/>                | <span data-ttu-id="71f9c-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="71f9c-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="71f9c-143">MOF</span><span class="sxs-lookup"><span data-stu-id="71f9c-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71f9c-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="71f9c-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71f9c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="71f9c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71f9c-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71f9c-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="71f9c-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71f9c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f9c-148">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="71f9c-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

