---
description: Entfernt einen Autorisierungs Eintrag von einem Wiederherstellungs Server.
ms.assetid: 1647b35d-1c2f-4fb5-84c0-10b357326abf
title: Removeauthorizationentry-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0bb0d24c9cf4936c6e0187e5091b9fac14ee28c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366187"
---
# <a name="removeauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="57585-103">Removeauthorizationentry-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="57585-103">RemoveAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="57585-104">Entfernt einen Autorisierungs Eintrag von einem Wiederherstellungs Server.</span><span class="sxs-lookup"><span data-stu-id="57585-104">Removes an authorization entry from a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="57585-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57585-105">Syntax</span></span>


```mof
uint32 RemoveAuthorizationEntry(
  [in]  string              AllowedPrimaryHostSystem,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="57585-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57585-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57585-107">"Bereitstellungs- *Hostsystem* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="57585-107">*AllowedPrimaryHostSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57585-108">Der primäre Server, für den der Autorisierungs Eintrag vom Server entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="57585-108">The primary server for which the authorization entry will be removed from the server.</span></span> <span data-ttu-id="57585-109">Dies ist identisch mit **der Eigenschaft "" der Eigenschaft** "" der Klasse " [**MSVM" \_ replicationauthorizationsettingdata**](msvm-replicationauthorizationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="57585-109">This is the same as the **AllowedPrimaryHostSystem** property of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="57585-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57585-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57585-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="57585-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57585-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57585-112">Return value</span></span>

<span data-ttu-id="57585-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="57585-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="57585-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="57585-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57585-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="57585-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="57585-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="57585-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="57585-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="57585-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="57585-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="57585-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="57585-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="57585-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="57585-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="57585-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="57585-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="57585-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="57585-122">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="57585-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="57585-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="57585-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="57585-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="57585-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="57585-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="57585-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="57585-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="57585-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="57585-127">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="57585-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="57585-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57585-128">Remarks</span></span>

<span data-ttu-id="57585-129">Wenn Sie einen Autorisierungs Eintrag entfernen, wird die Replikation für alle virtuellen Computer beendet, die mit dem Eintrag autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="57585-129">Removing an authorization entry will stop replication for any virtual machines that are authorized with the entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="57585-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57585-130">Requirements</span></span>



| <span data-ttu-id="57585-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57585-131">Requirement</span></span> | <span data-ttu-id="57585-132">Wert</span><span class="sxs-lookup"><span data-stu-id="57585-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57585-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57585-133">Minimum supported client</span></span><br/> | <span data-ttu-id="57585-134">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57585-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="57585-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57585-135">Minimum supported server</span></span><br/> | <span data-ttu-id="57585-136">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57585-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57585-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="57585-137">Namespace</span></span><br/>                | <span data-ttu-id="57585-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="57585-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="57585-139">MOF</span><span class="sxs-lookup"><span data-stu-id="57585-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57585-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="57585-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57585-141">DLL</span><span class="sxs-lookup"><span data-stu-id="57585-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57585-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57585-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="57585-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57585-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57585-144">**Addauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="57585-144">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="57585-145">**Modifyauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="57585-145">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="57585-146">**Setauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="57585-146">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="57585-147">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="57585-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

