---
description: Initiiert das Failback für einen virtuellen Wiederherstellungs Computer.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: 'Msvm_ReplicationService:: initiatefailback-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b356982296427212287ea11b528a7878dc166245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348867"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a><span data-ttu-id="c26e1-103">MSVM \_ replicationservice:: initiatefailback-Methode</span><span class="sxs-lookup"><span data-stu-id="c26e1-103">Msvm\_ReplicationService::InitiateFailback method</span></span>

<span data-ttu-id="c26e1-104">Initiiert das Failback für einen virtuellen Wiederherstellungs Computer.</span><span class="sxs-lookup"><span data-stu-id="c26e1-104">Initiates the failback for a recovery virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c26e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c26e1-105">Syntax</span></span>


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="c26e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c26e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c26e1-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c26e1-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c26e1-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den ein Failback initiiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c26e1-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failback.</span></span>

</dd> <dt>

<span data-ttu-id="c26e1-109">*Replicationsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c26e1-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c26e1-110">Eine Zeichen folgen Darstellung einer eingebetteten Instanz der [**MSVM \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Klasse, die die Replikationseinstellungen für das Failback definiert.</span><span class="sxs-lookup"><span data-stu-id="c26e1-110">A string representation of an embedded instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the failback.</span></span>

</dd> <dt>

<span data-ttu-id="c26e1-111">*Wiederherstellungspointidentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c26e1-111">*RecoveryPointIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c26e1-112">Optionale Eingabe, die den Wiederherstellungspunkt identifiziert, an den das Failback angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="c26e1-112">Optional input that identifies the recovery point to which failback is requested.</span></span>

</dd> <dt>

<span data-ttu-id="c26e1-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c26e1-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c26e1-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="c26e1-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="c26e1-115">Dieser Verweis kann verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c26e1-115">This reference can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c26e1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c26e1-116">Return value</span></span>

<span data-ttu-id="c26e1-117">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c26e1-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c26e1-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="c26e1-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="c26e1-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="c26e1-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="c26e1-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="c26e1-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="c26e1-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c26e1-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="c26e1-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="c26e1-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="c26e1-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="c26e1-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="c26e1-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="c26e1-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c26e1-131">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="c26e1-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c26e1-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c26e1-132">Remarks</span></span>

<span data-ttu-id="c26e1-133">**Initiatefailback** funktioniert auf einem virtuellen Wiederherstellungs Computer und übernimmt die virtuelle Maschine in den Status " *waitingforfailback* ".</span><span class="sxs-lookup"><span data-stu-id="c26e1-133">**InitiateFailback** works on a recovery virtual machine and takes the virtual machine to *WaitingForFailback* state.</span></span> <span data-ttu-id="c26e1-134">**Initiatefailback** leitet die failbackanforderung an den entsprechenden Anbieter weiter, der den Wiederherstellungspunkt von der neuen primären Seite umkehren.</span><span class="sxs-lookup"><span data-stu-id="c26e1-134">**InitiateFailback** forwards the failback request to the corresponding provider, which reverse-resyncs the recovery point from new-primary side.</span></span> <span data-ttu-id="c26e1-135">Nachdem das Failback des angeforderten Wiederherstellungs Punkts abgeschlossen ist, wechselt der Replikations Status in den Zustand " *failbackabgeschlossene* ".</span><span class="sxs-lookup"><span data-stu-id="c26e1-135">After failback of the requested recovery point completes, the replication state moves to *FailbackCompleted* state.</span></span>

## <a name="requirements"></a><span data-ttu-id="c26e1-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c26e1-136">Requirements</span></span>



| <span data-ttu-id="c26e1-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c26e1-137">Requirement</span></span> | <span data-ttu-id="c26e1-138">Wert</span><span class="sxs-lookup"><span data-stu-id="c26e1-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c26e1-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c26e1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c26e1-140">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="c26e1-140">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c26e1-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c26e1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c26e1-142">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c26e1-142">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c26e1-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="c26e1-143">Namespace</span></span><br/>                | <span data-ttu-id="c26e1-144">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c26e1-144">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="c26e1-145">MOF</span><span class="sxs-lookup"><span data-stu-id="c26e1-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c26e1-146"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c26e1-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c26e1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c26e1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c26e1-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c26e1-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c26e1-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c26e1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c26e1-150">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="c26e1-150">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

