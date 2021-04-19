---
description: Ändert einen Autorisierungs Eintrag für einen Wiederherstellungs Server.
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Modifyauthorizationentry-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17f5ff1a0e4e1cca95dc5f7764d2f8e2bf9d2c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359416"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="8df4e-103">Modifyauthorizationentry-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="8df4e-103">ModifyAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="8df4e-104">Ändert einen Autorisierungs Eintrag für einen Wiederherstellungs Server.</span><span class="sxs-lookup"><span data-stu-id="8df4e-104">Modifies an authorization entry for a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df4e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8df4e-105">Syntax</span></span>


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8df4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8df4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df4e-107">*Authorizationentry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df4e-107">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df4e-108">Eine Zeichen folgen Darstellung einer Instanz der [**MSVM \_ replicationauthorizationsettingdata**](msvm-replicationauthorizationsettingdata.md) -Klasse, die den Autorisierungs Eintrag definiert, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8df4e-108">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="8df4e-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8df4e-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df4e-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="8df4e-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df4e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8df4e-111">Return value</span></span>

<span data-ttu-id="8df4e-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="8df4e-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8df4e-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8df4e-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="8df4e-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="8df4e-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="8df4e-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="8df4e-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="8df4e-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="8df4e-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="8df4e-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-121">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="8df4e-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="8df4e-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="8df4e-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="8df4e-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="8df4e-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="8df4e-126">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="8df4e-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8df4e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df4e-127">Requirements</span></span>



| <span data-ttu-id="8df4e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8df4e-128">Requirement</span></span> | <span data-ttu-id="8df4e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8df4e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8df4e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8df4e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8df4e-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8df4e-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8df4e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8df4e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8df4e-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8df4e-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8df4e-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="8df4e-134">Namespace</span></span><br/>                | <span data-ttu-id="8df4e-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8df4e-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8df4e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8df4e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8df4e-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8df4e-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8df4e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8df4e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8df4e-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8df4e-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8df4e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8df4e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df4e-141">**Addauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="8df4e-141">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="8df4e-142">**Removeauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="8df4e-142">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="8df4e-143">**Setauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="8df4e-143">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="8df4e-144">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="8df4e-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

