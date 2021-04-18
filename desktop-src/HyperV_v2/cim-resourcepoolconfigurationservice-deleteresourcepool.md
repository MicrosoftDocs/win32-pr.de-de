---
description: Starten Sie einen Auftrag, um einen Ressourcenpool zu löschen.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Deleteresourcepool-Methode der CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cab27df07a6a3a9679cb5e6595b6ba558d8b05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357371"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="8f38e-103">Deleteresourcepool-Methode der CIM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="8f38e-103">DeleteResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="8f38e-104">Starten Sie einen Auftrag, um einen Ressourcenpool zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8f38e-104">Start a job to delete a resource pool.</span></span> <span data-ttu-id="8f38e-105">Möglicherweise sind keine Zuordnungen ausstehend, oder der Löschvorgang schlägt fehl mit "in Verwendung".</span><span class="sxs-lookup"><span data-stu-id="8f38e-105">No allocations may be outstanding or the delete will fail with "In Use."</span></span> <span data-ttu-id="8f38e-106">Wenn es sich beim Ressourcenpool um einen Stamm Ressourcenpool handelt, werden alle Host Ressourcen an das zugrunde liegende System zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8f38e-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f38e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f38e-107">Syntax</span></span>


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8f38e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f38e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f38e-109">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f38e-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f38e-110">Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) , der auf den zu löschenden Pool verweist.</span><span class="sxs-lookup"><span data-stu-id="8f38e-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references to the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="8f38e-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8f38e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f38e-112">Ein [**CIM- \_ bettejob**](cim-concretejob.md) , der auf den Auftrag verweist (kann **null** sein, wenn der Auftrag abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="8f38e-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f38e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f38e-113">Return value</span></span>

<span data-ttu-id="8f38e-114">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8f38e-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8f38e-115">**Auftrag ohne Fehler abgeschlossen** (0)</span><span class="sxs-lookup"><span data-stu-id="8f38e-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-116">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="8f38e-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-117">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="8f38e-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="8f38e-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-119">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="8f38e-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-120">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="8f38e-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-121">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="8f38e-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-122">**Falscher ResourceType für den Pool** (7).</span><span class="sxs-lookup"><span data-stu-id="8f38e-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="8f38e-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="8f38e-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="8f38e-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8f38e-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="8f38e-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8f38e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f38e-127">Requirements</span></span>



| <span data-ttu-id="8f38e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f38e-128">Requirement</span></span> | <span data-ttu-id="8f38e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8f38e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f38e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f38e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8f38e-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8f38e-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8f38e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f38e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8f38e-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8f38e-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8f38e-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f38e-134">Namespace</span></span><br/>                | <span data-ttu-id="8f38e-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8f38e-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8f38e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8f38e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f38e-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8f38e-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f38e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8f38e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f38e-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8f38e-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8f38e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f38e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f38e-141">**CIM \_ resourcepoolconfigurationservice**</span><span class="sxs-lookup"><span data-stu-id="8f38e-141">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




