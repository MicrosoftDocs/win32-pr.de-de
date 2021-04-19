---
description: Bestimmt, ob das angegebene virtuelle System zu einem Zielhost migriert werden kann, der von einem Netzwerknamen oder einer IP-Adresse angegeben wird.
ms.assetid: eacc8448-4683-48df-81b9-8599292944db
title: CheckVirtualSystemIsMigratableToHost-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b81f6562f892acbaa5bf7ff7f4f3c772574bd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367864"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="7b2f5-103">CheckVirtualSystemIsMigratableToHost-Methode der MSVM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="7b2f5-103">CheckVirtualSystemIsMigratableToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="7b2f5-104">Bestimmt, ob das angegebene virtuelle System zu einem Zielhost migriert werden kann, der von einem Netzwerknamen oder einer IP-Adresse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7b2f5-104">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b2f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b2f5-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  string                  DestinationHost,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="7b2f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b2f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b2f5-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b2f5-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f5-108">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer zum Testen der Migrations Fähigkeit von darstellt.</span><span class="sxs-lookup"><span data-stu-id="7b2f5-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f5-109">*Destinationhost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b2f5-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f5-110">Der Name des Host Systems für die Migration.</span><span class="sxs-lookup"><span data-stu-id="7b2f5-110">The name of the host system for the migration.</span></span> <span data-ttu-id="7b2f5-111">Das Format dieses Namens wird von der **destinationhostformatssupported** -Eigenschaft der [**MSVM \_ virtualsystemmigrationfunktionalitäten**](msvm-virtualsystemmigrationcapabilities.md) -Klasse angegeben, die dieser Klasse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7b2f5-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f5-112">*Migrationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b2f5-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f5-113">Eine eingebettete Instanz der [**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md) -Klasse, die Einstellungen für den Migrations Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="7b2f5-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f5-114">*Newsystemsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b2f5-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f5-115">Eine eingebettete Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="7b2f5-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f5-116">*Newresourcesettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b2f5-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f5-117">Ein Array von Zeichen folgen, die eine eingebettete Instanz der [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse enthalten, die die neuen Eigenschaften darstellt, die für virtuelle Ressourcen des virtuellen Systems nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="7b2f5-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f5-118">*IsMigratable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7b2f5-118">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f5-119">Empfängt das Ergebnis der Migrations Überprüfung, das angibt, ob das virtuelle System erfolgreich migriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7b2f5-119">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b2f5-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b2f5-120">Return value</span></span>

<span data-ttu-id="7b2f5-121">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7b2f5-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7b2f5-122">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7b2f5-123">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7b2f5-124">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="7b2f5-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7b2f5-125">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7b2f5-126">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7b2f5-127">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-127">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7b2f5-128">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-128">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7b2f5-129">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-129">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7b2f5-130">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7b2f5-131">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-131">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7b2f5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b2f5-132">Requirements</span></span>



| <span data-ttu-id="7b2f5-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b2f5-133">Requirement</span></span> | <span data-ttu-id="7b2f5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="7b2f5-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2f5-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7b2f5-136">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b2f5-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7b2f5-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b2f5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7b2f5-138">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b2f5-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b2f5-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b2f5-139">Namespace</span></span><br/>                | <span data-ttu-id="7b2f5-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7b2f5-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7b2f5-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7b2f5-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b2f5-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7b2f5-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b2f5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7b2f5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b2f5-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b2f5-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7b2f5-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b2f5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b2f5-146">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="7b2f5-146">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




