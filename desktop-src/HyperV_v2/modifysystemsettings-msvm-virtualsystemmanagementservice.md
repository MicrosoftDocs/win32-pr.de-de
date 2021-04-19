---
description: Ändert die Einstellungen der virtuellen Maschine.
ms.assetid: 3266bd0d-398b-4d3b-9248-e29c069aab11
title: Modifysystemsettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4e6bf40b3dd206affcdc014e98554bfa8f88b4c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362836"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="1a4c4-103">Modifysystemsettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="1a4c4-103">ModifySystemSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1a4c4-104">Ändert die Einstellungen der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1a4c4-104">Modifies virtual machine settings.</span></span> <span data-ttu-id="1a4c4-105">Wenn Sie auf die Systemeinstellungen einer "aktuellen" VM-Konfiguration angewendet werden, kann die virtuelle Computer Instanz als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1a4c4-105">When applied to the system settings of a "current" virtual machine configuration, as a side effect the virtual machine instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a4c4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a4c4-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1a4c4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a4c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a4c4-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a4c4-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a4c4-109">Eine eingebettete Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die die geänderten Aspekte der virtuellen Maschine enthält.</span><span class="sxs-lookup"><span data-stu-id="1a4c4-109">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that contains the modified aspects of the virtual machine.</span></span> <span data-ttu-id="1a4c4-110">Die **InstanceId-** Eigenschaft identifiziert die Einstellung für den virtuellen Computer, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a4c4-110">The **InstanceID** property identifies the virtual machine setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="1a4c4-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1a4c4-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a4c4-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="1a4c4-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a4c4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a4c4-113">Return value</span></span>

<span data-ttu-id="1a4c4-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="1a4c4-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1a4c4-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-116">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-117">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="1a4c4-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-119">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-120">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-121">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-124">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1a4c4-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1a4c4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a4c4-126">Requirements</span></span>



| <span data-ttu-id="1a4c4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a4c4-127">Requirement</span></span> | <span data-ttu-id="1a4c4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1a4c4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4c4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1a4c4-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a4c4-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1a4c4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a4c4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1a4c4-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a4c4-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a4c4-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a4c4-133">Namespace</span></span><br/>                | <span data-ttu-id="1a4c4-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1a4c4-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1a4c4-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1a4c4-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a4c4-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1a4c4-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a4c4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1a4c4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a4c4-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a4c4-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a4c4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a4c4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a4c4-140">**Modifyvirtualsystem (v1)**</span><span class="sxs-lookup"><span data-stu-id="1a4c4-140">**ModifyVirtualSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystem-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="1a4c4-141">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="1a4c4-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

