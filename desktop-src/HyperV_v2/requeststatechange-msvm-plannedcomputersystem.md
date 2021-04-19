---
description: Fordert an, dass der Status des geplanten Systems in den angegebenen Wert geändert wird.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: RequestStateChange-Methode der Msvm_PlannedComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358435"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a><span data-ttu-id="06056-103">RequestStateChange-Methode der MSVM \_ plannedcomputersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="06056-103">RequestStateChange method of the Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="06056-104">Fordert an, dass der Status des geplanten Systems in den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="06056-104">Requests that the state of the planned system be changed to the value specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="06056-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06056-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="06056-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06056-107">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06056-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06056-108">Der angeforderte Zustand für das geplante System.</span><span class="sxs-lookup"><span data-stu-id="06056-108">The requested state for the planned system.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="06056-109">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="06056-109">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="06056-110">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="06056-110">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="06056-111">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="06056-111">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="06056-112">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="06056-112">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="06056-113">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="06056-113">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="06056-114">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="06056-114">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="06056-115">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="06056-115">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="06056-116">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="06056-116">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="06056-117">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="06056-117">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="06056-118">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="06056-118">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="06056-119">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="06056-119">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="06056-120">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="06056-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06056-121">Dieser Parameter wird nicht verwendet und sollte **null** sein.</span><span class="sxs-lookup"><span data-stu-id="06056-121">This parameter is not used and should be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06056-122">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06056-122">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06056-123">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="06056-123">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06056-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06056-124">Return value</span></span>

<span data-ttu-id="06056-125">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="06056-125">This method returns one of the following values.</span></span>



| <span data-ttu-id="06056-126">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="06056-126">Return code/value</span></span>                                                                                                                      | <span data-ttu-id="06056-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06056-127">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06056-128"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="06056-128"><dt></dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="06056-129">Erfolg</span><span class="sxs-lookup"><span data-stu-id="06056-129">Success</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="06056-130"><dt></dt><dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="06056-130"><dt></dt> <dt>4096</dt></span></span> </dl>  |                                                                                    |
| <dl> <span data-ttu-id="06056-131"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="06056-131"><dt></dt> <dt>32768</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="06056-132"><dt></dt><dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="06056-132"><dt></dt> <dt>32769</dt></span></span> </dl> | <span data-ttu-id="06056-133">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="06056-133">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="06056-134"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="06056-134"><dt></dt> <dt>32770</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="06056-135"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="06056-135"><dt></dt> <dt>32771</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="06056-136"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="06056-136"><dt></dt> <dt>32772</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="06056-137"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="06056-137"><dt></dt> <dt>32773</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="06056-138"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="06056-138"><dt></dt> <dt>32774</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="06056-139"><dt></dt><dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="06056-139"><dt></dt> <dt>32775</dt></span></span> </dl> | <span data-ttu-id="06056-140">Der im *requestedstate* -Parameter angegebene Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="06056-140">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="06056-141"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="06056-141"><dt></dt> <dt>32776</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="06056-142"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="06056-142"><dt></dt> <dt>32777</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="06056-143"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="06056-143"><dt></dt> <dt>32778</dt></span></span> </dl> |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="06056-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06056-144">Requirements</span></span>



| <span data-ttu-id="06056-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06056-145">Requirement</span></span> | <span data-ttu-id="06056-146">Wert</span><span class="sxs-lookup"><span data-stu-id="06056-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06056-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06056-147">Minimum supported client</span></span><br/> | <span data-ttu-id="06056-148">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06056-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="06056-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06056-149">Minimum supported server</span></span><br/> | <span data-ttu-id="06056-150">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06056-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06056-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="06056-151">Namespace</span></span><br/>                | <span data-ttu-id="06056-152">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="06056-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="06056-153">MOF</span><span class="sxs-lookup"><span data-stu-id="06056-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06056-154"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="06056-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06056-155">DLL</span><span class="sxs-lookup"><span data-stu-id="06056-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06056-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06056-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06056-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06056-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06056-158">**MSVM \_ plannedcomputersystem**</span><span class="sxs-lookup"><span data-stu-id="06056-158">**Msvm\_PlannedComputerSystem**</span></span>](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




