---
description: Bestimmt, ob das angegebene virtuelle System zu einem Zielsystem migriert werden kann.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: CheckVirtualSystemIsMigratableToSystem-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345667"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="d0dd8-103">CheckVirtualSystemIsMigratableToSystem-Methode der MSVM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="d0dd8-103">CheckVirtualSystemIsMigratableToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="d0dd8-104">Bestimmt, ob das angegebene virtuelle System zu einem Zielsystem migriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d0dd8-104">Determines whether the specified virtual system can be migrated to a destination system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0dd8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0dd8-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="d0dd8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0dd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0dd8-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd8-108">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer zum Testen der Migrations Fähigkeit von darstellt.</span><span class="sxs-lookup"><span data-stu-id="d0dd8-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="d0dd8-109">*DestinationSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd8-110">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer zum Testen der Migrations Fähigkeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="d0dd8-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability to.</span></span>

</dd> <dt>

<span data-ttu-id="d0dd8-111">*Migrationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd8-112">Eine eingebettete Instanz der [**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md) -Klasse, die Einstellungen für den Migrations Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="d0dd8-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="d0dd8-113">*Newsystemsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd8-114">Eine eingebettete Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="d0dd8-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d0dd8-115">*Newresourcesettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd8-116">Ein Array von Zeichen folgen, die eine eingebettete Instanz der [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse enthalten, die die neuen Eigenschaften darstellt, die für virtuelle Ressourcen des virtuellen Systems nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="d0dd8-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d0dd8-117">*IsMigratable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-117">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd8-118">Empfängt das Ergebnis der Migrations Überprüfung, das angibt, ob das virtuelle System erfolgreich migriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d0dd8-118">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0dd8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0dd8-119">Return value</span></span>

<span data-ttu-id="d0dd8-120">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="d0dd8-120">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d0dd8-121">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d0dd8-122">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d0dd8-123">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="d0dd8-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d0dd8-124">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d0dd8-125">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d0dd8-126">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d0dd8-127">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-127">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d0dd8-128">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d0dd8-129">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d0dd8-130">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-130">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d0dd8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0dd8-131">Requirements</span></span>



| <span data-ttu-id="d0dd8-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0dd8-132">Requirement</span></span> | <span data-ttu-id="d0dd8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d0dd8-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0dd8-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d0dd8-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d0dd8-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0dd8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d0dd8-137">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-137">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d0dd8-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0dd8-138">Namespace</span></span><br/>                | <span data-ttu-id="d0dd8-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d0dd8-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d0dd8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d0dd8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0dd8-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd8-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0dd8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d0dd8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0dd8-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd8-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d0dd8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0dd8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0dd8-145">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="d0dd8-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




