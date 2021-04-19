---
description: Methode zum Durchführen einer vorab Überprüfung, um zu bestimmen, ob ein virtuelles System wahrscheinlich erfolgreich zu einem Zielhost migriert wird, der durch einen Netzwerknamen oder eine IP-Adresse angegeben ist.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: CheckVirtualSystemIsMigratableToHost-Methode der CIM_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5769691a792b8f74225b640b0058ad4bd0e27c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355670"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="2e442-103">CheckVirtualSystemIsMigratableToHost-Methode der CIM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="2e442-103">CheckVirtualSystemIsMigratableToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="2e442-104">Methode zum Durchführen einer vorab Überprüfung, um zu bestimmen, ob ein virtuelles System wahrscheinlich erfolgreich zu einem Zielhost migriert wird, der durch einen Netzwerknamen oder eine IP-Adresse angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2e442-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target host specified by a network name or IP address.</span></span> <span data-ttu-id="2e442-105">Diese Methode garantiert nicht, dass eine nachfolgende Migration aufgrund dynamischer Ressourcen Verfügbarkeit immer erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="2e442-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span>

<span data-ttu-id="2e442-106">Rückgabecode Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="2e442-106">Return code description:</span></span>

<span data-ttu-id="2e442-107">Hinweis: Diese Methode ist nur dann als Übergangslösung vorgesehen, wenn eine Modellierung der Cluster Unterstützung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2e442-107">Note: This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e442-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e442-108">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="2e442-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e442-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e442-110">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e442-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e442-111">Ein [**CIM \_ Computersystem**](cim-computersystem.md) -Verweis auf das zu migrierende virtuelle Quellcomputer System.</span><span class="sxs-lookup"><span data-stu-id="2e442-111">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="2e442-112">*Destinationhost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e442-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e442-113">Ziel Host System für die Migration.</span><span class="sxs-lookup"><span data-stu-id="2e442-113">Target host system for the migration.</span></span>

<span data-ttu-id="2e442-114">Zulässige Formate für diesen Parameter werden durch Werte von Elementen der **destinationhostformatssupported** - \[ \] Array Eigenschaft in der Instanz von [**CIM \_ virtualsystemmigrationfunktionen**](cim-virtualsystemmigrationcapabilities.md) übermittelt, die durch die [**CIM \_ elementfunktionalitäten**](cim-elementcapabilities.md) -Zuordnung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="2e442-114">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="2e442-115">*Migrationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e442-115">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e442-116">Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemmigrationsettingdata**](cim-virtualsystemmigrationsettingdata.md) -Klasse enthält, die für den Migrations Vorgang geltende Migrations Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="2e442-116">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="2e442-117">*Newsystemsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e442-117">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e442-118">Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="2e442-118">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="2e442-119">*Newresourcesettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e442-119">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e442-120">Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für virtuelle Ressourcen im Bereich des virtuellen Systems nach der Migration gelten.</span><span class="sxs-lookup"><span data-stu-id="2e442-120">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="2e442-121">*IsMigratable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e442-121">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e442-122">Das Ergebnis der Migrations Überprüfung, das angibt, ob das virtuelle System erfolgreich migriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e442-122">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e442-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e442-123">Return value</span></span>

<span data-ttu-id="2e442-124">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e442-124">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="2e442-125">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="2e442-125">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="2e442-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e442-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e442-127"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-127"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="2e442-128">Überprüfung durchgeführt Das Ergebnis wurde über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="2e442-128">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="2e442-129"><dt>**Nicht unterstützt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-129"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="2e442-130">Die Methode wird von der Implementierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2e442-130">Method not supported by implementation.</span></span> <span data-ttu-id="2e442-131">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="2e442-131">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="2e442-132"><dt></dt> Fehler <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-132"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="2e442-133">Überprüfen von nicht spezifizierten Gründen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="2e442-133">Check failed for unspecified reasons.</span></span> <span data-ttu-id="2e442-134">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="2e442-134">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="2e442-135"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-135"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="2e442-136">Timeout bei der Überprüfung. Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="2e442-136">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="2e442-137"><dt>**Ungültiger Parameter**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-137"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="2e442-138">Mindestens ein Parameter ist formal ungültig.</span><span class="sxs-lookup"><span data-stu-id="2e442-138">One or more parameters are formally invalid.</span></span> <span data-ttu-id="2e442-139">Beispielsweise könnte der Wert des *destinationhost* -Parameters in einem nicht unterstützten Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e442-139">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span> <span data-ttu-id="2e442-140">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="2e442-140">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="2e442-141"><dt>**Ungültiger Status**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-141"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="2e442-142">Das virtuelle Quellsystem, das Quell Host System oder das Ziel Host System befinden sich in einem Zustand, der die Initiierung der angeforderten Migration des virtuellen Systems zulässt. Dabei kann es sich um eine temporäre Bedingung handeln.</span><span class="sxs-lookup"><span data-stu-id="2e442-142">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="2e442-143">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="2e442-143">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="2e442-144">Nicht <dt>**kompatible Parameter**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-144"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="2e442-145">Mindestens ein Eingabeparameter ist nicht als Satz oder in Bezug auf den Zielhost inkompatibel.</span><span class="sxs-lookup"><span data-stu-id="2e442-145">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="2e442-146">Beispielsweise enthält der Wert des *migrationnewsettingdata* -Parameters Eigenschaften, die vom Ziel Host System, das durch den Wert des *destinationhost* -Parameters identifiziert wird, nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2e442-146">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span> <span data-ttu-id="2e442-147">Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.</span><span class="sxs-lookup"><span data-stu-id="2e442-147">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="2e442-148"><dt>**DMTF reserviert**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-148"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="2e442-149"><dt>**Reservierte Methode**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-149"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="2e442-150"><dt>**Hersteller spezifischer**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-150"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="2e442-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e442-151">Requirements</span></span>



| <span data-ttu-id="2e442-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e442-152">Requirement</span></span> | <span data-ttu-id="2e442-153">Wert</span><span class="sxs-lookup"><span data-stu-id="2e442-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e442-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e442-154">Minimum supported client</span></span><br/> | <span data-ttu-id="2e442-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2e442-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2e442-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e442-156">Minimum supported server</span></span><br/> | <span data-ttu-id="2e442-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2e442-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2e442-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e442-158">Namespace</span></span><br/>                | <span data-ttu-id="2e442-159">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2e442-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2e442-160">MOF</span><span class="sxs-lookup"><span data-stu-id="2e442-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e442-161"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e442-162">DLL</span><span class="sxs-lookup"><span data-stu-id="2e442-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e442-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e442-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e442-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e442-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e442-165">**CIM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="2e442-165">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




