---
description: Ändert die generischen Systemkomponenten Einstellungen.
ms.assetid: e745be32-c26a-4343-99c8-950788243adf
title: Modifysystemcomponentsettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9495256d1b7610bebdac1fb2cc8b70960a63304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346904"
---
# <a name="modifysystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a9a41-103">Modifysystemcomponentsettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="a9a41-103">ModifySystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a9a41-104">Ändert die generischen Systemkomponenten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="a9a41-104">Modifies generic system component settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a41-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9a41-105">Syntax</span></span>


```mof
uint32 ModifySystemComponentSettings(
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a9a41-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9a41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a41-107">*Componentsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9a41-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a41-108">Ein Array von zu aktualisierenden Komponenten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="a9a41-108">An array of component settings to update.</span></span>

</dd> <dt>

<span data-ttu-id="a9a41-109">*Resultingcomponentsettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a9a41-109">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a41-110">Bei Erfolg wird ein Array von [**MSVM \_ systemcomponentsettingdata**](msvm-systemcomponentsettingdata.md) zurückgegeben, das auf die resultierenden Komponenten Einstellungen verweist.</span><span class="sxs-lookup"><span data-stu-id="a9a41-110">On success, returns an array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="a9a41-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a9a41-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a41-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a9a41-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a41-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9a41-113">Return value</span></span>

<span data-ttu-id="a9a41-114">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9a41-114">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a9a41-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="a9a41-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-116">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="a9a41-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-117">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="a9a41-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="a9a41-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-119">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="a9a41-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-120">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="a9a41-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-121">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="a9a41-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="a9a41-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="a9a41-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-124">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="a9a41-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a9a41-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="a9a41-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a9a41-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9a41-126">Requirements</span></span>



| <span data-ttu-id="a9a41-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9a41-127">Requirement</span></span> | <span data-ttu-id="a9a41-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a9a41-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a41-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9a41-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a41-130">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9a41-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9a41-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9a41-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a41-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a9a41-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a9a41-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9a41-133">Namespace</span></span><br/>                | <span data-ttu-id="a9a41-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a9a41-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a9a41-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a9a41-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9a41-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a9a41-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9a41-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a9a41-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9a41-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9a41-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9a41-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9a41-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a41-140">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="a9a41-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

