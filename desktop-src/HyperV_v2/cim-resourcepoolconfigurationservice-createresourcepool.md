---
description: Startet einen Auftrag, um einen Stamm Ressourcenpool zu erstellen. Der Bereich "resourcepool" wird auf dasselbe System wie dieser Dienst beschränkt.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Die Methode "kreateresourcepool" der CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752248"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="6f511-104">Die Methode "samateresourcepool" der CIM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="6f511-104">CreateResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="6f511-105">Startet einen Auftrag, um einen Stamm Ressourcenpool zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6f511-105">Starts a job to create a root ResourcePool.</span></span> <span data-ttu-id="6f511-106">Der Bereich "resourcepool" wird auf dasselbe System wie dieser Dienst beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6f511-106">The ResourcePool will be scoped to the same System as this Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f511-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f511-107">Syntax</span></span>


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6f511-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f511-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f511-109">*ElementName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f511-109">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f511-110">Ein Endbenutzer relevanter Name für den Pool, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6f511-110">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="6f511-111">Wenn der Wert **null** ist, kann ein vom System bereitgestellter Standardname verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f511-111">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="6f511-112">Der Wert wird in der **ElementName** -Eigenschaft für den erstellten Pool gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6f511-112">The value will be stored in the **ElementName** property for the created pool.</span></span>

</dd> <dt>

<span data-ttu-id="6f511-113">" *Hustresources* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="6f511-113">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f511-114">Ein Array von 0 (null) oder mehr [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Geräten, die verwendet werden, um den Pool zu erstellen oder die Quell Blöcke zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6f511-114">Array of zero or more [**CIM\_LogicalDevice**](cim-logicaldevice.md) devices that are used to create the Pool or modify the source extents.</span></span> <span data-ttu-id="6f511-115">Alle Elemente im Array müssen denselben Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6f511-115">All elements in the array must be of the same type.</span></span>

</dd> <dt>

<span data-ttu-id="6f511-116">*ResourceType* \[in\]</span><span class="sxs-lookup"><span data-stu-id="6f511-116">*ResourceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f511-117">Der Typ der Ressourcen, die vom erstellten Pool verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6f511-117">The type of resources the created pool will manage.</span></span> <span data-ttu-id="6f511-118">Wenn " *hustresources* " Elemente enthält, muss diese Eigenschaft den Typ "" haben.</span><span class="sxs-lookup"><span data-stu-id="6f511-118">If *HostResources* contains elements, this property must mach their type.</span></span>

</dd> <dt>

<span data-ttu-id="6f511-119">*Pool* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f511-119">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f511-120">Bei Erfolg wird ein Verweis auf den resultierenden [**CIM- \_ resourcepool zurückgegeben**](cim-resourcepool.md).</span><span class="sxs-lookup"><span data-stu-id="6f511-120">On success, returns a reference to the resulting [**CIM\_ResourcePool**](cim-resourcepool.md).</span></span> <span data-ttu-id="6f511-121">Wenn ein Auftrag zurückgegeben wird, kann dieser **null** sein. in diesem Fall muss der Client den Auftrag verwenden, um den resultierenden resourcepool nach Abschluss des Auftrags zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6f511-121">When a Job is returned, this may be **NULL**, in which case, the client must use the Job to find the resulting ResourcePool once the Job completes.</span></span>

</dd> <dt>

<span data-ttu-id="6f511-122">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f511-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f511-123">Verweis auf einen [**CIM- \_ concretejob**](cim-concretejob.md) , der den Auftrag darstellt (kann NULL sein, wenn der Auftrag abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="6f511-123">Reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) that represents the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f511-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f511-124">Return value</span></span>

<span data-ttu-id="6f511-125">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6f511-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6f511-126">**Auftrag ohne Fehler abgeschlossen** (0)</span><span class="sxs-lookup"><span data-stu-id="6f511-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-127">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="6f511-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-128">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6f511-128">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-129">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="6f511-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-130">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="6f511-130">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-131">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="6f511-131">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-132">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="6f511-132">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-133">**Falscher ResourceType für den Pool** (7).</span><span class="sxs-lookup"><span data-stu-id="6f511-133">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-134">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="6f511-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-135">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="6f511-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-136">**Größe nicht unterstützt** (4097)</span><span class="sxs-lookup"><span data-stu-id="6f511-136">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-137">**Reservierte Methode** (4098.32767)</span><span class="sxs-lookup"><span data-stu-id="6f511-137">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6f511-138">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="6f511-138">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6f511-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f511-139">Requirements</span></span>



| <span data-ttu-id="6f511-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f511-140">Requirement</span></span> | <span data-ttu-id="6f511-141">Wert</span><span class="sxs-lookup"><span data-stu-id="6f511-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f511-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f511-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6f511-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6f511-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6f511-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f511-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6f511-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6f511-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6f511-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f511-146">Namespace</span></span><br/>                | <span data-ttu-id="6f511-147">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6f511-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6f511-148">MOF</span><span class="sxs-lookup"><span data-stu-id="6f511-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f511-149"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6f511-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f511-150">DLL</span><span class="sxs-lookup"><span data-stu-id="6f511-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f511-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f511-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f511-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f511-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f511-153">**CIM \_ resourcepoolconfigurationservice**</span><span class="sxs-lookup"><span data-stu-id="6f511-153">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




