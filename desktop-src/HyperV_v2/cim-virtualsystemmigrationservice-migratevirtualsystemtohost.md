---
description: Methode zum Verschieben, migrieren oder Verschieben eines virtuellen Systems auf einen Zielhost, der durch einen Netzwerknamen oder eine IP-Adresse angegeben wird.
ms.assetid: 09fdc0b2-641c-47f5-b270-e26e3acf7ea5
title: MigrateVirtualSystemToHost-Methode der CIM_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1a90e3adadbb5efc5f9cae3b7710e07c1e05000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356119"
---
# <a name="migratevirtualsystemtohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="339eb-103">MigrateVirtualSystemToHost-Methode der CIM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="339eb-103">MigrateVirtualSystemToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="339eb-104">Methode zum Verschieben, migrieren oder Verschieben eines virtuellen Systems auf einen Zielhost, der durch einen Netzwerknamen oder eine IP-Adresse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="339eb-104">Method to move, migrate or relocate a virtual system to a target host specified by a network name or IP address.</span></span>

> [!Note]  
> <span data-ttu-id="339eb-105">Diese Methode ist nur dann als Übergangslösung vorgesehen, wenn die Modellierung der Cluster Unterstützung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="339eb-105">This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="339eb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="339eb-106">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="339eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="339eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="339eb-108">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="339eb-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339eb-109">Das zu migrierende virtuelle Quellcomputer System.</span><span class="sxs-lookup"><span data-stu-id="339eb-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="339eb-110">*Destinationhost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="339eb-110">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339eb-111">Ziel Host System für die Migration.</span><span class="sxs-lookup"><span data-stu-id="339eb-111">Target host system for the migration.</span></span>

<span data-ttu-id="339eb-112">Zulässige Formate für diesen Parameter werden durch Werte von Elementen der **destinationhostformatssupported** - \[ \] Array Eigenschaft in der Instanz von [**CIM \_ virtualsystemmigrationfunktionen**](cim-virtualsystemmigrationcapabilities.md) übermittelt, die durch die [**CIM \_ elementfunktionalitäten**](cim-elementcapabilities.md) -Zuordnung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="339eb-112">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="339eb-113">*Migrationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="339eb-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339eb-114">Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemmigrationsettingdata**](cim-virtualsystemmigrationsettingdata.md) -Klasse enthält, die für den Migrations Vorgang geltende Migrations Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="339eb-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="339eb-115">*Newsystemsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="339eb-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339eb-116">Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="339eb-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="339eb-117">*Newresourcesettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="339eb-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339eb-118">Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für virtuelle Ressourcen im Bereich des virtuellen Systems nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="339eb-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="339eb-119">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="339eb-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="339eb-120">Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="339eb-120">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="339eb-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="339eb-121">Return value</span></span>

<span data-ttu-id="339eb-122">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="339eb-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="339eb-123">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="339eb-123">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="339eb-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="339eb-124">Description</span></span>                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="339eb-125"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="339eb-126">Das virtuelle System wurde migriert.</span><span class="sxs-lookup"><span data-stu-id="339eb-126">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="339eb-127"><dt>**Nicht unterstützt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="339eb-128">Die Methode wird von der Implementierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="339eb-128">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="339eb-129"><dt></dt> Fehler <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-129"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="339eb-130">Die Migration des virtuellen Systems ist aus unbekannten Gründen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="339eb-130">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="339eb-131"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-131"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="339eb-132">Timeout bei der Migration virtueller Systeme; der Status des virtuellen Systems ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="339eb-132">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="339eb-133"><dt>**Ungültiger Parameter**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-133"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="339eb-134">Mindestens ein Parameter ist formal ungültig.</span><span class="sxs-lookup"><span data-stu-id="339eb-134">One or more parameters are formally invalid.</span></span> <span data-ttu-id="339eb-135">Beispielsweise könnte der Wert des *destinationhost* -Parameters in einem nicht unterstützten Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="339eb-135">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="339eb-136"><dt>**Ungültiger Status**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="339eb-137">Das virtuelle Quellsystem, das Quell Host System oder das Ziel Host System befinden sich in einem Zustand, der die Initiierung der angeforderten Migration des virtuellen Systems zulässt. Dabei kann es sich um eine temporäre Bedingung handeln.</span><span class="sxs-lookup"><span data-stu-id="339eb-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="339eb-138">Nicht <dt>**kompatible Parameter**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="339eb-139">Mindestens ein Eingabeparameter ist nicht als Satz oder in Bezug auf den Zielhost inkompatibel.</span><span class="sxs-lookup"><span data-stu-id="339eb-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="339eb-140">Beispielsweise enthält der Wert des *migrationnewsettingdata* -Parameters Eigenschaften, die vom Ziel Host System, das durch den Wert des *destinationhost* -Parameters identifiziert wird, nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="339eb-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="339eb-141"><dt>**DMTF reserviert**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="339eb-142"><dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="339eb-143"><dt>**Reservierte Methode**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="339eb-144"><dt>**Hersteller spezifischer**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="339eb-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="339eb-145">Requirements</span></span>



| <span data-ttu-id="339eb-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="339eb-146">Requirement</span></span> | <span data-ttu-id="339eb-147">Wert</span><span class="sxs-lookup"><span data-stu-id="339eb-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="339eb-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="339eb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="339eb-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="339eb-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="339eb-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="339eb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="339eb-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="339eb-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="339eb-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="339eb-152">Namespace</span></span><br/>                | <span data-ttu-id="339eb-153">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="339eb-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="339eb-154">MOF</span><span class="sxs-lookup"><span data-stu-id="339eb-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="339eb-155"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="339eb-156">DLL</span><span class="sxs-lookup"><span data-stu-id="339eb-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="339eb-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="339eb-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="339eb-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="339eb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339eb-159">**CIM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="339eb-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




