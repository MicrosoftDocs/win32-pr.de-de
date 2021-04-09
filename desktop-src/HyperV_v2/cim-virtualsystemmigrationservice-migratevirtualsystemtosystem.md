---
description: Methode zum Verschieben, migrieren oder Verschieben eines virtuellen Systems in ein Zielsystem.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: MigrateVirtualSystemToSystem-Methode der CIM_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864575"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="9229b-103">MigrateVirtualSystemToSystem-Methode der CIM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="9229b-103">MigrateVirtualSystemToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="9229b-104">Methode zum Verschieben, migrieren oder Verschieben eines virtuellen Systems in ein Zielsystem.</span><span class="sxs-lookup"><span data-stu-id="9229b-104">Method to move, migrate or relocate a virtual system to a target system.</span></span>

<span data-ttu-id="9229b-105">Rückgabecode Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="9229b-105">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="9229b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9229b-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="9229b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9229b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9229b-108">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9229b-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9229b-109">Das zu migrierende virtuelle Quellcomputer System.</span><span class="sxs-lookup"><span data-stu-id="9229b-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="9229b-110">*DestinationSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9229b-110">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9229b-111">Ziel Host System für die Migration des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="9229b-111">Destination host system whereto migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="9229b-112">*Migrationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9229b-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9229b-113">Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemmigrationsettingdata**](cim-virtualsystemmigrationsettingdata.md) -Klasse enthält, die für den Migrations Vorgang geltende Migrations Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="9229b-113">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="9229b-114">*Newsystemsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9229b-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9229b-115">Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="9229b-115">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="9229b-116">*Newresourcesettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9229b-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9229b-117">Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für virtuelle Ressourcen im Bereich des virtuellen Systems nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="9229b-117">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="9229b-118">*Newcomputersystem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9229b-118">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9229b-119">Verweis auf eine Instanz der [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse, die das virtuelle Computersystem nach der Migration darstellt.</span><span class="sxs-lookup"><span data-stu-id="9229b-119">Reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class representing the virtual computer system after it has been migrated.</span></span>

</dd> <dt>

<span data-ttu-id="9229b-120">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9229b-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9229b-121">Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="9229b-121">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9229b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9229b-122">Return value</span></span>

<span data-ttu-id="9229b-123">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9229b-123">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="9229b-124">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="9229b-124">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="9229b-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9229b-125">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9229b-126"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-126"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="9229b-127">Das virtuelle System wurde migriert.</span><span class="sxs-lookup"><span data-stu-id="9229b-127">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="9229b-128"><dt>**Nicht unterstützt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-128"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="9229b-129">Die Methode wird von der Implementierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9229b-129">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="9229b-130"><dt></dt> Fehler <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="9229b-131">Die Migration des virtuellen Systems ist aus unbekannten Gründen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="9229b-131">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="9229b-132"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-132"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="9229b-133">Timeout bei der Migration virtueller Systeme; der Status des virtuellen Systems ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="9229b-133">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="9229b-134"><dt>**Ungültiger Parameter**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-134"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="9229b-135">Mindestens ein Parameter ist formal ungültig, z. b., wenn der Wert des Ziel System Parameters keinen gültigen Objekt Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="9229b-135">One or more parameters are formally invalid For example, the value of the Destination System parameter does not contain a valid object path.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="9229b-136"><dt>**Ungültiger Status**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="9229b-137">Das virtuelle Quellsystem, das Quell Host System oder das Ziel Host System befinden sich in einem Zustand, der die Initiierung der angeforderten Migration des virtuellen Systems zulässt. Dabei kann es sich um eine temporäre Bedingung handeln.</span><span class="sxs-lookup"><span data-stu-id="9229b-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="9229b-138">Nicht <dt>**kompatible Parameter**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="9229b-139">Mindestens ein Eingabeparameter ist nicht als Satz oder in Bezug auf den Zielhost inkompatibel.</span><span class="sxs-lookup"><span data-stu-id="9229b-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="9229b-140">Beispielsweise enthält der Wert des *migrationnewsettingdata* -Parameters Eigenschaften, die vom Ziel Host System, das durch den Wert des *DestinationSystem* -Parameters identifiziert wird, nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9229b-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="9229b-141"><dt>**DMTF reserviert**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="9229b-142"><dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="9229b-143"><dt>**Reservierte Methode**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="9229b-144"><dt>**Hersteller spezifischer**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="9229b-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9229b-145">Requirements</span></span>



| <span data-ttu-id="9229b-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9229b-146">Requirement</span></span> | <span data-ttu-id="9229b-147">Wert</span><span class="sxs-lookup"><span data-stu-id="9229b-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9229b-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9229b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9229b-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9229b-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9229b-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9229b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9229b-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9229b-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9229b-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="9229b-152">Namespace</span></span><br/>                | <span data-ttu-id="9229b-153">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9229b-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9229b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="9229b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9229b-155"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9229b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9229b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9229b-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9229b-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9229b-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9229b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9229b-159">**CIM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="9229b-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




