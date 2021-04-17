---
description: Fügt einer virtuellen Systemkonfiguration Gast Dienst Einstellungen hinzu.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Addguestservicesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5bcdfd8c159e92efe633c04e22af5bceb9d003e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525208"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="2d7f6-103">Addguestservicesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="2d7f6-103">AddGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2d7f6-104">Fügt einer virtuellen Systemkonfiguration Gast Dienst Einstellungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-104">Adds guest service settings to a virtual system configuration.</span></span>

<span data-ttu-id="2d7f6-105">Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Gast Dienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d7f6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d7f6-106">Syntax</span></span>


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2d7f6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d7f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d7f6-108">*Affectedconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d7f6-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d7f6-109">Verweis auf einen [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) , der die betroffene Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-109">Reference to a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that describes the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2d7f6-110">*Guestservicesettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d7f6-110">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d7f6-111">Ein Array, das die Einstellungen des Gast Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-111">An array containing the guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="2d7f6-112">*Resultingguestservicesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2d7f6-112">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d7f6-113">Bei Erfolg enthält einen Verweis auf eine [**CIM- \_ SettingData**](cim-settingdata.md) , in der die resultierenden Gast Dienst Einstellungen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-113">On success, contains a reference to a [**CIM\_SettingData**](cim-settingdata.md) that describes the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="2d7f6-114">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2d7f6-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d7f6-115">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d7f6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d7f6-116">Return value</span></span>

<span data-ttu-id="2d7f6-117">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2d7f6-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d7f6-119">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2d7f6-120">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="2d7f6-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2d7f6-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2d7f6-122">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2d7f6-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2d7f6-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2d7f6-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2d7f6-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2d7f6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d7f6-127">Requirements</span></span>



| <span data-ttu-id="2d7f6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d7f6-128">Requirement</span></span> | <span data-ttu-id="2d7f6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2d7f6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d7f6-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2d7f6-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d7f6-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2d7f6-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d7f6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2d7f6-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2d7f6-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2d7f6-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d7f6-134">Namespace</span></span><br/>                | <span data-ttu-id="2d7f6-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d7f6-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2d7f6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2d7f6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d7f6-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2d7f6-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d7f6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2d7f6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d7f6-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d7f6-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d7f6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d7f6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d7f6-141">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="2d7f6-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

