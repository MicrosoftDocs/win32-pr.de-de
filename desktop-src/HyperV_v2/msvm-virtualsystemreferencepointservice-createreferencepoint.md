---
description: Erstellt einen Referenzpunkt eines virtuellen Systems.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Die Methode "kreatereferencepoint" der Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354908"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="87afe-103">Methode "kreatereferencepoint" der Klasse "MSVM \_ virtualsystemreferencepointservice"</span><span class="sxs-lookup"><span data-stu-id="87afe-103">CreateReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="87afe-104">Erstellt einen Referenzpunkt eines virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="87afe-104">Creates a reference point of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="87afe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87afe-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="87afe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87afe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87afe-107">*Affectedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87afe-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87afe-108">Ein [**MSVM- \_ Computersystem**](msvm-computersystem.md) , das auf das betroffene virtuelle System verweist.</span><span class="sxs-lookup"><span data-stu-id="87afe-108">A [**Msvm\_ComputerSystem**](msvm-computersystem.md) that references the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="87afe-109">*Referencepointsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87afe-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87afe-110">Enthält die Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="87afe-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="87afe-111">*Referencepointtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87afe-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87afe-112">Angeforderter Verweis Punkttyp:</span><span class="sxs-lookup"><span data-stu-id="87afe-112">Requested reference point type:</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="87afe-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Protokoll basiert** (0)</span><span class="sxs-lookup"><span data-stu-id="87afe-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (0)</span></span>


</dt> <dd>

<span data-ttu-id="87afe-114">Basierend auf der Protokoll Verfolgung von Hyper-V-Replikaten.</span><span class="sxs-lookup"><span data-stu-id="87afe-114">Based on Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="87afe-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basierend** (1)</span><span class="sxs-lookup"><span data-stu-id="87afe-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="87afe-116">Basierend auf robusten Änderungsnachverfolgung von virtuellen Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="87afe-116">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="87afe-117">*Resultingreferencepoint* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="87afe-117">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87afe-118">Resultierender virtueller System-Referenzpunkt</span><span class="sxs-lookup"><span data-stu-id="87afe-118">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="87afe-119">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="87afe-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87afe-120">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="87afe-120">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="87afe-121">In diesem Fall wird die Instanz der " [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) "-Klasse, die den neuen virtuellen System Verweis Punkt darstellt, über die [**CIM- \_ affectedjobelements**](cim-affectedjobelement.md) -Zuordnung mit dem Wert der **affectedelta** -Eigenschaft, die auf die neue Instanz der **MSVM \_ virtualsystemreferencepoint** -Klasse verweist, die den Verweis Punkt des virtuellen Systems und den Wert der **elementeffects** auf 5 (Create) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="87afe-121">In this case, the instance of the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) class representing the new virtual system reference point is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **Msvm\_VirtualSystemReferencePoint** class representing the virtual system reference point and the value of the **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87afe-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87afe-122">Return value</span></span>

<span data-ttu-id="87afe-123">Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87afe-123">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="87afe-124">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="87afe-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-125">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="87afe-125">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-126">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="87afe-126">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-127">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="87afe-127">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-128">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="87afe-128">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-129">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="87afe-129">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-130">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="87afe-130">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-131">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="87afe-131">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-132">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="87afe-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-133">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="87afe-133">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="87afe-134">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="87afe-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="87afe-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87afe-135">Requirements</span></span>



| <span data-ttu-id="87afe-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87afe-136">Requirement</span></span> | <span data-ttu-id="87afe-137">Wert</span><span class="sxs-lookup"><span data-stu-id="87afe-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87afe-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87afe-138">Minimum supported client</span></span><br/> | <span data-ttu-id="87afe-139">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87afe-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="87afe-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87afe-140">Minimum supported server</span></span><br/> | <span data-ttu-id="87afe-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="87afe-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="87afe-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="87afe-142">Namespace</span></span><br/>                | <span data-ttu-id="87afe-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="87afe-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="87afe-144">MOF</span><span class="sxs-lookup"><span data-stu-id="87afe-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87afe-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="87afe-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87afe-146">DLL</span><span class="sxs-lookup"><span data-stu-id="87afe-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87afe-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87afe-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87afe-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87afe-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87afe-149">**MSVM \_ virtualsystemreferencepointservice**</span><span class="sxs-lookup"><span data-stu-id="87afe-149">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




