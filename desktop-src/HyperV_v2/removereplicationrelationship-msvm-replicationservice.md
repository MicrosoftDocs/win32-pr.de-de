---
description: Entfernt die Replikations Beziehung eines virtuellen Computers und verhält sich mit der primären Replikations Beziehung der virtuellen Maschine.
ms.assetid: a9a20aa1-378d-4a2a-9ebc-9786ab2dfda7
title: Removereplicationrelationship-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb897ff72cd927390362f076114fc8757baa6c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862931"
---
# <a name="removereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="d245f-103">Removereplicationrelationship-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="d245f-103">RemoveReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="d245f-104">Entfernt die Replikations Beziehung eines virtuellen Computers und verhält sich mit der primären Replikations Beziehung der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="d245f-104">Removes a virtual machine replication relationship and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="d245f-105">Ab Windows 8.1 wird empfohlen, **removereplicationrelationship** nicht mehr zu verwenden, um die Replikations Beziehung eines virtuellen Computers zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d245f-105">Starting with Windows 8.1, we recommend not to use **RemoveReplicationRelationship** anymore to remove a virtual machine replication relationship.</span></span> <span data-ttu-id="d245f-106">Verwenden Sie stattdessen [**removereplicationrelationshipex**](removereplicationrelationshipex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="d245f-106">Instead, use [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d245f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d245f-107">Syntax</span></span>


```mof
uint32 RemoveReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d245f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d245f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d245f-109">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d245f-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d245f-110">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikations Beziehung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d245f-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication relationship should be removed.</span></span>

</dd> <dt>

<span data-ttu-id="d245f-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d245f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d245f-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="d245f-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d245f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d245f-113">Return value</span></span>

<span data-ttu-id="d245f-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="d245f-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d245f-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="d245f-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="d245f-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="d245f-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="d245f-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="d245f-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="d245f-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="d245f-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="d245f-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="d245f-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="d245f-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="d245f-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="d245f-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="d245f-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d245f-128">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="d245f-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d245f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d245f-129">Requirements</span></span>



| <span data-ttu-id="d245f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d245f-130">Requirement</span></span> | <span data-ttu-id="d245f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d245f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d245f-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d245f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d245f-133">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d245f-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d245f-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d245f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d245f-135">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d245f-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d245f-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d245f-136">Namespace</span></span><br/>                | <span data-ttu-id="d245f-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d245f-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d245f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d245f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d245f-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d245f-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d245f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d245f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d245f-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d245f-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d245f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d245f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d245f-143">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="d245f-143">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d245f-144">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="d245f-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

