---
description: Ruft Replikations Statistiken für eine virtuelle Maschine ab und fungiert für die primäre Replikations Beziehung des virtuellen Computers.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Getreplicationstatistics-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9dff711830ccdb805c362961671dff28f5bf0b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353111"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="85633-103">Getreplicationstatistics-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="85633-103">GetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="85633-104">Ruft Replikations Statistiken für eine virtuelle Maschine ab und fungiert für die primäre Replikations Beziehung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="85633-104">Retrieves replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="85633-105">Ab Windows 8.1 wird die Verwendung von **getreplicationstatistics** zum Abrufen von Replikations Statistiken nicht mehr empfohlen.</span><span class="sxs-lookup"><span data-stu-id="85633-105">Starting with Windows 8.1, we recommend not to use **GetReplicationStatistics** anymore to retrieve replication statistics.</span></span> <span data-ttu-id="85633-106">Verwenden Sie stattdessen [**getreplicationstatisticsex**](getreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="85633-106">Instead, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85633-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="85633-107">Syntax</span></span>


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="85633-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="85633-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85633-109">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85633-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85633-110">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikations Statistiken abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85633-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="85633-111">*Replicationstatistics* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85633-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85633-112">Bei erfolgreicher Ausführung empfängt eine eingebettete Instanz der [**MSVM- \_ replicationstatistics**](msvm-replicationstatistics.md) -Klasse, die die Replikations Statistiken für den angeforderten virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="85633-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="85633-113">*Replicationhealthissues* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85633-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85633-114">Wenn erfolgreich, wird ein Array von eingebetteten Instanzen der [**MSVM- \_ Fehler**](msvm-error.md) Klasse empfangen, die auf Replikations Warnungen oder Fehler für den angeforderten virtuellen Computer hinweisen.</span><span class="sxs-lookup"><span data-stu-id="85633-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="85633-115">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85633-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85633-116">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="85633-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85633-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85633-117">Return value</span></span>

<span data-ttu-id="85633-118">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="85633-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="85633-119">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="85633-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85633-120">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="85633-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="85633-121">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="85633-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="85633-122">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="85633-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="85633-123">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="85633-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="85633-124">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="85633-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="85633-125">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="85633-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="85633-126">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="85633-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="85633-127">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="85633-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="85633-128">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="85633-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="85633-129">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="85633-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="85633-130">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="85633-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="85633-131">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="85633-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="85633-132">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="85633-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="85633-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85633-133">Requirements</span></span>



| <span data-ttu-id="85633-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85633-134">Requirement</span></span> | <span data-ttu-id="85633-135">Wert</span><span class="sxs-lookup"><span data-stu-id="85633-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85633-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85633-136">Minimum supported client</span></span><br/> | <span data-ttu-id="85633-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85633-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="85633-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85633-138">Minimum supported server</span></span><br/> | <span data-ttu-id="85633-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85633-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85633-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="85633-140">Namespace</span></span><br/>                | <span data-ttu-id="85633-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="85633-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="85633-142">MOF</span><span class="sxs-lookup"><span data-stu-id="85633-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85633-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="85633-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85633-144">DLL</span><span class="sxs-lookup"><span data-stu-id="85633-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85633-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85633-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85633-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85633-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85633-147">**Reabtreplicationstatistics**</span><span class="sxs-lookup"><span data-stu-id="85633-147">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="85633-148">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="85633-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

