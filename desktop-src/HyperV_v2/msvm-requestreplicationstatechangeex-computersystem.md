---
description: Fordert an, dass der Replikations Status der Replikations Beziehung der virtuellen Maschine auf den angegebenen Wert geändert wird.
ms.assetid: 8EC78CCC-2997-4239-A20C-BA56F848ECB6
title: 'Msvm_ComputerSystem:: requestreplicationstatechangeex-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChangeEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d77db9dff90f985991c8e9013ea4f239cb6479f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348092"
---
# <a name="msvm_computersystemrequestreplicationstatechangeex-method"></a><span data-ttu-id="33889-103">MSVM \_ Computersystem:: requestreplicationstatechangeex-Methode</span><span class="sxs-lookup"><span data-stu-id="33889-103">Msvm\_ComputerSystem::RequestReplicationStateChangeEx method</span></span>

<span data-ttu-id="33889-104">Fordert an, dass der Replikations Status der Replikations Beziehung der virtuellen Maschine auf den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="33889-104">Requests that the replication state of the replication relationship of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="33889-105">Während die Statusänderung ausgeführt wird, wird die Eigenschaft **replicationstate** in den Wert des *requestedstate* -Parameters geändert.</span><span class="sxs-lookup"><span data-stu-id="33889-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="33889-106">Diese Methode wird nur für Instanzen der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse unterstützt, die eine virtuelle Maschine darstellen.</span><span class="sxs-lookup"><span data-stu-id="33889-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="33889-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="33889-107">Syntax</span></span>


```C++
uint32 RequestReplicationStateChangeEx(
  [in]  string              ReplicationRelationship,
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="33889-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="33889-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33889-109">*Replicationrelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33889-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33889-110">Eine Zeichen folgen Darstellung einer eingebetteten Instanz der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, die die Replikations Beziehung für den Status Change Request definiert.</span><span class="sxs-lookup"><span data-stu-id="33889-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for state change request.</span></span> <span data-ttu-id="33889-111">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="33889-111">This parameter is optional.</span></span> <span data-ttu-id="33889-112">Wenn es nicht angegeben ist, wird die Anforderung in der primären Replikations Beziehung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33889-112">When it's unspecified, the request runs on the primary replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="33889-113">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33889-113">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33889-114">Der neue Replikations Status.</span><span class="sxs-lookup"><span data-stu-id="33889-114">The new replication state.</span></span> <span data-ttu-id="33889-115">Muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="33889-115">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="33889-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Die erste Replikation kann gestartet** werden (1).</span><span class="sxs-lookup"><span data-stu-id="33889-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="33889-117">Bereit zum Starten der ersten Replikation.</span><span class="sxs-lookup"><span data-stu-id="33889-117">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="33889-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Warten auf Abschluss der ersten Replikation** (2)</span><span class="sxs-lookup"><span data-stu-id="33889-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="33889-119">Warten auf den Abschluss der ersten Replikation.</span><span class="sxs-lookup"><span data-stu-id="33889-119">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="33889-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replizieren** (3)</span><span class="sxs-lookup"><span data-stu-id="33889-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="33889-121">Replikation.</span><span class="sxs-lookup"><span data-stu-id="33889-121">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="33889-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synchronisierungs Replikation beendet** (4)</span><span class="sxs-lookup"><span data-stu-id="33889-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="33889-123">Synchronisierungs Replikation ist beendet.</span><span class="sxs-lookup"><span data-stu-id="33889-123">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="33889-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span><span class="sxs-lookup"><span data-stu-id="33889-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="33889-125">Unterbrechen der Replikation</span><span class="sxs-lookup"><span data-stu-id="33889-125">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="33889-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Neusynchronisierung Abbrechen** (9)</span><span class="sxs-lookup"><span data-stu-id="33889-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="33889-127">Abbrechen der erneuten Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="33889-127">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="33889-128">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="33889-128">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33889-129">Ein optionaler Verweis auf ein [**MSVM-" \_ concretejob**](msvm-concretejob.md) "-Objekt, das zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33889-129">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="33889-130">Falls vorhanden, kann der zurückgegebene Verweis zum Überwachen des Fortschritts und zum Abrufen des Ergebnisses der Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33889-130">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="33889-131">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33889-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33889-132">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="33889-132">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33889-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33889-133">Return value</span></span>

<span data-ttu-id="33889-134">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="33889-134">This method returns one of the following values.</span></span>



| <span data-ttu-id="33889-135">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="33889-135">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="33889-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33889-136">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="33889-137"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="33889-137"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="33889-138">Erfolg</span><span class="sxs-lookup"><span data-stu-id="33889-138">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="33889-139"><dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="33889-139"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="33889-140">Der Übergang erfolgt asynchron.</span><span class="sxs-lookup"><span data-stu-id="33889-140">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="33889-141"><dt></dt> Fehler <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="33889-141"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="33889-142"><dt>**Zugriff verweigert**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="33889-142"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="33889-143"><dt>**Nicht unterstützt**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="33889-143"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="33889-144"><dt>**Status ist unbekannt**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="33889-144"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="33889-145"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="33889-145"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="33889-146"><dt>**Ungültiger Parameter**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="33889-146"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="33889-147">Der in einem der Parameter angegebene Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33889-147">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="33889-148"><dt>**System wird verwendet**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="33889-148"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="33889-149"><dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="33889-149"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="33889-150">Der im *requestedstate* -Parameter angegebene Wert wird im aktuellen Replikations Modus oder-Status nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33889-150">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="33889-151"><dt>**Falscher Datentyp**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="33889-151"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="33889-152"><dt>**System ist nicht verfügbar**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="33889-152"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="33889-153"><dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="33889-153"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="33889-154"><dt>**Datei nicht gefunden**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="33889-154"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="33889-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33889-155">Requirements</span></span>



| <span data-ttu-id="33889-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33889-156">Requirement</span></span> | <span data-ttu-id="33889-157">Wert</span><span class="sxs-lookup"><span data-stu-id="33889-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33889-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33889-158">Minimum supported client</span></span><br/> | <span data-ttu-id="33889-159">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="33889-159">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="33889-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33889-160">Minimum supported server</span></span><br/> | <span data-ttu-id="33889-161">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33889-161">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33889-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="33889-162">Namespace</span></span><br/>                | <span data-ttu-id="33889-163">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="33889-163">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="33889-164">MOF</span><span class="sxs-lookup"><span data-stu-id="33889-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33889-165"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="33889-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33889-166">DLL</span><span class="sxs-lookup"><span data-stu-id="33889-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33889-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33889-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33889-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33889-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33889-169">**MSVM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="33889-169">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




