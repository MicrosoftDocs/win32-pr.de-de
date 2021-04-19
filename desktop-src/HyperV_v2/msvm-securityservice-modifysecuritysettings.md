---
description: Ändert die aktuellen Sicherheitseinstellungen einer virtuellen Maschine.
ms.assetid: b3eedab6-fd69-4c54-a8bf-4e3b77207687
title: Modifysecuritysettings-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.ModifySecuritySettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4422f04be1833d66280392704630fcb670eba810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363820"
---
# <a name="modifysecuritysettings-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="bb7ba-103">Modifysecuritysettings-Methode der MSVM \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="bb7ba-103">ModifySecuritySettings method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="bb7ba-104">Ändert die aktuellen Sicherheitseinstellungen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-104">Modifies the current security settings of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb7ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb7ba-105">Syntax</span></span>


```mof
uint32 ModifySecuritySettings(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bb7ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb7ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb7ba-107">*Securitysettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb7ba-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb7ba-108">Die neuen Sicherheits Einstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-108">The new security setting data.</span></span>

</dd> <dt>

<span data-ttu-id="bb7ba-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bb7ba-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb7ba-110">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="bb7ba-111">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb7ba-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb7ba-112">Return value</span></span>

<span data-ttu-id="bb7ba-113">Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="bb7ba-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="bb7ba-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-120">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-122">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-123">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="bb7ba-124">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bb7ba-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb7ba-125">Requirements</span></span>



| <span data-ttu-id="bb7ba-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb7ba-126">Requirement</span></span> | <span data-ttu-id="bb7ba-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bb7ba-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7ba-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bb7ba-129">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb7ba-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bb7ba-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bb7ba-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bb7ba-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bb7ba-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb7ba-132">Namespace</span></span><br/>                | <span data-ttu-id="bb7ba-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bb7ba-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bb7ba-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bb7ba-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb7ba-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bb7ba-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb7ba-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bb7ba-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb7ba-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb7ba-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb7ba-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb7ba-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb7ba-139">**MSVM- \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="bb7ba-139">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




