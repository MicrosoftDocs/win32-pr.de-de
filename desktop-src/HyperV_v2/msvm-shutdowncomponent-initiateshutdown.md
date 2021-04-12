---
description: Initiiert einen Vorgang zum Herunterfahren des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine. Wenn 0 (null) zurückgegeben wird, wurde das Herunterfahren erfolgreich initiiert. Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: InitiateShutdown-Methode der Msvm_ShutdownComponent-Klasse (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216763"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="aa030-105">InitiateShutdown-Methode der MSVM \_ shutdowncomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="aa030-105">InitiateShutdown method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="aa030-106">Initiiert einen Vorgang zum Herunterfahren des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="aa030-106">Initiates an operating system shutdown operation on the associated child virtual machine.</span></span> <span data-ttu-id="aa030-107">Wenn 0 (null) zurückgegeben wird, wurde das Herunterfahren erfolgreich initiiert.</span><span class="sxs-lookup"><span data-stu-id="aa030-107">If zero (0) is returned, then the shutdown was initiated successfully.</span></span> <span data-ttu-id="aa030-108">Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.</span><span class="sxs-lookup"><span data-stu-id="aa030-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa030-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa030-109">Syntax</span></span>


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="aa030-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa030-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa030-111">*Erzwingen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa030-111">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa030-112">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="aa030-112">Type: **boolean**</span></span>

<span data-ttu-id="aa030-113">Ein Flag, das beim Wert " **true**" erzwingt, dass Anwendungen geschlossen werden, obwohl nicht gespeicherte Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="aa030-113">A flag which, if **True**, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="aa030-114">*Grund* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa030-114">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa030-115">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa030-115">Type: **string**</span></span>

<span data-ttu-id="aa030-116">Der Grund für den Vorgang zum Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="aa030-116">The reason for the shutdown operation.</span></span> <span data-ttu-id="aa030-117">Dies ist eine benutzerdefinierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="aa030-117">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa030-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa030-118">Return value</span></span>

<span data-ttu-id="aa030-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa030-119">Type: **uint32**</span></span>

<dl> <dt>

<span data-ttu-id="aa030-120">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="aa030-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-121">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="aa030-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-122">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="aa030-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-123">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="aa030-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-124">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="aa030-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-125">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="aa030-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-126">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="aa030-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-127">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="aa030-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-128">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="aa030-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-129">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="aa030-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-130">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="aa030-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-131">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="aa030-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-132">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="aa030-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-133">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="aa030-133">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-134">**Das System ist nicht bereit** (32780).</span><span class="sxs-lookup"><span data-stu-id="aa030-134">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-135">**Der Computer ist gesperrt und kann nicht ohne die Option "Force** " (32781) heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="aa030-135">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="aa030-136">**Ein Herunterfahren des Systems wird** ausgeführt (32782).</span><span class="sxs-lookup"><span data-stu-id="aa030-136">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="aa030-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa030-137">Remarks</span></span>

<span data-ttu-id="aa030-138">Der Zugriff auf die [**MSVM \_ shutdowncomponent**](msvm-shutdowncomponent.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="aa030-138">Access to the [**Msvm\_ShutdownComponent**](msvm-shutdowncomponent.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="aa030-139">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="aa030-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa030-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa030-140">Requirements</span></span>



| <span data-ttu-id="aa030-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa030-141">Requirement</span></span> | <span data-ttu-id="aa030-142">Wert</span><span class="sxs-lookup"><span data-stu-id="aa030-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa030-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa030-143">Minimum supported client</span></span><br/> | <span data-ttu-id="aa030-144">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa030-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="aa030-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa030-145">Minimum supported server</span></span><br/> | <span data-ttu-id="aa030-146">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa030-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa030-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa030-147">Namespace</span></span><br/>                | <span data-ttu-id="aa030-148">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="aa030-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="aa030-149">Header</span><span class="sxs-lookup"><span data-stu-id="aa030-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa030-150"><dt>Winreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa030-150"><dt>Winreg.h</dt></span></span> </dl>                     |
| <span data-ttu-id="aa030-151">MOF</span><span class="sxs-lookup"><span data-stu-id="aa030-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa030-152"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aa030-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa030-153">DLL</span><span class="sxs-lookup"><span data-stu-id="aa030-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa030-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa030-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa030-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa030-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa030-156">**MSVM \_ shutdowncomponent**</span><span class="sxs-lookup"><span data-stu-id="aa030-156">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

