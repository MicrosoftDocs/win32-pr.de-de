---
description: Repliziert einen virtuellen Computer, für den ein Failover ausgeführt wurde, zurück auf den primären Server.
ms.assetid: 21806a66-85b4-4d9e-8a50-52d2b1933b67
title: Reversereplicationrelationship-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ReverseReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 25ab0c754c5139b0b3419db74162a8ac0495cf1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357738"
---
# <a name="reversereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="3e359-103">Reversereplicationrelationship-Methode der MSVM \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3e359-103">ReverseReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="3e359-104">Repliziert einen virtuellen Computer, für den ein Failover ausgeführt wurde, zurück auf den primären Server.</span><span class="sxs-lookup"><span data-stu-id="3e359-104">Replicates a failed-over virtual machine back to the primary server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e359-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e359-105">Syntax</span></span>


```mof
uint32 ReverseReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3e359-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e359-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e359-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e359-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e359-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikation umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e359-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be reversed.</span></span>

</dd> <dt>

<span data-ttu-id="3e359-109">*Replicationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e359-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e359-110">Eine Zeichen folgen Darstellung einer Instanz der [**MSVM \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Klasse, die die Replikationseinstellungen definiert.</span><span class="sxs-lookup"><span data-stu-id="3e359-110">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="3e359-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3e359-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e359-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3e359-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e359-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e359-113">Return value</span></span>

<span data-ttu-id="3e359-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3e359-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3e359-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3e359-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3e359-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="3e359-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3e359-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3e359-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="3e359-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3e359-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="3e359-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="3e359-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="3e359-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="3e359-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="3e359-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="3e359-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3e359-128">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="3e359-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3e359-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e359-129">Requirements</span></span>



| <span data-ttu-id="3e359-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e359-130">Requirement</span></span> | <span data-ttu-id="3e359-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3e359-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e359-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e359-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3e359-133">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e359-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3e359-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e359-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3e359-135">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e359-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e359-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e359-136">Namespace</span></span><br/>                | <span data-ttu-id="3e359-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3e359-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3e359-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3e359-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e359-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3e359-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e359-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3e359-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e359-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e359-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e359-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e359-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e359-143">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="3e359-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

