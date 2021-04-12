---
description: Initiiert ein Failover für einen virtuellen Computer zu einem Anwendungs-oder Standard Replikations Punkt Image.
ms.assetid: cd7e9398-c234-4637-906d-69b46ebf3f51
title: Initiatefailover-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f05a9b126028b741782d253ac12b79f9f88e1e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344539"
---
# <a name="initiatefailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="0387f-103">Initiatefailover-Methode der MSVM \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0387f-103">InitiateFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="0387f-104">Initiiert ein Failover für einen virtuellen Computer zu einem Anwendungs-oder Standard Replikations Punkt Image.</span><span class="sxs-lookup"><span data-stu-id="0387f-104">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span>

## <a name="syntax"></a><span data-ttu-id="0387f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0387f-105">Syntax</span></span>


```mof
uint32 InitiateFailover(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0387f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0387f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0387f-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0387f-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0387f-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den ein Failover initiiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0387f-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failover.</span></span>

</dd> <dt>

<span data-ttu-id="0387f-109">*Snapshotsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0387f-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0387f-110">Ein Verweis auf eine [**CIM- \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Instanz, die die für das Failover verwendete Momentaufnahme darstellt.</span><span class="sxs-lookup"><span data-stu-id="0387f-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used for the failover.</span></span> <span data-ttu-id="0387f-111">Wenn dieser Parameter **null** ist, wird das Failover auf den letzten Zeitpunkt durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0387f-111">If this parameter is **Null**, the failover is to be performed to the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="0387f-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0387f-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0387f-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0387f-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0387f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0387f-114">Return value</span></span>

<span data-ttu-id="0387f-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0387f-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0387f-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="0387f-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="0387f-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="0387f-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="0387f-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="0387f-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="0387f-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="0387f-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="0387f-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="0387f-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="0387f-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="0387f-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="0387f-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="0387f-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0387f-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="0387f-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0387f-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0387f-130">Requirements</span></span>



| <span data-ttu-id="0387f-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0387f-131">Requirement</span></span> | <span data-ttu-id="0387f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="0387f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0387f-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0387f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0387f-134">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0387f-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0387f-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0387f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0387f-136">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0387f-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0387f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="0387f-137">Namespace</span></span><br/>                | <span data-ttu-id="0387f-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0387f-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0387f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0387f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0387f-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0387f-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0387f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0387f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0387f-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0387f-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0387f-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0387f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0387f-144">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="0387f-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="0387f-145">**Revertfailover**</span><span class="sxs-lookup"><span data-stu-id="0387f-145">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="0387f-146">**Setfailovernetworkadaptersettings**</span><span class="sxs-lookup"><span data-stu-id="0387f-146">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

