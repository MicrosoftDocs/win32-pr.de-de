---
description: Erstellt einen untergeordneten Ressourcenpool.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Die Methode "kreatepool" der Msvm_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360654"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="368fa-103">Die Methode "kreatepool" der Klasse "MSVM \_ resourcepoolconfigurationservice"</span><span class="sxs-lookup"><span data-stu-id="368fa-103">CreatePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="368fa-104">Erstellt einen untergeordneten Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="368fa-104">Creates a child resource pool.</span></span> <span data-ttu-id="368fa-105">Der Ressourcenpool wird auf dasselbe System wie dieser Dienst beschränkt.</span><span class="sxs-lookup"><span data-stu-id="368fa-105">The resource pool will be scoped to the same System as this Service.</span></span> <span data-ttu-id="368fa-106">Der sich ergebende Pool ist ein untergeordneter Pool.</span><span class="sxs-lookup"><span data-stu-id="368fa-106">The resulting pool will be a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="368fa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="368fa-107">Syntax</span></span>


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="368fa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="368fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="368fa-109">*Poolsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="368fa-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368fa-110">Eine eingebettete Instanz der [**MSVM \_ resourcepoolsettingdata**](msvm-resourcepoolsettingdata.md) -Klasse, die verwendet wird, um die Pool Einstellungen anzugeben, die nicht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="368fa-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the pool settings that are not allocation related.</span></span>

</dd> <dt>

<span data-ttu-id="368fa-111">"Parser"- *Pools* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="368fa-111">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368fa-112">Ein Array von [**MSVM- \_ resourcepool**](msvm-resourcepool.md) -verweisen, die den Pool oder die Pools darstellen, aus denen der neue Pool erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="368fa-112">An array of [**Msvm\_ResourcePool**](msvm-resourcepool.md) references that represent the pool or pools from which to create the new pool.</span></span>

</dd> <dt>

<span data-ttu-id="368fa-113">*Zuordnung von Einstellungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="368fa-113">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368fa-114">Ein Array aus mindestens einer eingebetteten Instanz der [**MSVM \_ resourceallocationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse, die verwendet wird, um die Einstellungen für die Pool Zuordnung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="368fa-114">An array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span> <span data-ttu-id="368fa-115">Dieses Array muss entweder ein-Element für jedes Element im *parentpools* -Array oder genau ein Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="368fa-115">This array must contain either one element for each element in the *ParentPools* array, or exactly one element.</span></span> <span data-ttu-id="368fa-116">Wenn dieses Array ein Element enthält und *parentpools* mehr als ein Element enthält, gibt *alllocationsettings* eine freigegebene Kapazitäts Zuordnung an, die von einem der übergeordneten Pools erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="368fa-116">If this array contains one element and *ParentPools* contains more than one element, *AlllocationSettings* specifies a shared capacity allocation that can be satisfied by any of the parent pools.</span></span>

<span data-ttu-id="368fa-117">Hiermit werden die Ressourcen, die vom untergeordneten dem Pool zugewiesen werden können, auf eine niedrigere Grenze beschränkt als die von den übergeordneten Elementen bereitgestellte Aggregat Kapazität.</span><span class="sxs-lookup"><span data-stu-id="368fa-117">This is used to restrict the resources that can be allocated from the child to the pool to a lower limit than the aggregate capacity provided by its parents.</span></span> <span data-ttu-id="368fa-118">Diese Option wird nicht von allen Ressourcentypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="368fa-118">This option is not supported by all resource types.</span></span> <span data-ttu-id="368fa-119">Wenn ein Ressourcentyp keine freigegebene Kapazitäts Zuordnung unterstützt, gibt diese Methode 32770 zurück (wird nicht unterstützt).</span><span class="sxs-lookup"><span data-stu-id="368fa-119">If a resource type does not support shared capacity allocation, this method will return 32770 (Not Supported).</span></span>

</dd> <dt>

<span data-ttu-id="368fa-120">*Pool* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="368fa-120">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="368fa-121">Ein Verweis auf den resultierenden Pool.</span><span class="sxs-lookup"><span data-stu-id="368fa-121">A reference to the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="368fa-122">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="368fa-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="368fa-123">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="368fa-123">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="368fa-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="368fa-124">Return value</span></span>

<span data-ttu-id="368fa-125">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="368fa-125">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="368fa-126">**Auftrag ohne Fehler abgeschlossen** (0)</span><span class="sxs-lookup"><span data-stu-id="368fa-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-127">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="368fa-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-128">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="368fa-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-129">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="368fa-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-130">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="368fa-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-131">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="368fa-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-132">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="368fa-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-133">**Unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="368fa-133">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-134">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="368fa-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-135">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="368fa-135">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-136">**Verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="368fa-136">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-137">**Ungültiger Status** (32775)</span><span class="sxs-lookup"><span data-stu-id="368fa-137">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-138">**Falscher Ressourcentyp für den Pool** (32776).</span><span class="sxs-lookup"><span data-stu-id="368fa-138">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-139">Nicht **verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="368fa-139">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-140">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="368fa-140">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-141">**Anbieter reserviert** (32779)</span><span class="sxs-lookup"><span data-stu-id="368fa-141">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-142">**Unzureichende Ressourcen** (32780)</span><span class="sxs-lookup"><span data-stu-id="368fa-142">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-143">**Objekt nicht gefunden** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="368fa-143">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-144">**Objekt vorhanden** (32788)</span><span class="sxs-lookup"><span data-stu-id="368fa-144">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="368fa-145">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="368fa-145">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="368fa-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="368fa-146">Requirements</span></span>



| <span data-ttu-id="368fa-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="368fa-147">Requirement</span></span> | <span data-ttu-id="368fa-148">Wert</span><span class="sxs-lookup"><span data-stu-id="368fa-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="368fa-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="368fa-149">Minimum supported client</span></span><br/> | <span data-ttu-id="368fa-150">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="368fa-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="368fa-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="368fa-151">Minimum supported server</span></span><br/> | <span data-ttu-id="368fa-152">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="368fa-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="368fa-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="368fa-153">Namespace</span></span><br/>                | <span data-ttu-id="368fa-154">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="368fa-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="368fa-155">MOF</span><span class="sxs-lookup"><span data-stu-id="368fa-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="368fa-156"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="368fa-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="368fa-157">DLL</span><span class="sxs-lookup"><span data-stu-id="368fa-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="368fa-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="368fa-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="368fa-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="368fa-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="368fa-160">**MSVM \_ resourcepoolconfigurationservice**</span><span class="sxs-lookup"><span data-stu-id="368fa-160">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

