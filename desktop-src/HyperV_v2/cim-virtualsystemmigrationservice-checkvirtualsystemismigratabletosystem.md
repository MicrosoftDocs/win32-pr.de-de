---
description: 'Weitere Informationen finden Sie unter: CheckVirtualSystemIsMigratableToSystem-Methode der CIM_VirtualSystemMigrationService-Klasse'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: CheckVirtualSystemIsMigratableToSystem-Methode der CIM_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348947"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="1a244-103">CheckVirtualSystemIsMigratableToSystem-Methode der CIM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="1a244-103">CheckVirtualSystemIsMigratableToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="1a244-104">Methode zum Durchführen einer vorab Überprüfung, um zu bestimmen, ob ein virtuelles System wahrscheinlich erfolgreich zu einem Zielsystem migriert wird.</span><span class="sxs-lookup"><span data-stu-id="1a244-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target system.</span></span> <span data-ttu-id="1a244-105">Diese Methode garantiert nicht, dass eine nachfolgende Migration aufgrund dynamischer Ressourcen Verfügbarkeit immer erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1a244-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span> <span data-ttu-id="1a244-106">Rückgabecode Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="1a244-106">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="1a244-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a244-107">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="1a244-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a244-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a244-109">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a244-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a244-110">[**CIM \_ Computersystem**](cim-computersystem.md) Instanz, die auf das zu migrierende virtuelle Quellcomputer System verweist.</span><span class="sxs-lookup"><span data-stu-id="1a244-110">[**CIM\_ComputerSystem**](cim-computersystem.md) instance referencing the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1a244-111">*DestinationSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a244-111">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a244-112">[**CIM \_ System**](cim-system.md) Instanz, die auf das Zielsystem verweist, auf das das virtuelle System migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a244-112">[**CIM\_System**](cim-system.md) instance referencing the destination system onto which to migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="1a244-113">*Migrationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a244-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a244-114">Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemmigrationsettingdata**](cim-virtualsystemmigrationsettingdata.md) -Klasse enthält, die für den Migrations Vorgang geltende Migrations Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a244-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="1a244-115">*Newsystemsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a244-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a244-116">Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="1a244-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1a244-117">*Newresourcesettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a244-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a244-118">Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für virtuelle Ressourcen im Bereich des virtuellen Systems nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="1a244-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1a244-119">*IsMigratable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1a244-119">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a244-120">Das Ergebnis der Migrations Überprüfung, das angibt, ob das virtuelle System erfolgreich migriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a244-120">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a244-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a244-121">Return value</span></span>

<span data-ttu-id="1a244-122">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1a244-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="1a244-123">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="1a244-123">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="1a244-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a244-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a244-125"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="1a244-126">Überprüfung durchgeführt Das Ergebnis wurde über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="1a244-126">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="1a244-127"><dt>**Nicht unterstützt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="1a244-128">Die Methode wird von der Implementierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a244-128">Method not supported by implementation.</span></span> <span data-ttu-id="1a244-129">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="1a244-129">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="1a244-130"><dt></dt> Fehler <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="1a244-131">Überprüfen von nicht spezifizierten Gründen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="1a244-131">Check failed for unspecified reasons.</span></span> <span data-ttu-id="1a244-132">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="1a244-132">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="1a244-133"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-133"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="1a244-134">Timeout bei der Überprüfung. Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="1a244-134">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="1a244-135"><dt>**Ungültiger Parameter**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-135"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="1a244-136">Mindestens ein Parameter ist formal ungültig.</span><span class="sxs-lookup"><span data-stu-id="1a244-136">One or more parameters are formally invalid.</span></span> <span data-ttu-id="1a244-137">Beispielsweise besteht der Wert des *DestinationSystem* -Parameters nicht aus einem gültigen Objekt Pfad.</span><span class="sxs-lookup"><span data-stu-id="1a244-137">For example, the value of the *DestinationSystem* parameter does not comprise a valid object path.</span></span> <span data-ttu-id="1a244-138">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="1a244-138">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="1a244-139"><dt>**Ungültiger Status**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-139"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="1a244-140">Das virtuelle Quellsystem, das Quell Host System oder das Ziel Host System befinden sich in einem Zustand, der die Initiierung der angeforderten Migration des virtuellen Systems zulässt. Dabei kann es sich um eine temporäre Bedingung handeln.</span><span class="sxs-lookup"><span data-stu-id="1a244-140">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="1a244-141">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="1a244-141">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="1a244-142">Nicht <dt>**kompatible Parameter**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-142"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="1a244-143">Mindestens ein Eingabeparameter ist nicht als Satz oder in Bezug auf den Zielhost inkompatibel.</span><span class="sxs-lookup"><span data-stu-id="1a244-143">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="1a244-144">Beispielsweise enthält der Wert des *newsettingdata* -Parameters Eigenschaften, die vom Ziel Host System, das durch den Wert des *DestinationSystem* -Parameters identifiziert wird, nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1a244-144">For example the value of the *NewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span> <span data-ttu-id="1a244-145">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="1a244-145">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="1a244-146"><dt>**DMTF reserviert**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-146"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="1a244-147"><dt>**Reservierte Methode**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-147"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="1a244-148"><dt>**Hersteller spezifischer**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-148"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="1a244-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a244-149">Requirements</span></span>



| <span data-ttu-id="1a244-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a244-150">Requirement</span></span> | <span data-ttu-id="1a244-151">Wert</span><span class="sxs-lookup"><span data-stu-id="1a244-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a244-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a244-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1a244-153">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1a244-153">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1a244-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a244-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1a244-155">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1a244-155">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1a244-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a244-156">Namespace</span></span><br/>                | <span data-ttu-id="1a244-157">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1a244-157">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1a244-158">MOF</span><span class="sxs-lookup"><span data-stu-id="1a244-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a244-159"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a244-160">DLL</span><span class="sxs-lookup"><span data-stu-id="1a244-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a244-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a244-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a244-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a244-163">**CIM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="1a244-163">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




