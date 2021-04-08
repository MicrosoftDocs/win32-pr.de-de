---
description: Ändert die Einstellungen des Gast Diensts.
ms.assetid: a308aa59-bd43-4dd5-a690-c435102e8043
title: Modifyguestservicesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bc0af24346c445022ba3f8725ea6102c61dc9c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862063"
---
# <a name="modifyguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="8db44-103">Modifyguestservicesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="8db44-103">ModifyGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="8db44-104">Ändert die Einstellungen des Gast Diensts.</span><span class="sxs-lookup"><span data-stu-id="8db44-104">Modifies guest service settings.</span></span>

<span data-ttu-id="8db44-105">Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Gast Dienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8db44-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db44-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8db44-106">Syntax</span></span>


```mof
uint32 ModifyGuestServiceSettings(
  [in]  string              GuestServiceSettings[],
  [out] CIM_SettingData REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8db44-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db44-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db44-108">*Guestservicesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8db44-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db44-109">Ein Array, das die neuen Einstellungen des Gast Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="8db44-109">An array that contains the new guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="8db44-110">*Resultingguestservicesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8db44-110">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8db44-111">Bei Erfolg wird ein Array von [**CIM- \_ SettingData**](cim-settingdata.md) zusammenhängender, das auf die resultierenden Gast Dienst Einstellungen verweist.</span><span class="sxs-lookup"><span data-stu-id="8db44-111">On success, contiains an array of [**CIM\_SettingData**](cim-settingdata.md) that reference the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="8db44-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8db44-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8db44-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="8db44-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8db44-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8db44-114">Return value</span></span>

<span data-ttu-id="8db44-115">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="8db44-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8db44-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8db44-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="8db44-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-118">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="8db44-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="8db44-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-120">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="8db44-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-121">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="8db44-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-122">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="8db44-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="8db44-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="8db44-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="8db44-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8db44-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="8db44-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8db44-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8db44-127">Requirements</span></span>



| <span data-ttu-id="8db44-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8db44-128">Requirement</span></span> | <span data-ttu-id="8db44-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8db44-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8db44-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8db44-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8db44-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8db44-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8db44-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8db44-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8db44-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8db44-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8db44-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="8db44-134">Namespace</span></span><br/>                | <span data-ttu-id="8db44-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8db44-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8db44-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8db44-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8db44-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8db44-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8db44-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8db44-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8db44-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8db44-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8db44-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8db44-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db44-141">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="8db44-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

