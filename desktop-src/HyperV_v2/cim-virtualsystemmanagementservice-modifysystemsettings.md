---
description: Ändert die Einstellungen des virtuellen Systems.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: Modifysystemsettings-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da610d03e683b06ad743d1b6d4fe413dc5b31d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959404"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="db074-103">Modifysystemsettings-Methode der CIM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="db074-103">ModifySystemSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="db074-104">Ändert die Einstellungen des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="db074-104">Modifies virtual system settings.</span></span>

<span data-ttu-id="db074-105">Wenn Sie auf die Systemeinstellungen einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, kann die virtuelle System Instanz als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="db074-105">When applied to the system settings of a "current" virtual system configuration, as a side effect the virtual system instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="db074-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="db074-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="db074-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="db074-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db074-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db074-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db074-109">Eine Zeichenfolge, die eine Instanz der Klasse [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) enthält, die zum Ändern der Einstellungen des virtuellen Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db074-109">String containing an instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to modify the settings of the virtual system.</span></span> <span data-ttu-id="db074-110">Die Instanz muss eine gültige **InstanceId** aufweisen, um die zu ändernde Einstellung des virtuellen Systems zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="db074-110">The instance must have a valid **InstanceID** in order to identify the virtual system setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="db074-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db074-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db074-112">Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="db074-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db074-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db074-113">Return value</span></span>

<span data-ttu-id="db074-114">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db074-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="db074-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="db074-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="db074-116">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="db074-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="db074-117">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="db074-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="db074-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="db074-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="db074-119">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="db074-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="db074-120">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="db074-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="db074-121">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="db074-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="db074-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="db074-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="db074-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="db074-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="db074-124">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="db074-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="db074-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="db074-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="db074-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db074-126">Requirements</span></span>



| <span data-ttu-id="db074-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db074-127">Requirement</span></span> | <span data-ttu-id="db074-128">Wert</span><span class="sxs-lookup"><span data-stu-id="db074-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db074-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db074-129">Minimum supported client</span></span><br/> | <span data-ttu-id="db074-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="db074-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="db074-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db074-131">Minimum supported server</span></span><br/> | <span data-ttu-id="db074-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="db074-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="db074-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="db074-133">Namespace</span></span><br/>                | <span data-ttu-id="db074-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="db074-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="db074-135">MOF</span><span class="sxs-lookup"><span data-stu-id="db074-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db074-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="db074-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="db074-137">DLL</span><span class="sxs-lookup"><span data-stu-id="db074-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db074-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="db074-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="db074-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db074-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db074-140">**CIM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="db074-140">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




