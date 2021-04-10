---
description: Erstellt ein neues Replikat eines virtuellen Computers mit der angegebenen Momentaufnahme zu Testzwecken.
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: Testreplicasystem-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 029130e619aa36d0aa9b9c1c85a877fb26e1b22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867952"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="711de-103">Testreplicasystem-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="711de-103">TestReplicaSystem method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="711de-104">Erstellt ein neues Replikat eines virtuellen Computers mit der angegebenen Momentaufnahme zu Testzwecken.</span><span class="sxs-lookup"><span data-stu-id="711de-104">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span>

## <a name="syntax"></a><span data-ttu-id="711de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="711de-105">Syntax</span></span>


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="711de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="711de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711de-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="711de-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711de-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikation getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="711de-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be tested.</span></span>

</dd> <dt>

<span data-ttu-id="711de-109">*Snapshotsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="711de-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711de-110">Ein Verweis auf eine [**CIM- \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Instanz, die die Momentaufnahme darstellt, die zum Erstellen des Test Failover Systems verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="711de-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used to create the test failover system.</span></span> <span data-ttu-id="711de-111">Wenn dieser Parameter **null** ist, wird das Failover auf den letzten Zeitpunkt durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="711de-111">If this parameter is **Null**, the failover is to be performed off the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="711de-112">*Resultingsystem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="711de-112">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="711de-113">Wenn ein virtueller Computer erfolgreich definiert wurde, empfängt einen Verweis auf eine Instanz der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse, die den neu definierten virtuellen Testcomputer darstellt.</span><span class="sxs-lookup"><span data-stu-id="711de-113">If a virtual machine is successfully defined, receives a reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly defined test virtual machine.</span></span> <span data-ttu-id="711de-114">Wenn dieses System nicht mehr benötigt wird, zerstören Sie es durch Aufrufen der [**destroysystem**](destroysystem-msvm-virtualsystemmanagementservice.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="711de-114">When this system is no longer needed, destroy it by calling the [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="711de-115">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="711de-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="711de-116">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="711de-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711de-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="711de-117">Return value</span></span>

<span data-ttu-id="711de-118">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="711de-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="711de-119">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="711de-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="711de-120">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="711de-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="711de-121">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="711de-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="711de-122">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="711de-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="711de-123">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="711de-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="711de-124">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="711de-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="711de-125">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="711de-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="711de-126">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="711de-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="711de-127">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="711de-127">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="711de-128">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="711de-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="711de-129">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="711de-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="711de-130">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="711de-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="711de-131">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="711de-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="711de-132">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="711de-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="711de-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="711de-133">Requirements</span></span>



| <span data-ttu-id="711de-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="711de-134">Requirement</span></span> | <span data-ttu-id="711de-135">Wert</span><span class="sxs-lookup"><span data-stu-id="711de-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="711de-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="711de-136">Minimum supported client</span></span><br/> | <span data-ttu-id="711de-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="711de-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="711de-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="711de-138">Minimum supported server</span></span><br/> | <span data-ttu-id="711de-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="711de-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="711de-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="711de-140">Namespace</span></span><br/>                | <span data-ttu-id="711de-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="711de-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="711de-142">MOF</span><span class="sxs-lookup"><span data-stu-id="711de-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="711de-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="711de-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="711de-144">DLL</span><span class="sxs-lookup"><span data-stu-id="711de-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="711de-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="711de-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="711de-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="711de-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711de-147">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="711de-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

