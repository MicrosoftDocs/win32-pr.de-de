---
description: Löscht einen Ressourcenpool.
ms.assetid: bc3111a4-9687-49ec-890e-190358230c53
title: Deletepool-Methode der Msvm_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.DeletePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 84273daa0aa30dca8722d90d4fcec22b88325bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364097"
---
# <a name="deletepool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="0b109-103">Deletepool-Methode der MSVM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0b109-103">DeletePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="0b109-104">Löscht einen Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="0b109-104">Deletes a resource pool.</span></span> <span data-ttu-id="0b109-105">Zum erfolgreichen Löschen eines Ressourcenpools können keine Zuordnungen ausstehend sein, oder der Löschvorgang schlägt mit 32774 (in Verwendung) fehl.</span><span class="sxs-lookup"><span data-stu-id="0b109-105">To successfully delete a resource pool, no allocations can be outstanding or the delete will fail with 32774 (In Use).</span></span> <span data-ttu-id="0b109-106">Wenn es sich beim Ressourcenpool um einen Stamm Ressourcenpool handelt, werden alle Host Ressourcen an das zugrunde liegende System zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b109-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b109-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b109-107">Syntax</span></span>


```mof
uint32 DeletePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0b109-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b109-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b109-109">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b109-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b109-110">Ein Verweis auf eine Instanz der [**CIM \_ resourcepool**](cim-resourcepool.md) -Klasse, die den zu löschenden Pool darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b109-110">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="0b109-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b109-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b109-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0b109-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b109-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b109-113">Return value</span></span>

<span data-ttu-id="0b109-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0b109-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0b109-115">**Auftrag ohne Fehler abgeschlossen** (0)</span><span class="sxs-lookup"><span data-stu-id="0b109-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-116">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0b109-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="0b109-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-118">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="0b109-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="0b109-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="0b109-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="0b109-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-122">**Unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="0b109-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="0b109-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="0b109-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-125">**Verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="0b109-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-126">**Ungültiger Status** (32775)</span><span class="sxs-lookup"><span data-stu-id="0b109-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-127">**Falscher Ressourcentyp für den Pool** (32776).</span><span class="sxs-lookup"><span data-stu-id="0b109-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-128">Nicht **verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="0b109-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="0b109-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-130">**Anbieter reserviert** (32779)</span><span class="sxs-lookup"><span data-stu-id="0b109-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-131">**Unzureichende Ressourcen** (32780)</span><span class="sxs-lookup"><span data-stu-id="0b109-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-132">**Objekt nicht gefunden** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="0b109-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-133">**Objekt vorhanden** (32788)</span><span class="sxs-lookup"><span data-stu-id="0b109-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="0b109-134">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="0b109-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0b109-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b109-135">Requirements</span></span>



| <span data-ttu-id="0b109-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b109-136">Requirement</span></span> | <span data-ttu-id="0b109-137">Wert</span><span class="sxs-lookup"><span data-stu-id="0b109-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b109-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b109-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0b109-139">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b109-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0b109-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b109-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0b109-141">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b109-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b109-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b109-142">Namespace</span></span><br/>                | <span data-ttu-id="0b109-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0b109-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0b109-144">MOF</span><span class="sxs-lookup"><span data-stu-id="0b109-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b109-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0b109-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b109-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0b109-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b109-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b109-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b109-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b109-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b109-149">**MSVM \_ resourcepoolconfigurationservice**</span><span class="sxs-lookup"><span data-stu-id="0b109-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

