---
description: Fügt einem Wiederherstellungs Server einen Autorisierungs Eintrag hinzu.
ms.assetid: edc11c5b-b1a1-45e0-a920-2f1f1b0b8779
title: Addauthorizationentry-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.AddAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fd4c47bd4468d5804ec7e096d35db271726c92b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348024"
---
# <a name="addauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="72803-103">Addauthorizationentry-Methode der MSVM \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="72803-103">AddAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="72803-104">Fügt einem Wiederherstellungs Server einen Autorisierungs Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="72803-104">Adds an authorization entry to a recovery server.</span></span> <span data-ttu-id="72803-105">Diese Einträge werden zum autorialisieren von Verbindungen mit dem Wiederherstellungs Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="72803-105">These entries are used for authorizing connections to the recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="72803-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="72803-106">Syntax</span></span>


```mof
uint32 AddAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="72803-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="72803-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72803-108">*Authorizationentry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72803-108">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72803-109">Eine Zeichen folgen Darstellung einer Instanz der [**MSVM \_ replicationauthorizationsettingdata**](msvm-replicationauthorizationsettingdata.md) -Klasse, die den hinzu zufügenden Autorisierungs Eintrag definiert.</span><span class="sxs-lookup"><span data-stu-id="72803-109">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be added.</span></span>

</dd> <dt>

<span data-ttu-id="72803-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72803-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72803-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="72803-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72803-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72803-112">Return value</span></span>

<span data-ttu-id="72803-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="72803-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="72803-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="72803-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72803-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="72803-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="72803-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="72803-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="72803-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="72803-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="72803-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="72803-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="72803-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="72803-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="72803-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="72803-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="72803-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="72803-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="72803-122">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="72803-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="72803-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="72803-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="72803-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="72803-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="72803-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="72803-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="72803-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="72803-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="72803-127">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="72803-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="72803-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72803-128">Requirements</span></span>



| <span data-ttu-id="72803-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72803-129">Requirement</span></span> | <span data-ttu-id="72803-130">Wert</span><span class="sxs-lookup"><span data-stu-id="72803-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72803-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72803-131">Minimum supported client</span></span><br/> | <span data-ttu-id="72803-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72803-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72803-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72803-133">Minimum supported server</span></span><br/> | <span data-ttu-id="72803-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72803-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72803-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="72803-135">Namespace</span></span><br/>                | <span data-ttu-id="72803-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="72803-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72803-137">MOF</span><span class="sxs-lookup"><span data-stu-id="72803-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72803-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="72803-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72803-139">DLL</span><span class="sxs-lookup"><span data-stu-id="72803-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72803-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72803-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72803-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72803-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72803-142">**Modifyauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="72803-142">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="72803-143">**Removeauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="72803-143">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="72803-144">**Setauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="72803-144">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="72803-145">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="72803-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

