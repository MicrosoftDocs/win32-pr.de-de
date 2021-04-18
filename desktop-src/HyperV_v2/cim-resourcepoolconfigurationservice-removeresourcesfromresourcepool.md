---
description: Startet einen Auftrag, um Ressourcen aus einem Ressourcenpool zu entfernen.
ms.assetid: 1689ccbf-a524-45b7-bf95-6341a3b28f6c
title: Removeresourcesfromresourcepool-Methode der CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.RemoveResourcesFromResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41c8a7d1608b9c4d5ea629aa9c053e022d59d9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526783"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="1efe6-103">Removeresourcesfromresourcepool-Methode der CIM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="1efe6-103">RemoveResourcesFromResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="1efe6-104">Startet einen Auftrag, um Ressourcen aus einem Ressourcenpool zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="1efe6-104">Starts a job to remove resources from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="1efe6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1efe6-105">Syntax</span></span>


```mof
uint32 RemoveResourcesFromResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1efe6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1efe6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1efe6-107">" *Hustresources* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="1efe6-107">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1efe6-108">Array von [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Instanzen, die aus dem Pool entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1efe6-108">Array of [**CIM\_LogicalDevice**](cim-logicaldevice.md) instances to remove from the pool.</span></span>

</dd> <dt>

<span data-ttu-id="1efe6-109">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1efe6-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1efe6-110">Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) , der den Pool darstellt, aus dem die Ressourcen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1efe6-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) representing the pool to remove the resources from.</span></span>

</dd> <dt>

<span data-ttu-id="1efe6-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1efe6-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1efe6-112">Ein [**CIM- \_ bettejob**](cim-concretejob.md) , der auf den Auftrag verweist (kann **null** sein, wenn der Auftrag abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="1efe6-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1efe6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1efe6-113">Return value</span></span>

<span data-ttu-id="1efe6-114">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1efe6-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1efe6-115">**Auftrag ohne Fehler abgeschlossen** (0)</span><span class="sxs-lookup"><span data-stu-id="1efe6-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-116">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="1efe6-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-117">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="1efe6-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="1efe6-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-119">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="1efe6-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-120">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="1efe6-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-121">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="1efe6-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-122">**Falscher ResourceType für den Pool** (7).</span><span class="sxs-lookup"><span data-stu-id="1efe6-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1efe6-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="1efe6-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-125">**Größe nicht unterstützt** (4097)</span><span class="sxs-lookup"><span data-stu-id="1efe6-125">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-126">**Reservierte Methode** (4098.32767)</span><span class="sxs-lookup"><span data-stu-id="1efe6-126">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1efe6-127">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="1efe6-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1efe6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1efe6-128">Requirements</span></span>



| <span data-ttu-id="1efe6-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1efe6-129">Requirement</span></span> | <span data-ttu-id="1efe6-130">Wert</span><span class="sxs-lookup"><span data-stu-id="1efe6-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1efe6-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1efe6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1efe6-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1efe6-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1efe6-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1efe6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1efe6-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1efe6-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1efe6-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="1efe6-135">Namespace</span></span><br/>                | <span data-ttu-id="1efe6-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1efe6-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1efe6-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1efe6-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1efe6-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1efe6-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1efe6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1efe6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1efe6-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1efe6-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1efe6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1efe6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1efe6-142">**CIM \_ resourcepoolconfigurationservice**</span><span class="sxs-lookup"><span data-stu-id="1efe6-142">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




