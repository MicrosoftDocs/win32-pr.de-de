---
description: Entfernt generische Komponenten Einstellungen aus einer virtuellen Systemkonfiguration.
ms.assetid: 54ddb960-65b7-409d-ad80-f3685562a1a1
title: Removesystemcomponentsettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93ef7b794b901212fad72a1fcdf6223d8344b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344256"
---
# <a name="removesystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="42b6e-103">Removesystemcomponentsettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="42b6e-103">RemoveSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="42b6e-104">Entfernt generische Komponenten Einstellungen aus einer virtuellen Systemkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="42b6e-104">Removes generic component settings from a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42b6e-105">Syntax</span></span>


```mof
uint32 RemoveSystemComponentSettings(
  [in]  Msvm_SystemComponentSettingData REF ComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="42b6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42b6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42b6e-107">*Componentsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42b6e-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b6e-108">Array von [**MSVM \_ systemcomponentsettingdata**](msvm-systemcomponentsettingdata.md) , das auf die zu entfernenden Komponenten Einstellungen verweist.</span><span class="sxs-lookup"><span data-stu-id="42b6e-108">Array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the component settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="42b6e-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="42b6e-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42b6e-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="42b6e-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42b6e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42b6e-111">Return value</span></span>

<span data-ttu-id="42b6e-112">Gibt bei Erfolg 0 oder 4096 zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="42b6e-112">Returns 0 or 4096 on a success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="42b6e-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="42b6e-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42b6e-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="42b6e-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="42b6e-115">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="42b6e-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="42b6e-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="42b6e-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="42b6e-117">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="42b6e-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="42b6e-118">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="42b6e-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="42b6e-119">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="42b6e-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="42b6e-120">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="42b6e-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="42b6e-121">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="42b6e-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="42b6e-122">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="42b6e-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="42b6e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42b6e-123">Requirements</span></span>



| <span data-ttu-id="42b6e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42b6e-124">Requirement</span></span> | <span data-ttu-id="42b6e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="42b6e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b6e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42b6e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42b6e-127">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42b6e-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="42b6e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42b6e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42b6e-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="42b6e-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="42b6e-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="42b6e-130">Namespace</span></span><br/>                | <span data-ttu-id="42b6e-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="42b6e-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="42b6e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="42b6e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42b6e-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="42b6e-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42b6e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="42b6e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42b6e-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42b6e-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42b6e-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42b6e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b6e-137">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="42b6e-137">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

