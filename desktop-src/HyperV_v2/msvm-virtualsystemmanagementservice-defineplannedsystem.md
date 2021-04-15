---
description: Definiert ein geplantes virtuelles System.
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: Defineplannedsystem-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d5e9fa8a49e86850d044216a3d95e3d4dd756fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525205"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="9275c-103">Defineplannedsystem-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="9275c-103">DefinePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="9275c-104">Definiert ein geplantes virtuelles System.</span><span class="sxs-lookup"><span data-stu-id="9275c-104">Defines a planned virtual system.</span></span>

<span data-ttu-id="9275c-105">Eingaben, die nicht vollständig angegeben sind, können mit Standardwerten aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="9275c-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9275c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9275c-106">Syntax</span></span>


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9275c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9275c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9275c-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9275c-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9275c-109">Die Systemeinstellungen für das virtuelle System.</span><span class="sxs-lookup"><span data-stu-id="9275c-109">The system settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="9275c-110">*Resourcesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9275c-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9275c-111">Die Ressourcen Einstellungen für das virtuelle System.</span><span class="sxs-lookup"><span data-stu-id="9275c-111">The resource settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="9275c-112">*Referenceconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9275c-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9275c-113">Ein [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) , das die Verweis Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="9275c-113">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the reference configuration.</span></span>

</dd> <dt>

<span data-ttu-id="9275c-114">*Resultingsystem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9275c-114">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9275c-115">Ein [**CIM- \_ Computersystem**](cim-computersystem.md) , das das resultierende System enthält.</span><span class="sxs-lookup"><span data-stu-id="9275c-115">A [**CIM\_ComputerSystem**](cim-computersystem.md) containing the resulting system.</span></span>

</dd> <dt>

<span data-ttu-id="9275c-116">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9275c-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9275c-117">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="9275c-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9275c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9275c-118">Return value</span></span>

<span data-ttu-id="9275c-119">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9275c-119">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9275c-120">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="9275c-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9275c-121">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="9275c-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9275c-122">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="9275c-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9275c-123">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="9275c-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9275c-124">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="9275c-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9275c-125">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="9275c-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9275c-126">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="9275c-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9275c-127">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="9275c-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9275c-128">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="9275c-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9275c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9275c-129">Requirements</span></span>



| <span data-ttu-id="9275c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9275c-130">Requirement</span></span> | <span data-ttu-id="9275c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9275c-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9275c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9275c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9275c-133">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9275c-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9275c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9275c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9275c-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9275c-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9275c-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="9275c-136">Namespace</span></span><br/>                | <span data-ttu-id="9275c-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9275c-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9275c-138">MOF</span><span class="sxs-lookup"><span data-stu-id="9275c-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9275c-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9275c-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9275c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9275c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9275c-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9275c-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9275c-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9275c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9275c-143">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="9275c-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

