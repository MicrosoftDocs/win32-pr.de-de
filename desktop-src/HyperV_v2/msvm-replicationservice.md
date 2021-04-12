---
description: Verwaltet die Replikation für einen virtuellen Computer.
ms.assetid: 0335fb94-5f2b-43be-bfb4-bc6811c5b507
title: Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService
- Msvm_ReplicationService.InstanceID
- Msvm_ReplicationService.Caption
- Msvm_ReplicationService.Description
- Msvm_ReplicationService.ElementName
- Msvm_ReplicationService.InstallDate
- Msvm_ReplicationService.Name
- Msvm_ReplicationService.OperationalStatus
- Msvm_ReplicationService.StatusDescriptions
- Msvm_ReplicationService.Status
- Msvm_ReplicationService.HealthState
- Msvm_ReplicationService.CommunicationStatus
- Msvm_ReplicationService.DetailedStatus
- Msvm_ReplicationService.OperatingStatus
- Msvm_ReplicationService.PrimaryStatus
- Msvm_ReplicationService.EnabledState
- Msvm_ReplicationService.OtherEnabledState
- Msvm_ReplicationService.RequestedState
- Msvm_ReplicationService.EnabledDefault
- Msvm_ReplicationService.TimeOfLastStateChange
- Msvm_ReplicationService.AvailableRequestedStates
- Msvm_ReplicationService.TransitioningToState
- Msvm_ReplicationService.SystemCreationClassName
- Msvm_ReplicationService.SystemName
- Msvm_ReplicationService.CreationClassName
- Msvm_ReplicationService.PrimaryOwnerName
- Msvm_ReplicationService.PrimaryOwnerContact
- Msvm_ReplicationService.StartMode
- Msvm_ReplicationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86e9140e2fe9b047c57c762be2e0fba048511993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216577"
---
# <a name="msvm_replicationservice-class"></a><span data-ttu-id="0f60f-103">MSVM \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0f60f-103">Msvm\_ReplicationService class</span></span>

<span data-ttu-id="0f60f-104">Verwaltet die Replikation für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0f60f-104">Manages the replication for a virtual machine.</span></span>

<span data-ttu-id="0f60f-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0f60f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f60f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f60f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Replica Service";
  string   Description = "Replication Service";
  string   ElementName;
  datetime InstallDate;
  string   Name = "replicasvc";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ReplicationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="0f60f-107">Member</span><span class="sxs-lookup"><span data-stu-id="0f60f-107">Members</span></span>

<span data-ttu-id="0f60f-108">Die **MSVM- \_ replicationservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0f60f-108">The **Msvm\_ReplicationService** class has these types of members:</span></span>

-   [<span data-ttu-id="0f60f-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="0f60f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0f60f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f60f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0f60f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="0f60f-111">Methods</span></span>

<span data-ttu-id="0f60f-112">Die **MSVM- \_ replicationservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0f60f-112">The **Msvm\_ReplicationService** class has these methods.</span></span>



| <span data-ttu-id="0f60f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="0f60f-113">Method</span></span>                                                                                                 | <span data-ttu-id="0f60f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f60f-114">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f60f-115">**Addauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="0f60f-115">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="0f60f-116">Fügt einem Server einen Autorisierungs Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="0f60f-116">Adds an authorization entry to a server.</span></span><br/>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0f60f-117">**Changereplicationmodetoprimary**</span><span class="sxs-lookup"><span data-stu-id="0f60f-117">**ChangeReplicationModeToPrimary**</span></span>](changereplicationmodetoprimary-msvm-replicationservice.md)       | <span data-ttu-id="0f60f-118">Ändert die erweiterte Replikations Beziehung zur primären Beziehung für einen virtuellen Replikat Computer.</span><span class="sxs-lookup"><span data-stu-id="0f60f-118">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="0f60f-119">Der virtuelle Replikat Computer muss den Status "Failover committet" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0f60f-119">The replica virtual machine must be in a failover committed state.</span></span><br/> <span data-ttu-id="0f60f-120">**Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-120">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="0f60f-121">**Commitfailover**</span><span class="sxs-lookup"><span data-stu-id="0f60f-121">**CommitFailover**</span></span>](commitfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="0f60f-122">Führt einen Commit für die Wiederherstellungs Momentaufnahme aus, die die [**initiatefailover**](initiatefailover-msvm-replicationservice.md) -Methode für ein Failover verwendet hat</span><span class="sxs-lookup"><span data-stu-id="0f60f-122">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="0f60f-123">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="0f60f-123">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="0f60f-124">Erstellt eine neue Replikations Beziehung für eine virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="0f60f-124">Creates a new replication relationship for a virtual machine.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="0f60f-125">**Getreplicationstatistics**</span><span class="sxs-lookup"><span data-stu-id="0f60f-125">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)                   | <span data-ttu-id="0f60f-126">Ruft Replikations Statistiken für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="0f60f-126">Retrieves replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="0f60f-127">**Getreplicationstatisticsex**</span><span class="sxs-lookup"><span data-stu-id="0f60f-127">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)               | <span data-ttu-id="0f60f-128">Ruft die Replikations Statistiken ab, die der angegebenen Replikations Beziehung der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0f60f-128">Retrieves the replication statistics that are associated with specified replication relationship of the virtual machine.</span></span><br/> <span data-ttu-id="0f60f-129">**Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-129">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                    |
| [<span data-ttu-id="0f60f-130">**Getsystemzertifikate**</span><span class="sxs-lookup"><span data-stu-id="0f60f-130">**GetSystemCertificates**</span></span>](getsystemcertificates-msvm-replicationservice.md)                         | <span data-ttu-id="0f60f-131">Ruft die System Zertifikate auf einem Host System ab.</span><span class="sxs-lookup"><span data-stu-id="0f60f-131">Retrieves the system certificates on a host system.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="0f60f-132">**Importinitialreplica**</span><span class="sxs-lookup"><span data-stu-id="0f60f-132">**ImportInitialReplica**</span></span>](importinitialreplica-msvm-replicationservice.md)                           | <span data-ttu-id="0f60f-133">Importiert die anfängliche Replikation für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0f60f-133">Imports the initial replication for a virtual machine.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="0f60f-134">**Initiatefailback**</span><span class="sxs-lookup"><span data-stu-id="0f60f-134">**InitiateFailback**</span></span>](initiatefailback-msvm-replicationservice.md)                                   | <span data-ttu-id="0f60f-135">Initiiert das Failback für einen virtuellen Wiederherstellungs Computer.</span><span class="sxs-lookup"><span data-stu-id="0f60f-135">Initiates the failback for a recovery virtual machine.</span></span> <span data-ttu-id="0f60f-136">Das heißt, das Failover für den virtuellen Computer wird auf eine APP oder ein Absturz konsistentes Image festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-136">That is, sets the failover for the virtual machine to an app or crash consistent image.</span></span><br/> <span data-ttu-id="0f60f-137">**Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-137">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                              |
| [<span data-ttu-id="0f60f-138">**Initiatefailover**</span><span class="sxs-lookup"><span data-stu-id="0f60f-138">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)                                   | <span data-ttu-id="0f60f-139">Initiiert ein Failover für einen virtuellen Computer zu einem Anwendungs-oder Standard Replikations Punkt Image.</span><span class="sxs-lookup"><span data-stu-id="0f60f-139">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="0f60f-140">**Modifyauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="0f60f-140">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="0f60f-141">Ändert einen Autorisierungs Eintrag auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="0f60f-141">Modifies an authorization entry on a server.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="0f60f-142">**Modifyreplicationsettings**</span><span class="sxs-lookup"><span data-stu-id="0f60f-142">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)                 | <span data-ttu-id="0f60f-143">Ändert die Replikationseinstellungen für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0f60f-143">Modifies the replication settings for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="0f60f-144">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="0f60f-144">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)                         | <span data-ttu-id="0f60f-145">Ändert die Einstellungen für den Hyper-V-Replikat Dienst.</span><span class="sxs-lookup"><span data-stu-id="0f60f-145">Modifies the settings for the Hyper-V Replica service.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="0f60f-146">**Removeauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="0f60f-146">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="0f60f-147">Entfernt den Autorisierungs Eintrag von einem Server.</span><span class="sxs-lookup"><span data-stu-id="0f60f-147">Removes the authorization entry from a server.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="0f60f-148">**RemoveReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="0f60f-148">**RemoveReplicationRelationship**</span></span>](removereplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="0f60f-149">Entfernt die Replikations Beziehung eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="0f60f-149">Removes a virtual machine replication relationship.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="0f60f-150">**Removereplicationrelationshipex**</span><span class="sxs-lookup"><span data-stu-id="0f60f-150">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)     | <span data-ttu-id="0f60f-151">Entfernt die angegebene Replikations Beziehung der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="0f60f-151">Removes the specified virtual machine replication relationship.</span></span> <span data-ttu-id="0f60f-152">Bei einem virtuellen Replikat Computer kann die primäre Replikation nicht entfernt werden, wenn die erweiterte Replikation aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0f60f-152">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span><br/> <span data-ttu-id="0f60f-153">**Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-153">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>     |
| [<span data-ttu-id="0f60f-154">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0f60f-154">**RequestStateChange**</span></span>](msvm-replicationservice-requeststatechange.md)                               | <span data-ttu-id="0f60f-155">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="0f60f-155">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0f60f-156">**Reabtreplicationstatistics**</span><span class="sxs-lookup"><span data-stu-id="0f60f-156">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)               | <span data-ttu-id="0f60f-157">Setzt die Replikations Statistiken für einen virtuellen Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="0f60f-157">Resets the replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="0f60f-158">**Reinstalltreplicationstatisticsex**</span><span class="sxs-lookup"><span data-stu-id="0f60f-158">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)           | <span data-ttu-id="0f60f-159">Setzt Replikations Statistiken zurück, die der angegebenen Replikations Beziehung einer virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0f60f-159">Resets replication statistics that are associated with the specified replication relationship of a virtual machine.</span></span><br/> <span data-ttu-id="0f60f-160">**Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-160">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                         |
| [<span data-ttu-id="0f60f-161">**Erneutes Synchronisieren.**</span><span class="sxs-lookup"><span data-stu-id="0f60f-161">**Resynchronize**</span></span>](resynchronize-msvm-replicationservice.md)                                         | <span data-ttu-id="0f60f-162">Führt einen Vorgang zur erneuten Synchronisierung auf dem angegebenen virtuellen Computer aus.</span><span class="sxs-lookup"><span data-stu-id="0f60f-162">Performs a resynchronization operation on the specified virtual machine.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="0f60f-163">**Reversereplicationrelationship**</span><span class="sxs-lookup"><span data-stu-id="0f60f-163">**ReverseReplicationRelationship**</span></span>](reversereplicationrelationship-msvm-replicationservice.md)       | <span data-ttu-id="0f60f-164">Repliziert einen virtuellen Computer, für den ein Failover ausgeführt wurde, zurück auf den primären Server.</span><span class="sxs-lookup"><span data-stu-id="0f60f-164">Replicates a failed-over virtual machine back to the primary server.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="0f60f-165">**Revertfailover**</span><span class="sxs-lookup"><span data-stu-id="0f60f-165">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="0f60f-166">Stellt das aktuelle Failover für einen virtuellen Computer wieder her, indem der aktuelle failoverdatenträger verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="0f60f-166">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="0f60f-167">**Setauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="0f60f-167">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="0f60f-168">Legt den Replikations Autorisierungs Eintrag für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="0f60f-168">Sets the replication authorization entry for a virtual machine.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="0f60f-169">**Setfailovernetworkadaptersettings**</span><span class="sxs-lookup"><span data-stu-id="0f60f-169">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md) | <span data-ttu-id="0f60f-170">Konfiguriert die IP-Einstellungen des Netzwerkadapters, die nach einem Failover auf einen virtuellen Computer angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0f60f-170">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="0f60f-171">**StartReplication**</span><span class="sxs-lookup"><span data-stu-id="0f60f-171">**StartReplication**</span></span>](startreplication-msvm-replicationservice.md)                                   | <span data-ttu-id="0f60f-172">Startet die Replikation eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="0f60f-172">Starts the replication of a virtual machine.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="0f60f-173">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="0f60f-173">**StartService**</span></span>](msvm-replicationservice-startservice.md)                                           | <span data-ttu-id="0f60f-174">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0f60f-174">Starts the service.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="0f60f-175">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="0f60f-175">**StopService**</span></span>](msvm-replicationservice-stopservice.md)                                             | <span data-ttu-id="0f60f-176">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0f60f-176">Stops the service.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="0f60f-177">**Testreplicasystem**</span><span class="sxs-lookup"><span data-stu-id="0f60f-177">**TestReplicaSystem**</span></span>](testreplicasystem-msvm-replicationservice.md)                                 | <span data-ttu-id="0f60f-178">Erstellt ein neues Replikat eines virtuellen Computers mit der angegebenen Momentaufnahme zu Testzwecken.</span><span class="sxs-lookup"><span data-stu-id="0f60f-178">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="0f60f-179">**Testreplicationconnection**</span><span class="sxs-lookup"><span data-stu-id="0f60f-179">**TestReplicationConnection**</span></span>](testreplicationconnection-msvm-replicationservice.md)                 | <span data-ttu-id="0f60f-180">Überprüft, ob die Replikation vom aktuellen Host System für das angegebene Wiederherstellungs System aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f60f-180">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span><br/>                                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="0f60f-181">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f60f-181">Properties</span></span>

<span data-ttu-id="0f60f-182">Die **MSVM- \_ replicationservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0f60f-182">The **Msvm\_ReplicationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f60f-183">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="0f60f-183">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-184">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0f60f-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-186">Gibt die möglichen Werte für den *requestedstate* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="0f60f-186">Indicates the possible values for the *RequestedState* parameter.</span></span> <span data-ttu-id="0f60f-187">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-188">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0f60f-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-191">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0f60f-191">A short description of the object.</span></span> <span data-ttu-id="0f60f-192">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V-Replikat Dienst" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Replica Service".</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-193">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="0f60f-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-194">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f60f-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-196">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="0f60f-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0f60f-197">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f60f-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0f60f-198">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0f60f-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0f60f-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="0f60f-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="0f60f-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="0f60f-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="0f60f-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0f60f-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0f60f-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0f60f-206">)</span><span class="sxs-lookup"><span data-stu-id="0f60f-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0f60f-207">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="0f60f-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-210">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0f60f-210">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-211">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0f60f-211">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0f60f-212">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ replicationservice" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-212">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ReplicationService".</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-213">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f60f-213">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-216">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0f60f-216">A description of the object.</span></span> <span data-ttu-id="0f60f-217">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Replication Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-217">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service".</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-218">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0f60f-218">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-219">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f60f-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-221">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="0f60f-221">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0f60f-222">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f60f-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0f60f-223">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0f60f-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="0f60f-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="0f60f-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="0f60f-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="0f60f-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="0f60f-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="0f60f-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0f60f-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0f60f-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0f60f-232">)</span><span class="sxs-lookup"><span data-stu-id="0f60f-232">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0f60f-233">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0f60f-233">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-236">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-236">A display name for the object.</span></span> <span data-ttu-id="0f60f-237">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-238">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="0f60f-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-239">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f60f-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-241">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0f60f-241">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0f60f-242">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="0f60f-243">Wert</span><span class="sxs-lookup"><span data-stu-id="0f60f-243">Value</span></span>                                                                        | <span data-ttu-id="0f60f-244">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0f60f-244">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="0f60f-245"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0f60f-245"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0f60f-246">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="0f60f-246">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0f60f-247">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0f60f-247">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-248">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f60f-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-250">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0f60f-250">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0f60f-251">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="0f60f-251">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0f60f-252">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-252">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="0f60f-253">Wert</span><span class="sxs-lookup"><span data-stu-id="0f60f-253">Value</span></span>                                                                        | <span data-ttu-id="0f60f-254">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0f60f-254">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="0f60f-255"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0f60f-255"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0f60f-256">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="0f60f-256">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0f60f-257">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0f60f-257">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-258">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f60f-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-260">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="0f60f-260">The current health of the element.</span></span> <span data-ttu-id="0f60f-261">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="0f60f-261">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="0f60f-262">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="0f60f-262">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0f60f-263">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="0f60f-264">Wert</span><span class="sxs-lookup"><span data-stu-id="0f60f-264">Value</span></span>                                                                        | <span data-ttu-id="0f60f-265">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0f60f-265">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="0f60f-266"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0f60f-266"><dt>5</dt></span></span> </dl> | <span data-ttu-id="0f60f-267">Der Integritäts Status ist "Normal".</span><span class="sxs-lookup"><span data-stu-id="0f60f-267">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0f60f-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0f60f-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-269">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f60f-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-271">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="0f60f-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0f60f-272">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0f60f-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-276">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="0f60f-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-277">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0f60f-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0f60f-278">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-279">**Name**</span><span class="sxs-lookup"><span data-stu-id="0f60f-279">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-282">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0f60f-282">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-283">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0f60f-283">The label by which the object is known.</span></span> <span data-ttu-id="0f60f-284">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "replicasvc" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "replicasvc".</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-285">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="0f60f-285">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-286">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f60f-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-288">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0f60f-288">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0f60f-289">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f60f-289">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0f60f-290">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-290">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0f60f-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0f60f-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="0f60f-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="0f60f-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="0f60f-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="0f60f-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="0f60f-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="0f60f-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="0f60f-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="0f60f-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="0f60f-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="0f60f-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="0f60f-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="0f60f-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="0f60f-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="0f60f-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="0f60f-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="0f60f-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0f60f-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0f60f-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0f60f-310">)</span><span class="sxs-lookup"><span data-stu-id="0f60f-310">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0f60f-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0f60f-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-312">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0f60f-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-314">Ein Array, das die aktuellen Status des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="0f60f-314">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="0f60f-315">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="0f60f-316">Der Wert bei Index 0 (null) ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="0f60f-316">The value at index zero will be one of the following values.</span></span>



| <span data-ttu-id="0f60f-317">Wert</span><span class="sxs-lookup"><span data-stu-id="0f60f-317">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="0f60f-318">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0f60f-318">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="0f60f-319"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0f60f-319"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                  | <span data-ttu-id="0f60f-320">Der Replikations Dienst wird normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-320">The replication service is operating normally.</span></span><br/>                                                                     |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span><dl> <span data-ttu-id="0f60f-321"><dt>**Fehler**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0f60f-321"><dt>**Error**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="0f60f-322">Mindestens ein replikationsnetzwerklistener wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-322">One or more replication network listeners are not running.</span></span> <span data-ttu-id="0f60f-323">Überprüfen Sie, ob die Replikations Dienst Einstellungen gültig sind.</span><span class="sxs-lookup"><span data-stu-id="0f60f-323">Verify that the replication service settings are valid.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0f60f-324">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="0f60f-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-327">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0f60f-327">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="0f60f-328">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="0f60f-328">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0f60f-329">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-330">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="0f60f-330">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-333">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0f60f-333">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-334">Alle Informationen dazu, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="0f60f-334">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="0f60f-335">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-335">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-336">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="0f60f-336">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-339">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="0f60f-339">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-340">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="0f60f-340">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="0f60f-341">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0f60f-341">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="0f60f-342">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-342">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-343">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="0f60f-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-344">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f60f-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-346">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="0f60f-346">Provides high level status information.</span></span> <span data-ttu-id="0f60f-347">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0f60f-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0f60f-348">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f60f-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0f60f-349">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0f60f-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0f60f-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="0f60f-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="0f60f-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="0f60f-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0f60f-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0f60f-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0f60f-356">)</span><span class="sxs-lookup"><span data-stu-id="0f60f-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0f60f-357">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0f60f-357">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-358">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f60f-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-360">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="0f60f-360">The last requested or desired state for the element.</span></span> <span data-ttu-id="0f60f-361">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-361">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0f60f-362">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuellen Zustände für ein Element zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="0f60f-362">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="0f60f-363">Eine bestimmte Instanz der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse unterstützt die **requestedstate** -Eigenschaft möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="0f60f-363">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="0f60f-364">Wenn dies auftritt, wird der Wert 12 ("nicht zutreffend") verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f60f-364">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="0f60f-365">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-365">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="0f60f-366">Wert</span><span class="sxs-lookup"><span data-stu-id="0f60f-366">Value</span></span>                                                                         | <span data-ttu-id="0f60f-367">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0f60f-367">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="0f60f-368"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0f60f-368"><dt>12</dt></span></span> </dl> | <span data-ttu-id="0f60f-369">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0f60f-369">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0f60f-370">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="0f60f-370">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-371">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0f60f-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-373">Gibt an, ob der Dienst gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f60f-373">Indicates whether the service is currently running.</span></span> <span data-ttu-id="0f60f-374">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-374">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-375">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="0f60f-375">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-378">Qualifizierer: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="0f60f-378">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-379">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0f60f-379">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="0f60f-380">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-380">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-381">**Status**</span><span class="sxs-lookup"><span data-stu-id="0f60f-381">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-384">Gibt den Status des Elements an.</span><span class="sxs-lookup"><span data-stu-id="0f60f-384">Indicates the status of the element.</span></span> <span data-ttu-id="0f60f-385">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-386">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="0f60f-386">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-387">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0f60f-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-389">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0f60f-389">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0f60f-390">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-391">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="0f60f-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-392">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-394">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0f60f-394">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-395">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="0f60f-395">The scoping system's creation class name.</span></span> <span data-ttu-id="0f60f-396">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-396">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-397">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="0f60f-397">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-398">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f60f-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-400">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0f60f-400">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-401">Der NetBIOS-Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="0f60f-401">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="0f60f-402">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-402">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-403">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="0f60f-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-404">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f60f-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-406">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0f60f-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0f60f-407">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f60f-408">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="0f60f-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f60f-409">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f60f-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f60f-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f60f-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f60f-411">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="0f60f-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0f60f-412">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f60f-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f60f-413">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f60f-413">Requirements</span></span>



| <span data-ttu-id="0f60f-414">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f60f-414">Requirement</span></span> | <span data-ttu-id="0f60f-415">Wert</span><span class="sxs-lookup"><span data-stu-id="0f60f-415">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f60f-416">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f60f-416">Minimum supported client</span></span><br/> | <span data-ttu-id="0f60f-417">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f60f-417">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0f60f-418">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f60f-418">Minimum supported server</span></span><br/> | <span data-ttu-id="0f60f-419">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f60f-419">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f60f-420">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f60f-420">Namespace</span></span><br/>                | <span data-ttu-id="0f60f-421">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0f60f-421">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0f60f-422">MOF</span><span class="sxs-lookup"><span data-stu-id="0f60f-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f60f-423"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0f60f-423"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f60f-424">DLL</span><span class="sxs-lookup"><span data-stu-id="0f60f-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f60f-425"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f60f-425"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

