---
description: Starten Sie einen Auftrag, um einen untergeordneten Pool aus einem übergeordneten Pool mithilfe der angegebenen Zuordnungs Einstellungen zu erstellen.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Methode "kreatechildresourcepool" der CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356797"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="b8330-103">Methode "kreatechildresourcepool" der CIM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b8330-103">CreateChildResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="b8330-104">Starten Sie einen Auftrag, um einen untergeordneten Pool aus einem übergeordneten Pool mithilfe der angegebenen Zuordnungs Einstellungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8330-104">Start a job to create a sub-pool from a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8330-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8330-105">Syntax</span></span>


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b8330-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8330-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8330-107">*ElementName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8330-107">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8330-108">Ein Endbenutzer relevanter Name für den Pool, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b8330-108">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="b8330-109">Wenn der Wert **null** ist, kann ein vom System bereitgestellter Standardname verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8330-109">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="b8330-110">Der Wert wird in der **ElementName** -Eigenschaft für das erstellte Element gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b8330-110">The value will be stored in the **ElementName** property for the created element.</span></span>

</dd> <dt>

<span data-ttu-id="b8330-111">*Einstellungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8330-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8330-112">Eine Zeichenfolge, die eine-Darstellung einer [**CIM \_ SettingData**](cim-settingdata.md) -Instanz enthält, die verwendet wird, um die Einstellungen für den untergeordneten Pool anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b8330-112">String containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the child Pool.</span></span>

</dd> <dt>

<span data-ttu-id="b8330-113">*Pool Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8330-113">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8330-114">Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) , aus dem der neue Pool erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8330-114">A [**CIM\_ResourcePool**](cim-resourcepool.md) from which to create the new Pool.</span></span>

</dd> <dt>

<span data-ttu-id="b8330-115">*Pool* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b8330-115">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8330-116">Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) , der auf den resultierenden Pool verweist.</span><span class="sxs-lookup"><span data-stu-id="b8330-116">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="b8330-117">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b8330-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8330-118">Verweis auf den Auftrag (kann NULL sein, wenn der Auftrag abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="b8330-118">Reference to the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8330-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8330-119">Return value</span></span>

<span data-ttu-id="b8330-120">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b8330-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b8330-121">**Auftrag ohne Fehler abgeschlossen** (0)</span><span class="sxs-lookup"><span data-stu-id="b8330-121">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-122">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b8330-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-123">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b8330-123">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-124">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="b8330-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-125">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="b8330-125">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-126">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="b8330-126">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-127">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="b8330-127">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-128">**Falscher ResourceType für den Pool** (7).</span><span class="sxs-lookup"><span data-stu-id="b8330-128">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-129">**Unzureichende Ressourcen** (8)</span><span class="sxs-lookup"><span data-stu-id="b8330-129">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-130">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="b8330-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-131">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="b8330-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-132">**Größe nicht unterstützt** (4097)</span><span class="sxs-lookup"><span data-stu-id="b8330-132">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-133">**Reservierte Methode** (4098.32767)</span><span class="sxs-lookup"><span data-stu-id="b8330-133">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b8330-134">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="b8330-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b8330-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8330-135">Requirements</span></span>



| <span data-ttu-id="b8330-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8330-136">Requirement</span></span> | <span data-ttu-id="b8330-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b8330-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8330-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8330-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b8330-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b8330-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b8330-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8330-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b8330-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b8330-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b8330-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8330-142">Namespace</span></span><br/>                | <span data-ttu-id="b8330-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b8330-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b8330-144">MOF</span><span class="sxs-lookup"><span data-stu-id="b8330-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8330-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b8330-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8330-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b8330-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8330-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8330-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8330-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8330-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8330-149">**CIM \_ resourcepoolconfigurationservice**</span><span class="sxs-lookup"><span data-stu-id="b8330-149">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




