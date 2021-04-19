---
description: Eine konkrete Version der CIM- \_ Auftrags Klasse. Diese Klasse stellt eine generische instanziier Bare Arbeitseinheit dar, die ausgeführt werden soll, z. b. einen Batch oder einen Druckauftrag.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: CIM_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356819"
---
# <a name="cim_concretejob-class"></a><span data-ttu-id="3a3d2-104">CIM- \_ Klasse "concretejob"</span><span class="sxs-lookup"><span data-stu-id="3a3d2-104">CIM\_ConcreteJob class</span></span>

<span data-ttu-id="3a3d2-105">Eine konkrete Version der [**CIM- \_ Auftrags**](cim-job.md) Klasse.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-105">A concrete version of the [**CIM\_Job**](cim-job.md) class.</span></span> <span data-ttu-id="3a3d2-106">Diese Klasse stellt eine generische instanziier Bare Arbeitseinheit dar, die ausgeführt werden soll, z. b. einen Batch oder einen Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-106">This class represent a generic instantiable unit of work to run, such as a batch or a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a3d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a3d2-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a><span data-ttu-id="3a3d2-108">Member</span><span class="sxs-lookup"><span data-stu-id="3a3d2-108">Members</span></span>

<span data-ttu-id="3a3d2-109">Die CIM-Klasse " **\_ concretejob** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3a3d2-109">The **CIM\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="3a3d2-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="3a3d2-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a3d2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a3d2-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a3d2-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="3a3d2-112">Methods</span></span>

<span data-ttu-id="3a3d2-113">Die CIM-Klasse " **\_ concretejob** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-113">The **CIM\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="3a3d2-114">Methode</span><span class="sxs-lookup"><span data-stu-id="3a3d2-114">Method</span></span>                                                           | <span data-ttu-id="3a3d2-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a3d2-115">Description</span></span>                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a3d2-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-116">**GetError**</span></span>](cim-concretejob-geterror.md)                     | <span data-ttu-id="3a3d2-117">Hiermit werden Fehlerinformationen für den Betriebsstatus eines konkreten Auftrags abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-117">Retrieves error information for the operational status of a concrete job.</span></span><br/> |
| [<span data-ttu-id="3a3d2-118">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-118">**RequestStateChange**</span></span>](cim-concretejob-requeststatechange.md) | <span data-ttu-id="3a3d2-119">Fordert die angegebene Zustandsänderung an einen konkreten Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-119">Requests the specified state change to a concrete job.</span></span><br/>                    |



 

### <a name="properties"></a><span data-ttu-id="3a3d2-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a3d2-120">Properties</span></span>

<span data-ttu-id="3a3d2-121">Die CIM-Klasse " **\_ concretejob** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-121">The **CIM\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a3d2-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a3d2-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a3d2-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a3d2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a3d2-125">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="3a3d2-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="3a3d2-126">Eindeutig und verdeckt identifiziert eine Instanz dieser Klasse innerhalb des Gültigkeits Bereichs des enthaltenden Namespace.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-126">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="3a3d2-127">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert der **InstanceId-** Eigenschaft im folgenden Muster erstellt werden: *OrgId*:*localId*</span><span class="sxs-lookup"><span data-stu-id="3a3d2-127">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="3a3d2-128">*OrgId* muss einen urheberrechtlich geschützten oder anderweitig eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die die **InstanceId** definiert, oder eine registrierte ID ist, die von einer anerkannten globalen Autorität zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-128">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="3a3d2-129">Dieses Muster ähnelt der Struktur von Schema Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-129">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="3a3d2-130">Um die Eindeutigkeit sicherzustellen, muss der erste Doppelpunkt in **InstanceId** zwischen der *OrgId* und der *Lok-* ID liegen.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-130">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="3a3d2-131">Daher darf die *OrgId* keinen Doppelpunkt (': ') enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-131">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="3a3d2-132">*LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-132">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="3a3d2-133">Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceId** -Wert nicht für **InstanceId** -Eigenschaften wieder verwendet wird, die von diesem Anbieter oder von anderen Anbietern für diesen Namespace erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-133">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="3a3d2-134">Für von DMTF (verteilte Management Task Force) definierte Instanzen muss das Muster verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-134">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="3a3d2-135">**JobState**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-135">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a3d2-136">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a3d2-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a3d2-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a3d2-138">Der Betriebsstatus des Auftrags und der Übergang zwischen diesen Zuständen.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-138">The operational state of the job, and the transition between those states.</span></span>

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span data-ttu-id="3a3d2-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**Neu** (2)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**New** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-140">der Auftrag wurde nie gestartet.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-140">the job has never been started.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3a3d2-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-142">Der Auftrag wechselt von den Zuständen "neu", "angehalten" oder "Dienst" in den Zustand "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="3a3d2-142">The job is moving from the 'New', 'Suspended', or 'Service' states into the 'Running' state.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="3a3d2-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (4)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-144">Der Auftrag wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-144">The Job is running.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="3a3d2-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>Angeh **alten (5** )</span><span class="sxs-lookup"><span data-stu-id="3a3d2-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-146">Der Auftrag wurde angehalten, kann jedoch nahtlos neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-146">The Job is stopped, but can be restarted in a seamless manner.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="3a3d2-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (6)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-148">Der Auftrag wechselt in den Zustand "abgeschlossen", "beendet" oder "abgebrochen".</span><span class="sxs-lookup"><span data-stu-id="3a3d2-148">The job is moving to a 'Completed', 'Terminated', or 'Killed' state.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="3a3d2-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (7)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-150">Der Auftrag wurde normal abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-150">The job has completed normally.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="3a3d2-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Beendet** (8)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-152">Der Auftrag wurde mit dem Status "beenden" beendet Change Request.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-152">The job has been stopped by a 'Terminate' state change request.</span></span> <span data-ttu-id="3a3d2-153">Der Auftrag und alle zugrunde liegenden Prozesse werden beendet und können (Dies ist Auftrags spezifisch) nur als neuer Auftrag neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-153">The job and all its underlying processes are ended and can be restarted (this is job-specific) only as a new job.</span></span>

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span data-ttu-id="3a3d2-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>Abgeb **Rochen (9** )</span><span class="sxs-lookup"><span data-stu-id="3a3d2-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Killed** (9)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-155">Der Auftrag wurde mit dem Status "Kill" beendet Change Request.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-155">The job has been stopped by a 'Kill' state change request.</span></span> <span data-ttu-id="3a3d2-156">Die zugrunde liegenden Prozesse wurden möglicherweise noch ausgeführt, und die Bereinigung ist möglicherweise erforderlich, um Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-156">Underlying processes might have been left running, and cleanup might be required to free up resources.</span></span>

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span data-ttu-id="3a3d2-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Ausnahme** (10)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exception** (10)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-158">Der Auftrag befindet sich in einem nicht ordnungsgemäßen Zustand, der möglicherweise auf eine Fehlerbedingung hinweist.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-158">The Job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="3a3d2-159">Der tatsächliche Status wird möglicherweise auch in auftragsspezifischen Objekten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-159">Actual status might be displayed though job-specific objects.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3a3d2-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (11)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-161">Der Auftrag befindet sich in einem herstellerspezifischen Zustand, der die Problem Ermittlung, Lösung oder beides unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-161">The Job is in a vendor-specific state that supports problem discovery, or resolution, or both</span></span>

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span data-ttu-id="3a3d2-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Abfrage ausstehend** (12)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query Pending** (12)</span></span>


</dt> <dd>

<span data-ttu-id="3a3d2-163">Es wird darauf gewartet, dass ein Client eine Abfrage auflöst.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-163">Waiting for a client to resolve a query.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3a3d2-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (13.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (13..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3a3d2-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a3d2-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a3d2-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a3d2-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a3d2-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a3d2-169">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Name")</span><span class="sxs-lookup"><span data-stu-id="3a3d2-169">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a3d2-170">Der benutzerfreundliche Name der-Instanz.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-170">The user-friendly name of the instance.</span></span> <span data-ttu-id="3a3d2-171">Außerdem kann der benutzerfreundliche Name als Eigenschaft für eine Suche oder Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-171">In addition, the user-friendly name can be used as a property for a search or query.</span></span>

> [!Note]  
> <span data-ttu-id="3a3d2-172">Der Name muss innerhalb des Namespace nicht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-172">The name does not have to be unique within the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="3a3d2-173">**Timebeforeremoval**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-173">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a3d2-174">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-174">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a3d2-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3a3d2-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3a3d2-176">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-176">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a3d2-177">Gibt an, wie lange ein abgeschlossener Auftrag beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-177">Indicates how long a completed job is retained.</span></span> <span data-ttu-id="3a3d2-178">Der Standardwert ist "00000000000500.000000:000" (fünf Minuten).</span><span class="sxs-lookup"><span data-stu-id="3a3d2-178">The default value is "00000000000500.000000:000" (five minutes).</span></span>

</dd> <dt>

<span data-ttu-id="3a3d2-179">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-179">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a3d2-180">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a3d2-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a3d2-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a3d2-182">Das Datum oder die Uhrzeit der letzten Änderung des Auftrags Zustands.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-182">The date or time when the state of the job last changed.</span></span>

> [!Note]  
> <span data-ttu-id="3a3d2-183">Wenn der Status des Auftrags nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3a3d2-183">If the state of the Job has not changed and this property is populated, then it must be set to a zero interval value.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a3d2-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a3d2-184">Requirements</span></span>



| <span data-ttu-id="3a3d2-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a3d2-185">Requirement</span></span> | <span data-ttu-id="3a3d2-186">Wert</span><span class="sxs-lookup"><span data-stu-id="3a3d2-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a3d2-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-187">Minimum supported client</span></span><br/> | <span data-ttu-id="3a3d2-188">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3a3d2-188">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3a3d2-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a3d2-189">Minimum supported server</span></span><br/> | <span data-ttu-id="3a3d2-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a3d2-190">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3a3d2-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a3d2-191">Namespace</span></span><br/>                | <span data-ttu-id="3a3d2-192">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a3d2-192">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3a3d2-193">MOF</span><span class="sxs-lookup"><span data-stu-id="3a3d2-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a3d2-194"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3a3d2-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a3d2-195">DLL</span><span class="sxs-lookup"><span data-stu-id="3a3d2-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a3d2-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a3d2-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a3d2-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a3d2-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a3d2-198">**CIM- \_ Auftrag**</span><span class="sxs-lookup"><span data-stu-id="3a3d2-198">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

