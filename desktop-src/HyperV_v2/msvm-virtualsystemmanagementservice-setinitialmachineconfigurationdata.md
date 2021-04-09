---
description: Legt die Konfigurationsdaten für die ersten virtuellen Computer fest.
ms.assetid: 0f174d29-ddb2-4a8c-b664-926245573778
title: Setinitialmachineconfigurationdata-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetInitialMachineConfigurationData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08028358d6bb53406abe15c88e0acd02e748d387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750177"
---
# <a name="setinitialmachineconfigurationdata-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="df1f9-103">Setinitialmachineconfigurationdata-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="df1f9-103">SetInitialMachineConfigurationData method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="df1f9-104">Legt die anfänglichen Computer Konfigurationsdaten eines virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="df1f9-104">Sets a VM's initial machine configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="df1f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df1f9-105">Syntax</span></span>


```mof
uint32 SetInitialMachineConfigurationData(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  uint8                  ImcData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="df1f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df1f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df1f9-107">*TARGETSYSTEM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df1f9-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df1f9-108">Ein Verweis auf das virtuelle Computersystem, auf dem die IMC-Daten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="df1f9-108">A reference to the virtual computer system on which the IMC data will be set.</span></span>

</dd> <dt>

<span data-ttu-id="df1f9-109">*Imcdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df1f9-109">*ImcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df1f9-110">Die festzulegenden IMC-Daten.</span><span class="sxs-lookup"><span data-stu-id="df1f9-110">The IMC data to set.</span></span> <span data-ttu-id="df1f9-111">Die ersten vier Bytes müssen die Länge des Arrays in der Big-d-Reihenfolge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="df1f9-111">The first four bytes must be the length of the array in big-endian order</span></span>

</dd> <dt>

<span data-ttu-id="df1f9-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="df1f9-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df1f9-113">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="df1f9-113">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="df1f9-114">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="df1f9-114">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df1f9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df1f9-115">Return value</span></span>

<span data-ttu-id="df1f9-116">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="df1f9-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="df1f9-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="df1f9-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="df1f9-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="df1f9-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="df1f9-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="df1f9-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="df1f9-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="df1f9-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="df1f9-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="df1f9-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="df1f9-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="df1f9-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="df1f9-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="df1f9-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="df1f9-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="df1f9-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df1f9-130">Requirements</span></span>



| <span data-ttu-id="df1f9-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df1f9-131">Requirement</span></span> | <span data-ttu-id="df1f9-132">Wert</span><span class="sxs-lookup"><span data-stu-id="df1f9-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df1f9-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df1f9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="df1f9-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df1f9-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="df1f9-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df1f9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="df1f9-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="df1f9-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="df1f9-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="df1f9-137">Namespace</span></span><br/>                | <span data-ttu-id="df1f9-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="df1f9-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="df1f9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="df1f9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df1f9-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="df1f9-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df1f9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="df1f9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df1f9-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df1f9-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="df1f9-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df1f9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df1f9-144">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="df1f9-144">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




