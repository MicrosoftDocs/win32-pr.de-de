---
description: Startet einen Auftrag, um einen übergeordneten Pool mithilfe der angegebenen Zuordnungs Einstellungen zu ändern.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Changesamentresourcepool-Methode der CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359874"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="2b59b-103">Changesamentresourcepool-Methode der CIM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="2b59b-103">ChangeParentResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="2b59b-104">Startet einen Auftrag, um einen übergeordneten Pool mithilfe der angegebenen Zuordnungs Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2b59b-104">Start a job to change a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b59b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b59b-105">Syntax</span></span>


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2b59b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b59b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b59b-107">*Childpool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b59b-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b59b-108">Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) , der auf den untergeordneten Pool verweist.</span><span class="sxs-lookup"><span data-stu-id="2b59b-108">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="2b59b-109">*Pool Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b59b-109">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b59b-110">Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) -Array, das auf den übergeordneten Pool (n) verweist.</span><span class="sxs-lookup"><span data-stu-id="2b59b-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) array that references the parent pool(s).</span></span>

</dd> <dt>

<span data-ttu-id="2b59b-111">*Einstellungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b59b-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b59b-112">Eine optionale Zeichenfolge, die eine Darstellung einer [**CIM \_ SettingData**](cim-settingdata.md) -Instanz enthält, die verwendet wird, um die Einstellungen für den übergeordneten Pool anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2b59b-112">Optional string containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the parent pool.</span></span>

</dd> <dt>

<span data-ttu-id="2b59b-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2b59b-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b59b-114">Ein [**CIM- \_ bettejob**](cim-concretejob.md) , der auf den Auftrag verweist (kann **null** sein, wenn der Auftrag abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="2b59b-114">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b59b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b59b-115">Return value</span></span>

<span data-ttu-id="2b59b-116">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b59b-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2b59b-117">**Auftrag ohne Fehler abgeschlossen** (0)</span><span class="sxs-lookup"><span data-stu-id="2b59b-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-118">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="2b59b-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-119">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="2b59b-119">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="2b59b-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-121">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="2b59b-121">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-122">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="2b59b-122">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-123">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="2b59b-123">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-124">**Falscher ResourceType für den Pool** (7).</span><span class="sxs-lookup"><span data-stu-id="2b59b-124">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-125">**Unzureichende Ressourcen** (8)</span><span class="sxs-lookup"><span data-stu-id="2b59b-125">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-126">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="2b59b-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-127">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="2b59b-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-128">**Größe nicht unterstützt** (4097)</span><span class="sxs-lookup"><span data-stu-id="2b59b-128">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-129">**Reservierte Methode** (4098.32767)</span><span class="sxs-lookup"><span data-stu-id="2b59b-129">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2b59b-130">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="2b59b-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2b59b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b59b-131">Requirements</span></span>



| <span data-ttu-id="2b59b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b59b-132">Requirement</span></span> | <span data-ttu-id="2b59b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2b59b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b59b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b59b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2b59b-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2b59b-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2b59b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b59b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2b59b-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2b59b-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2b59b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b59b-138">Namespace</span></span><br/>                | <span data-ttu-id="2b59b-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2b59b-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2b59b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2b59b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b59b-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2b59b-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b59b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2b59b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b59b-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b59b-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b59b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b59b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b59b-145">**CIM \_ resourcepoolconfigurationservice**</span><span class="sxs-lookup"><span data-stu-id="2b59b-145">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




