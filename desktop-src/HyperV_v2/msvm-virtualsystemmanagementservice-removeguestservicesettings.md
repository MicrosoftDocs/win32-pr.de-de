---
description: Entfernt Gast Dienst Einstellungen aus einer Konfiguration des virtuellen Systems.
ms.assetid: 33e55d74-adfd-4174-8f05-14e797a33806
title: Removeguestservicesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0aee1f8f9d729c093bff2a580e054d93fa7fc033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340158"
---
# <a name="removeguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ce1b7-103">Removeguestservicesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="ce1b7-103">RemoveGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ce1b7-104">Entfernt Gast Dienst Einstellungen aus einer Konfiguration des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="ce1b7-104">Removes guest service settings from a virtual system configuration.</span></span>

<span data-ttu-id="ce1b7-105">Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Gast Dienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ce1b7-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce1b7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce1b7-106">Syntax</span></span>


```mof
uint32 RemoveGuestServiceSettings(
  [in]  CIM_SettingData REF GuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ce1b7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce1b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce1b7-108">*Guestservicesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce1b7-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce1b7-109">Verweis auf ein Array von [**CIM \_ SettingData**](cim-settingdata.md) , das die zu entfernende Gast Dienst Einstellung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ce1b7-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the guest service setting to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ce1b7-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce1b7-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce1b7-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ce1b7-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce1b7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce1b7-112">Return value</span></span>

<span data-ttu-id="ce1b7-113">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="ce1b7-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ce1b7-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ce1b7-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ce1b7-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="ce1b7-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ce1b7-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ce1b7-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ce1b7-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ce1b7-120">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ce1b7-121">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ce1b7-122">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ce1b7-123">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ce1b7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce1b7-124">Requirements</span></span>



| <span data-ttu-id="ce1b7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce1b7-125">Requirement</span></span> | <span data-ttu-id="ce1b7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ce1b7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce1b7-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ce1b7-128">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce1b7-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ce1b7-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce1b7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ce1b7-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ce1b7-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ce1b7-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce1b7-131">Namespace</span></span><br/>                | <span data-ttu-id="ce1b7-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ce1b7-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ce1b7-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ce1b7-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce1b7-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ce1b7-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce1b7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ce1b7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce1b7-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ce1b7-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ce1b7-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce1b7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce1b7-138">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="ce1b7-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

