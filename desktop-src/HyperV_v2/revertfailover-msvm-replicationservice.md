---
description: Stellt das aktuelle Failover für einen virtuellen Computer wieder her, indem der aktuelle failoverdatenträger verworfen wird.
ms.assetid: 99d3a3d3-49e4-4410-b979-47b62ebc6aa6
title: Revertfailover-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RevertFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: db20abf34fdad2e0eba499fd1b4cc390bf93b754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350974"
---
# <a name="revertfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="e891c-103">Revertfailover-Methode der MSVM \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="e891c-103">RevertFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="e891c-104">Stellt das aktuelle Failover für einen virtuellen Computer wieder her, indem der aktuelle failoverdatenträger verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="e891c-104">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span> <span data-ttu-id="e891c-105">Nach diesem Vorgang kann [**initiatefailover**](initiatefailover-msvm-replicationservice.md) erneut aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e891c-105">After this operation, [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) can be called again.</span></span>

## <a name="syntax"></a><span data-ttu-id="e891c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e891c-106">Syntax</span></span>


```mof
uint32 RevertFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e891c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e891c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e891c-108">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e891c-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e891c-109">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den das Failover wieder hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e891c-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to revert the failover.</span></span>

</dd> <dt>

<span data-ttu-id="e891c-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e891c-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e891c-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="e891c-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e891c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e891c-112">Return value</span></span>

<span data-ttu-id="e891c-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e891c-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e891c-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="e891c-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="e891c-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="e891c-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="e891c-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="e891c-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="e891c-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e891c-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="e891c-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-122">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="e891c-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="e891c-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="e891c-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="e891c-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="e891c-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e891c-127">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="e891c-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e891c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e891c-128">Requirements</span></span>



| <span data-ttu-id="e891c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e891c-129">Requirement</span></span> | <span data-ttu-id="e891c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e891c-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e891c-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e891c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e891c-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e891c-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e891c-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e891c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e891c-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e891c-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e891c-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="e891c-135">Namespace</span></span><br/>                | <span data-ttu-id="e891c-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e891c-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e891c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e891c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e891c-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e891c-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e891c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e891c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e891c-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e891c-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e891c-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e891c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e891c-142">**Initiatefailover**</span><span class="sxs-lookup"><span data-stu-id="e891c-142">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="e891c-143">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="e891c-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="e891c-144">**Setfailovernetworkadaptersettings**</span><span class="sxs-lookup"><span data-stu-id="e891c-144">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

