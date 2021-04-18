---
description: Führt einen Commit für die Wiederherstellungs Momentaufnahme aus, die die initiatefailover-Methode für ein Failover verwendet hat
ms.assetid: 05c27211-adc7-400a-83e2-81792ae7577f
title: Commitfailover-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CommitFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 04687ea29f39645c2407de44faf6bba6ecc75832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358963"
---
# <a name="commitfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="b9a68-103">Commitfailover-Methode der MSVM \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b9a68-103">CommitFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="b9a68-104">Führt einen Commit für die Wiederherstellungs Momentaufnahme aus, die die [**initiatefailover**](initiatefailover-msvm-replicationservice.md) -Methode für ein Failover verwendet hat</span><span class="sxs-lookup"><span data-stu-id="b9a68-104">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span>

<span data-ttu-id="b9a68-105">Diese Methode vereinfacht die Wiederherstellungspunkte auf dem virtuellen Wiederherstellungs Computer durch Anwenden der Wiederherstellungs Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="b9a68-105">This method flattens the recovery points on the recovery virtual machine by applying the recovery snapshot.</span></span> <span data-ttu-id="b9a68-106">Danach kann der Failovervorgang nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="b9a68-106">After this is done, the failover operation cannot be canceled.</span></span> <span data-ttu-id="b9a68-107">Diese werden in der Regel von Benutzern ausgeführt, wenn der für das Failover verwendete Replikations Punkt zufriedenstellend ist und der virtuelle Wiederherstellungs Computer die Rolle als primär ändern kann.</span><span class="sxs-lookup"><span data-stu-id="b9a68-107">Users will typically perform this when the replication point used for failover is satisfactory and the recovery virtual machine can change role to be primary.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a68-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9a68-108">Syntax</span></span>


```mof
uint32 CommitFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b9a68-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9a68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9a68-110">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9a68-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9a68-111">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den ein Commit für das Failover ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9a68-111">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to commit the failover.</span></span>

</dd> <dt>

<span data-ttu-id="b9a68-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9a68-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9a68-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="b9a68-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9a68-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9a68-114">Return value</span></span>

<span data-ttu-id="b9a68-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b9a68-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b9a68-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a68-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="b9a68-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="b9a68-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="b9a68-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="b9a68-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="b9a68-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b9a68-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="b9a68-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="b9a68-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="b9a68-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="b9a68-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="b9a68-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="b9a68-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b9a68-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="b9a68-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b9a68-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9a68-130">Requirements</span></span>



| <span data-ttu-id="b9a68-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9a68-131">Requirement</span></span> | <span data-ttu-id="b9a68-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b9a68-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a68-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9a68-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a68-134">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9a68-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b9a68-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9a68-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a68-136">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9a68-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9a68-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9a68-137">Namespace</span></span><br/>                | <span data-ttu-id="b9a68-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b9a68-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b9a68-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b9a68-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9a68-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b9a68-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9a68-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b9a68-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9a68-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9a68-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9a68-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9a68-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9a68-144">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="b9a68-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

