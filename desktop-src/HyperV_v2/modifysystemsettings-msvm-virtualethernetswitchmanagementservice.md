---
description: Ändert Einstellungen für virtuelle Switches.
ms.assetid: 8d323578-990f-483c-8515-8a21479767b1
title: Modifysystemsettings-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3512debfd6d49e3c09cb8a508a7f0d748ab128e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347519"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="f9a82-103">Modifysystemsettings-Methode der MSVM \_ virtualethernetzwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="f9a82-103">ModifySystemSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="f9a82-104">Ändert Einstellungen für virtuelle Switches.</span><span class="sxs-lookup"><span data-stu-id="f9a82-104">Modifies virtual switch settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a82-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9a82-105">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f9a82-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9a82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a82-107">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9a82-107">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a82-108">Eine eingebettete Instanz der [**MSVM \_ virtualethernetzwitchsettingdata**](msvm-virtualethernetswitchsettingdata.md) -Klasse, die die geänderten Aspekte des virtuellen Switches enthält.</span><span class="sxs-lookup"><span data-stu-id="f9a82-108">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that contains the modified aspects of the virtual switch.</span></span> <span data-ttu-id="f9a82-109">Die **InstanceId-** Eigenschaft identifiziert die zu ändernde Einstellung für den virtuellen Switch.</span><span class="sxs-lookup"><span data-stu-id="f9a82-109">The **InstanceID** property identifies the virtual switch setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="f9a82-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f9a82-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a82-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="f9a82-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9a82-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9a82-112">Return value</span></span>

<span data-ttu-id="f9a82-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f9a82-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f9a82-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="f9a82-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="f9a82-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="f9a82-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="f9a82-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="f9a82-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="f9a82-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-120">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="f9a82-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f9a82-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-122">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="f9a82-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-123">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="f9a82-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f9a82-124">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="f9a82-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f9a82-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9a82-125">Requirements</span></span>



| <span data-ttu-id="f9a82-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9a82-126">Requirement</span></span> | <span data-ttu-id="f9a82-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f9a82-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a82-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9a82-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f9a82-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9a82-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f9a82-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9a82-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f9a82-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9a82-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9a82-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9a82-132">Namespace</span></span><br/>                | <span data-ttu-id="f9a82-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f9a82-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f9a82-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f9a82-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9a82-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f9a82-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9a82-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f9a82-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9a82-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f9a82-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f9a82-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9a82-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a82-139">**MSVM \_ virtualethernetzwitchmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="f9a82-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

