---
description: Ruft die Replikations Statistiken ab, die der angegebenen Replikations Beziehung der virtuellen Maschine zugeordnet sind.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: 'Msvm_ReplicationService:: getreplicationstatisticsex-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356511"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a><span data-ttu-id="a04ec-103">MSVM \_ replicationservice:: getreplicationstatisticsex-Methode</span><span class="sxs-lookup"><span data-stu-id="a04ec-103">Msvm\_ReplicationService::GetReplicationStatisticsEx method</span></span>

<span data-ttu-id="a04ec-104">Ruft die Replikations Statistiken ab, die der angegebenen Replikations Beziehung der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a04ec-104">Retrieves the replication statistics that are associated with the specified replication relationship of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a04ec-105">Syntax</span></span>


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="a04ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a04ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04ec-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a04ec-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04ec-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikations Statistiken abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a04ec-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="a04ec-109">*Replicationrelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a04ec-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04ec-110">Eine Zeichen folgen Darstellung einer eingebetteten Instanz der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, die die Replikations Beziehung definiert, für die die Replikations Statistiken abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a04ec-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="a04ec-111">*Replicationstatistics* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a04ec-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a04ec-112">Bei erfolgreicher Ausführung empfängt eine eingebettete Instanz der [**MSVM- \_ replicationstatistics**](msvm-replicationstatistics.md) -Klasse, die die Replikations Statistiken für die angeforderte Replikations Beziehung enthält.</span><span class="sxs-lookup"><span data-stu-id="a04ec-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="a04ec-113">*Replicationhealthissues* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a04ec-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a04ec-114">Wenn erfolgreich, wird ein Array von eingebetteten Instanzen der [**MSVM- \_ Fehler**](msvm-error.md) Klasse empfangen, die auf Replikations Warnungen oder Fehler für den angeforderten virtuellen Computer hinweisen.</span><span class="sxs-lookup"><span data-stu-id="a04ec-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="a04ec-115">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a04ec-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a04ec-116">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a04ec-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="a04ec-117">Dieser Verweis kann **null** sein, wenn der Task beendet ist.</span><span class="sxs-lookup"><span data-stu-id="a04ec-117">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04ec-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a04ec-118">Return value</span></span>

<span data-ttu-id="a04ec-119">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="a04ec-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a04ec-120">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="a04ec-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-121">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="a04ec-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-122">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="a04ec-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-123">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="a04ec-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-124">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="a04ec-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-125">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="a04ec-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-126">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="a04ec-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-127">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="a04ec-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-128">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="a04ec-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-129">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="a04ec-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-130">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="a04ec-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-131">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="a04ec-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-132">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="a04ec-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a04ec-133">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="a04ec-133">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a04ec-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a04ec-134">Requirements</span></span>



| <span data-ttu-id="a04ec-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a04ec-135">Requirement</span></span> | <span data-ttu-id="a04ec-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a04ec-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a04ec-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a04ec-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a04ec-138">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="a04ec-138">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a04ec-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a04ec-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a04ec-140">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a04ec-140">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a04ec-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="a04ec-141">Namespace</span></span><br/>                | <span data-ttu-id="a04ec-142">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a04ec-142">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="a04ec-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a04ec-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a04ec-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a04ec-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a04ec-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a04ec-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a04ec-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a04ec-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a04ec-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a04ec-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04ec-148">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="a04ec-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="a04ec-149">**Reinstalltreplicationstatisticsex**</span><span class="sxs-lookup"><span data-stu-id="a04ec-149">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

