---
description: Setzt die Replikations Statistiken für eine virtuelle Maschine zurück und setzt die primäre Replikations Beziehung des virtuellen Computers zusammen.
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Resegtreplicationstatistics-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8407e20cb38c9aecac26ab0bcee99ce0c8a6be2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358906"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="72dba-103">Remintreplicationstatistics-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="72dba-103">ResetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="72dba-104">Setzt die Replikations Statistiken für eine virtuelle Maschine zurück und setzt die primäre Replikations Beziehung des virtuellen Computers zusammen.</span><span class="sxs-lookup"><span data-stu-id="72dba-104">Resets the replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="72dba-105">Ab Windows 8.1 wird empfohlen, die Replikations Statistiken nicht mehr mithilfe von **recationstatistics** zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="72dba-105">Starting with Windows 8.1, we recommend not to use **ResetReplicationStatistics** anymore to reset replication statistics.</span></span> <span data-ttu-id="72dba-106">Verwenden Sie stattdessen [**rec treplicationstatisticsex**](resetreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="72dba-106">Instead, use [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="72dba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="72dba-107">Syntax</span></span>


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="72dba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="72dba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72dba-109">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72dba-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72dba-110">Ein Verweis auf eine Instanz der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse, die den virtuellen Computer darstellt, für den die Replikations Statistiken zurückgesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="72dba-110">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to reset the replication statistics for.</span></span>

</dd> <dt>

<span data-ttu-id="72dba-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72dba-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72dba-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="72dba-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72dba-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72dba-113">Return value</span></span>

<span data-ttu-id="72dba-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="72dba-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="72dba-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="72dba-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="72dba-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="72dba-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="72dba-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="72dba-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="72dba-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="72dba-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="72dba-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-123">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="72dba-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="72dba-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="72dba-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="72dba-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="72dba-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="72dba-128">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="72dba-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="72dba-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72dba-129">Requirements</span></span>



| <span data-ttu-id="72dba-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72dba-130">Requirement</span></span> | <span data-ttu-id="72dba-131">Wert</span><span class="sxs-lookup"><span data-stu-id="72dba-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72dba-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72dba-132">Minimum supported client</span></span><br/> | <span data-ttu-id="72dba-133">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72dba-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72dba-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72dba-134">Minimum supported server</span></span><br/> | <span data-ttu-id="72dba-135">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72dba-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72dba-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="72dba-136">Namespace</span></span><br/>                | <span data-ttu-id="72dba-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="72dba-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72dba-138">MOF</span><span class="sxs-lookup"><span data-stu-id="72dba-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72dba-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="72dba-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72dba-140">DLL</span><span class="sxs-lookup"><span data-stu-id="72dba-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72dba-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72dba-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72dba-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72dba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72dba-143">**Getreplicationstatistics**</span><span class="sxs-lookup"><span data-stu-id="72dba-143">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="72dba-144">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="72dba-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

