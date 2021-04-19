---
description: Fordert eine Statusänderung an.
ms.assetid: 9dfa96b1-19d4-42ea-b927-80b0d63a9be1
title: RequestStateChange-Methode der Msvm_DiskDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2de09b7f5ca7e212098f1299f597bf670e5a2970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362574"
---
# <a name="requeststatechange-method-of-the-msvm_diskdrive-class"></a><span data-ttu-id="3ec80-103">RequestStateChange-Methode der MSVM \_ diskdrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="3ec80-103">RequestStateChange method of the Msvm\_DiskDrive class</span></span>

<span data-ttu-id="3ec80-104">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="3ec80-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec80-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ec80-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="3ec80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ec80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ec80-107">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec80-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec80-108">Der für das Element angeforderte Zustand.</span><span class="sxs-lookup"><span data-stu-id="3ec80-108">The state requested for the element.</span></span> <span data-ttu-id="3ec80-109">Diese Informationen werden in die requestedstate-Eigenschaft der-Instanz eingefügt, wenn der Rückgabecode der requestStateChange-Methode 0 (' abgeschlossen ohne Fehler ') oder 4096 (0x1000) (' Auftrag gestartet ') ist.</span><span class="sxs-lookup"><span data-stu-id="3ec80-109">This information will be placed into the RequestedState property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="3ec80-110">Ausführliche Erläuterungen zu den requestedstate-Werten finden Sie in der Beschreibung der Eigenschaften "enabledstate" und "requestedstate".</span><span class="sxs-lookup"><span data-stu-id="3ec80-110">Refer to the description of the EnabledState and RequestedState properties for the detailed explanations of the RequestedState values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3ec80-111">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="3ec80-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3ec80-112">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="3ec80-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="3ec80-113">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="3ec80-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="3ec80-114">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="3ec80-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="3ec80-115">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="3ec80-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="3ec80-116">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="3ec80-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="3ec80-117">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="3ec80-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="3ec80-118">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="3ec80-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="3ec80-119">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="3ec80-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3ec80-120">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3ec80-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3ec80-121">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="3ec80-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="3ec80-122">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3ec80-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec80-123">Kann einen Verweis auf den erstellten konkreten TestJob enthalten, um den durch den Methodenaufruf initiierten Zustandsübergang zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="3ec80-123">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="3ec80-124">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ec80-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec80-125">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="3ec80-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="3ec80-126">Zum Angeben des timeoutperiod muss das Intervall Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ec80-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="3ec80-127">Der Wert 0 oder ein NULL-Parameter gibt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="3ec80-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="3ec80-128">Wenn diese Eigenschaft nicht 0 oder NULL enthält und die Implementierung diesen Parameter nicht unterstützt, sollte der Rückgabecode "Use of Timeout Parameter not supported" zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3ec80-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ec80-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ec80-129">Return value</span></span>

<span data-ttu-id="3ec80-130">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="3ec80-130">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3ec80-131">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3ec80-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ec80-132">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="3ec80-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3ec80-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ec80-133">Requirements</span></span>



| <span data-ttu-id="3ec80-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ec80-134">Requirement</span></span> | <span data-ttu-id="3ec80-135">Wert</span><span class="sxs-lookup"><span data-stu-id="3ec80-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec80-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ec80-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec80-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3ec80-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3ec80-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ec80-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec80-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3ec80-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3ec80-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ec80-140">Namespace</span></span><br/>                | <span data-ttu-id="3ec80-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3ec80-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3ec80-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3ec80-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ec80-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3ec80-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ec80-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3ec80-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ec80-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ec80-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ec80-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ec80-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec80-147">**MSVM \_ diskdrive**</span><span class="sxs-lookup"><span data-stu-id="3ec80-147">**Msvm\_DiskDrive**</span></span>](msvm-diskdrive.md)
</dt> </dl>

 

 




