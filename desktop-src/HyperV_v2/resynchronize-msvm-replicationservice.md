---
description: Führt einen Vorgang zur erneuten Synchronisierung auf dem angegebenen virtuellen Computer aus.
ms.assetid: a3d06780-f43b-45c4-a186-a3544f9c7963
title: Methode zum erneuten Synchronisieren der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.Resynchronize
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dcd4865d110843de27f0a242b31253310439e1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346358"
---
# <a name="resynchronize-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="478b2-103">Methode zum erneuten Synchronisieren der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="478b2-103">Resynchronize method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="478b2-104">Führt einen Vorgang zur erneuten Synchronisierung auf dem angegebenen virtuellen Computer aus.</span><span class="sxs-lookup"><span data-stu-id="478b2-104">Performs a resynchronization operation on the specified virtual machine.</span></span> <span data-ttu-id="478b2-105">Wenn ein Client diese Methode für einen virtuellen Replikat Computer aufruft, wird er mit dem erweiterten Replikat neu synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="478b2-105">When a client calls this method for a replica virtual machine, it resynchronizes with extended replica.</span></span>

<span data-ttu-id="478b2-106">Diese Methode vergleicht die Replikations fähigen Datenträger auf den primären und virtuellen Wiederherstellungs Computern und korrigiert alle Probleme bei der Replikations Datenintegrität, indem die verschiedenen Blöcke von der primären zur Wiederherstellung repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="478b2-106">This methods compares the replication enabled disks on the primary and recovery virtual machines, and fixes any replication data integrity issues by replicating the different blocks from the primary to the recovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="478b2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="478b2-107">Syntax</span></span>


```mof
uint32 Resynchronize(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="478b2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="478b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="478b2-109">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="478b2-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="478b2-110">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, der neu synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="478b2-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to be resynchronized.</span></span>

</dd> <dt>

<span data-ttu-id="478b2-111">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="478b2-111">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="478b2-112">Die geplante Startzeit für den Beginn der Neusynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="478b2-112">The scheduled start time for the resynchronization operation to begin.</span></span> <span data-ttu-id="478b2-113">Wenn dieser Parameter **null** ist, wird der Vorgang zur erneuten Synchronisierung sofort gestartet.</span><span class="sxs-lookup"><span data-stu-id="478b2-113">If this parameter is **Null**, the resynchronization operation starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="478b2-114">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="478b2-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="478b2-115">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="478b2-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="478b2-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="478b2-116">Return value</span></span>

<span data-ttu-id="478b2-117">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="478b2-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="478b2-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="478b2-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="478b2-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="478b2-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="478b2-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="478b2-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="478b2-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="478b2-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="478b2-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-126">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="478b2-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="478b2-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="478b2-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="478b2-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="478b2-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="478b2-131">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="478b2-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="478b2-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="478b2-132">Requirements</span></span>



| <span data-ttu-id="478b2-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="478b2-133">Requirement</span></span> | <span data-ttu-id="478b2-134">Wert</span><span class="sxs-lookup"><span data-stu-id="478b2-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="478b2-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="478b2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="478b2-136">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="478b2-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="478b2-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="478b2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="478b2-138">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="478b2-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="478b2-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="478b2-139">Namespace</span></span><br/>                | <span data-ttu-id="478b2-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="478b2-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="478b2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="478b2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="478b2-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="478b2-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="478b2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="478b2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="478b2-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="478b2-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="478b2-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="478b2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="478b2-146">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="478b2-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

