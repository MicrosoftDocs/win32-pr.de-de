---
description: Ändert die Ressourcen Einstellungen des übergeordneten Pools für Ressourcen, die einem untergeordneten Pool zugewiesen sind.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Modifypoolresources-Methode der Msvm_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867071"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="9c561-103">Modifypoolresources-Methode der MSVM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="9c561-103">ModifyPoolResources method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="9c561-104">Ändert die Ressourcen Einstellungen des übergeordneten Pools für Ressourcen, die einem untergeordneten Pool zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="9c561-104">Changes the parent pool resource settings for resources assigned to a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c561-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c561-105">Syntax</span></span>


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9c561-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c561-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c561-107">*Childpool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c561-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c561-108">Ein Verweis auf eine Instanz der [**CIM \_ resourcepool**](cim-resourcepool.md) -Klasse, die den zu ändernden untergeordneten Pool darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c561-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="9c561-109">"Parser"- *Pools* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c561-109">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c561-110">Ein Array von [**CIM- \_ resourcepool**](cim-resourcepool.md) -verweisen, die die neuen übergeordneten Pools darstellen, die dem untergeordneten Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c561-110">An array of [**CIM\_ResourcePool**](cim-resourcepool.md) references that represent the new parent pools to assign to the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="9c561-111">*Zuordnung von Einstellungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c561-111">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c561-112">Ein optionales Array von mindestens einer eingebetteten Instanz der [**MSVM \_ resourceallocationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse, die verwendet wird, um die Einstellungen für die Pool Zuordnung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9c561-112">An optional array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span>

</dd> <dt>

<span data-ttu-id="9c561-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9c561-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c561-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="9c561-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c561-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c561-115">Return value</span></span>

<span data-ttu-id="9c561-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9c561-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9c561-117">**Auftrag ohne Fehler abgeschlossen** (0)</span><span class="sxs-lookup"><span data-stu-id="9c561-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-118">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9c561-118">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="9c561-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-120">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="9c561-120">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-121">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="9c561-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-122">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="9c561-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-123">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="9c561-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-124">**Unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="9c561-124">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-125">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="9c561-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-126">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="9c561-126">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-127">**Verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="9c561-127">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-128">**Ungültiger Status** (32775)</span><span class="sxs-lookup"><span data-stu-id="9c561-128">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-129">**Falscher Ressourcentyp für den Pool** (32776).</span><span class="sxs-lookup"><span data-stu-id="9c561-129">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-130">Nicht **verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="9c561-130">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-131">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="9c561-131">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-132">**Anbieter reserviert** (32779)</span><span class="sxs-lookup"><span data-stu-id="9c561-132">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-133">**Unzureichende Ressourcen** (32780)</span><span class="sxs-lookup"><span data-stu-id="9c561-133">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-134">**Objekt nicht gefunden** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="9c561-134">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-135">**Objekt vorhanden** (32788)</span><span class="sxs-lookup"><span data-stu-id="9c561-135">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="9c561-136">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="9c561-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9c561-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c561-137">Requirements</span></span>



| <span data-ttu-id="9c561-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c561-138">Requirement</span></span> | <span data-ttu-id="9c561-139">Wert</span><span class="sxs-lookup"><span data-stu-id="9c561-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c561-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c561-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9c561-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c561-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9c561-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c561-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9c561-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c561-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c561-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c561-144">Namespace</span></span><br/>                | <span data-ttu-id="9c561-145">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9c561-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9c561-146">MOF</span><span class="sxs-lookup"><span data-stu-id="9c561-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c561-147"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9c561-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c561-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9c561-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c561-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c561-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c561-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c561-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c561-151">**MSVM \_ resourcepoolconfigurationservice**</span><span class="sxs-lookup"><span data-stu-id="9c561-151">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

