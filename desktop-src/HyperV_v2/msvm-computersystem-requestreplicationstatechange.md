---
description: Fordert an, dass der Replikations Status des virtuellen Computers auf den angegebenen Wert geändert wird und die primäre Replikations Beziehung der virtuellen Maschine auftritt.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Requestreplicationstatechange-Methode der Msvm_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528532"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="4cfbe-103">Requestreplicationstatechange-Methode der MSVM \_ Computersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="4cfbe-103">RequestReplicationStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="4cfbe-104">Fordert an, dass der Replikations Status des virtuellen Computers auf den angegebenen Wert geändert wird und die primäre Replikations Beziehung der virtuellen Maschine auftritt.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-104">Requests that the replication state of the virtual machine be changed to the specified value and acts on the primary replication relationship of the virtual machine.</span></span> <span data-ttu-id="4cfbe-105">Während die Statusänderung ausgeführt wird, wird die Eigenschaft **replicationstate** in den Wert des *requestedstate* -Parameters geändert.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="4cfbe-106">Diese Methode wird nur für Instanzen der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse unterstützt, die eine virtuelle Maschine darstellen.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="4cfbe-107">Ab Windows 8.1 wird empfohlen, " **requestreplicationstatechange** " nicht mehr zu verwenden, um die Änderung des Replikations Zustands anzufordern.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-107">Starting with Windows 8.1, we recommend not to use **RequestReplicationStateChange** anymore to request changing of replication state.</span></span> <span data-ttu-id="4cfbe-108">Verwenden Sie stattdessen [**requestreplicationstatechangeex**](msvm-requestreplicationstatechangeex-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4cfbe-108">Instead, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4cfbe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cfbe-109">Syntax</span></span>


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="4cfbe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cfbe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfbe-111">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cfbe-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfbe-112">Der neue Replikations Status.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-112">The new replication state.</span></span> <span data-ttu-id="4cfbe-113">Muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-113">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="4cfbe-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Die erste Replikation kann gestartet** werden (1).</span><span class="sxs-lookup"><span data-stu-id="4cfbe-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4cfbe-115">Bereit zum Starten der ersten Replikation.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-115">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="4cfbe-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Warten auf Abschluss der ersten Replikation** (2)</span><span class="sxs-lookup"><span data-stu-id="4cfbe-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4cfbe-117">Warten auf den Abschluss der ersten Replikation.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-117">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="4cfbe-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replizieren** (3)</span><span class="sxs-lookup"><span data-stu-id="4cfbe-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4cfbe-119">Replikation.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-119">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="4cfbe-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synchronisierungs Replikation beendet** (4)</span><span class="sxs-lookup"><span data-stu-id="4cfbe-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4cfbe-121">Synchronisierungs Replikation ist beendet.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-121">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="4cfbe-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span><span class="sxs-lookup"><span data-stu-id="4cfbe-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4cfbe-123">Unterbrechen der Replikation</span><span class="sxs-lookup"><span data-stu-id="4cfbe-123">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="4cfbe-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Neusynchronisierung Abbrechen** (9)</span><span class="sxs-lookup"><span data-stu-id="4cfbe-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="4cfbe-125">Abbrechen der erneuten Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-125">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4cfbe-126">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4cfbe-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfbe-127">Ein optionaler Verweis auf ein [**MSVM-" \_ concretejob**](msvm-concretejob.md) "-Objekt, das zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-127">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="4cfbe-128">Falls vorhanden, kann der zurückgegebene Verweis zum Überwachen des Fortschritts und zum Abrufen des Ergebnisses der Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-128">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="4cfbe-129">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cfbe-129">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfbe-130">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfbe-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cfbe-131">Return value</span></span>

<span data-ttu-id="4cfbe-132">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="4cfbe-133">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="4cfbe-133">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="4cfbe-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cfbe-134">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cfbe-135"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="4cfbe-136">Erfolg</span><span class="sxs-lookup"><span data-stu-id="4cfbe-136">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="4cfbe-137"><dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-137"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="4cfbe-138">Der Übergang erfolgt asynchron.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-138">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="4cfbe-139"><dt></dt> Fehler <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-139"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="4cfbe-140"><dt>**Zugriff verweigert**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-140"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="4cfbe-141"><dt>**Nicht unterstützt**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-141"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="4cfbe-142"><dt>**Status ist unbekannt**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-142"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="4cfbe-143"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-143"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="4cfbe-144"><dt>**Ungültiger Parameter**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-144"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="4cfbe-145">Der in einem der Parameter angegebene Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-145">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="4cfbe-146"><dt>**System wird verwendet**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-146"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="4cfbe-147"><dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-147"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="4cfbe-148">Der im *requestedstate* -Parameter angegebene Wert wird im aktuellen Replikations Modus oder-Status nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-148">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="4cfbe-149"><dt>**Falscher Datentyp**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-149"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="4cfbe-150"><dt>**System ist nicht verfügbar**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-150"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="4cfbe-151"><dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-151"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="4cfbe-152"><dt>**Datei nicht gefunden**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-152"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="4cfbe-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cfbe-153">Requirements</span></span>



| <span data-ttu-id="4cfbe-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cfbe-154">Requirement</span></span> | <span data-ttu-id="4cfbe-155">Wert</span><span class="sxs-lookup"><span data-stu-id="4cfbe-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfbe-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cfbe-156">Minimum supported client</span></span><br/> | <span data-ttu-id="4cfbe-157">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cfbe-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4cfbe-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cfbe-158">Minimum supported server</span></span><br/> | <span data-ttu-id="4cfbe-159">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cfbe-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4cfbe-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="4cfbe-160">Namespace</span></span><br/>                | <span data-ttu-id="4cfbe-161">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4cfbe-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4cfbe-162">MOF</span><span class="sxs-lookup"><span data-stu-id="4cfbe-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cfbe-163"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4cfbe-164">DLL</span><span class="sxs-lookup"><span data-stu-id="4cfbe-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cfbe-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4cfbe-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4cfbe-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cfbe-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfbe-167">**MSVM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="4cfbe-167">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




