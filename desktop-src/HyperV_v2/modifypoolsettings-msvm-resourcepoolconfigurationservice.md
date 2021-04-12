---
description: Ändert die Einstellungen eines untergeordneten Pools, die nicht zugeordnet sind.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Modifypoolsettings-Methode der Msvm_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217185"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="18e02-103">Modifypoolsettings-Methode der MSVM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="18e02-103">ModifyPoolSettings method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="18e02-104">Ändert die Einstellungen eines untergeordneten Pools, die nicht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="18e02-104">Changes the settings of a child pool that are not allocation related.</span></span>

## <a name="syntax"></a><span data-ttu-id="18e02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18e02-105">Syntax</span></span>


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="18e02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="18e02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18e02-107">*Childpool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18e02-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e02-108">Ein Verweis auf eine Instanz der [**CIM \_ resourcepool**](cim-resourcepool.md) -Klasse, die den zu ändernden untergeordneten Pool darstellt.</span><span class="sxs-lookup"><span data-stu-id="18e02-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="18e02-109">*Poolsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18e02-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e02-110">Eine eingebettete Instanz der [**MSVM \_ resourcepoolsettingdata**](msvm-resourcepoolsettingdata.md) -Klasse, die verwendet wird, um die neuen Einstellungen für den Pool anzugeben.</span><span class="sxs-lookup"><span data-stu-id="18e02-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the new settings for the pool.</span></span>

</dd> <dt>

<span data-ttu-id="18e02-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="18e02-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18e02-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="18e02-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18e02-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18e02-113">Return value</span></span>

<span data-ttu-id="18e02-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="18e02-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="18e02-115">**Auftrag ohne Fehler abgeschlossen** (0)</span><span class="sxs-lookup"><span data-stu-id="18e02-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-116">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="18e02-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="18e02-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-118">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="18e02-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="18e02-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="18e02-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="18e02-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-122">**Unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="18e02-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="18e02-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="18e02-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-125">**Verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="18e02-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-126">**Ungültiger Status** (32775)</span><span class="sxs-lookup"><span data-stu-id="18e02-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-127">**Falscher Ressourcentyp für den Pool** (32776).</span><span class="sxs-lookup"><span data-stu-id="18e02-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-128">Nicht **verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="18e02-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="18e02-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-130">**Anbieter reserviert** (32779)</span><span class="sxs-lookup"><span data-stu-id="18e02-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-131">**Unzureichende Ressourcen** (32780)</span><span class="sxs-lookup"><span data-stu-id="18e02-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-132">**Objekt nicht gefunden** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="18e02-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-133">**Objekt vorhanden** (32788)</span><span class="sxs-lookup"><span data-stu-id="18e02-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="18e02-134">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="18e02-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="18e02-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18e02-135">Requirements</span></span>



| <span data-ttu-id="18e02-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18e02-136">Requirement</span></span> | <span data-ttu-id="18e02-137">Wert</span><span class="sxs-lookup"><span data-stu-id="18e02-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e02-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18e02-138">Minimum supported client</span></span><br/> | <span data-ttu-id="18e02-139">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18e02-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="18e02-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18e02-140">Minimum supported server</span></span><br/> | <span data-ttu-id="18e02-141">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18e02-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18e02-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="18e02-142">Namespace</span></span><br/>                | <span data-ttu-id="18e02-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="18e02-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="18e02-144">MOF</span><span class="sxs-lookup"><span data-stu-id="18e02-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18e02-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="18e02-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18e02-146">DLL</span><span class="sxs-lookup"><span data-stu-id="18e02-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18e02-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18e02-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18e02-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18e02-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e02-149">**MSVM \_ resourcepoolconfigurationservice**</span><span class="sxs-lookup"><span data-stu-id="18e02-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

