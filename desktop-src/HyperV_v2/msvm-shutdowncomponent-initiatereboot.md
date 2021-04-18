---
description: Initiiert einen Neustart Vorgang des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Initiatereboot-Methode der Msvm_ShutdownComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368138"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="f582f-103">Initiatereboot-Methode der MSVM \_ shutdowncomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="f582f-103">InitiateReboot method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="f582f-104">Initiiert einen Neustart Vorgang des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="f582f-104">Initiates an operating system reboot operation on the associated child virtual machine.</span></span>

<span data-ttu-id="f582f-105">Wenn 0 (null) zurückgegeben wird, wurde der Neustart erfolgreich initiiert.</span><span class="sxs-lookup"><span data-stu-id="f582f-105">If zero (0) is returned, then the reboot was initiated successfully.</span></span> <span data-ttu-id="f582f-106">Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.</span><span class="sxs-lookup"><span data-stu-id="f582f-106">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f582f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f582f-107">Syntax</span></span>


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="f582f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f582f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f582f-109">*Erzwingen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f582f-109">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f582f-110">Ein Flag, das beim Wert "true" erzwingt, dass Anwendungen geschlossen werden, obwohl nicht gespeicherte Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f582f-110">A flag which, if TRUE, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="f582f-111">*Grund* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f582f-111">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f582f-112">Der Grund für den Neustart Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f582f-112">The reason for the reboot operation.</span></span> <span data-ttu-id="f582f-113">Dies ist eine benutzerdefinierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f582f-113">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f582f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f582f-114">Return value</span></span>

<span data-ttu-id="f582f-115">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="f582f-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f582f-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="f582f-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="f582f-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="f582f-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="f582f-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="f582f-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="f582f-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="f582f-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="f582f-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-124">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="f582f-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="f582f-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="f582f-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="f582f-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="f582f-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="f582f-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-130">**Das System ist nicht bereit** (32780).</span><span class="sxs-lookup"><span data-stu-id="f582f-130">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-131">**Der Computer ist gesperrt und kann nicht ohne die Option "Force** " (32781) heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="f582f-131">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="f582f-132">**Ein Herunterfahren des Systems wird** ausgeführt (32782).</span><span class="sxs-lookup"><span data-stu-id="f582f-132">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f582f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f582f-133">Requirements</span></span>



| <span data-ttu-id="f582f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f582f-134">Requirement</span></span> | <span data-ttu-id="f582f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f582f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f582f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f582f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f582f-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f582f-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f582f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f582f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f582f-139">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f582f-139">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f582f-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="f582f-140">Namespace</span></span><br/>                | <span data-ttu-id="f582f-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f582f-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f582f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f582f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f582f-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f582f-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f582f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f582f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f582f-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f582f-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f582f-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f582f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f582f-147">**MSVM \_ shutdowncomponent**</span><span class="sxs-lookup"><span data-stu-id="f582f-147">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




