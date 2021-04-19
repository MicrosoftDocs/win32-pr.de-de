---
description: Die CIM \_ clusteringservice-Klasse stellt die Funktionalität dar, die von einem Cluster bereitgestellt wird. Beispielsweise können Failoverfunktionen als Dienst eines Failoverclusters modelliert werden.
ms.assetid: 550e3be3-c1e2-4714-b702-49cb1213c65b
ms.tgt_platform: multiple
title: CIM_ClusteringService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService
- CIM_ClusteringService.Caption
- CIM_ClusteringService.Description
- CIM_ClusteringService.InstallDate
- CIM_ClusteringService.Status
- CIM_ClusteringService.CreationClassName
- CIM_ClusteringService.Name
- CIM_ClusteringService.Started
- CIM_ClusteringService.StartMode
- CIM_ClusteringService.SystemCreationClassName
- CIM_ClusteringService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 40dc0ebd8daebb79c323d54591fc16126e0ef97a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344614"
---
# <a name="cim_clusteringservice-class"></a><span data-ttu-id="f1128-104">CIM \_ clusteringservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="f1128-104">CIM\_ClusteringService class</span></span>

<span data-ttu-id="f1128-105">Die **CIM \_ clusteringservice** -Klasse stellt die Funktionalität dar, die von einem Cluster bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f1128-105">The **CIM\_ClusteringService** class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="f1128-106">Beispielsweise können Failoverfunktionen als Dienst eines Failoverclusters modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="f1128-106">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1128-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f1128-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f1128-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f1128-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f1128-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f1128-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f1128-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f1128-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1128-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1128-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{debac832-6b54-4add-8a62-8d3861b97b1d}"), AMENDMENT]
class CIM_ClusteringService : CIM_Service
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="f1128-112">Member</span><span class="sxs-lookup"><span data-stu-id="f1128-112">Members</span></span>

<span data-ttu-id="f1128-113">Die **CIM \_ clusteringservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f1128-113">The **CIM\_ClusteringService** class has these types of members:</span></span>

-   [<span data-ttu-id="f1128-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="f1128-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1128-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1128-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1128-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="f1128-116">Methods</span></span>

<span data-ttu-id="f1128-117">Die **CIM \_ clusteringservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f1128-117">The **CIM\_ClusteringService** class has these methods.</span></span>



| <span data-ttu-id="f1128-118">Methode</span><span class="sxs-lookup"><span data-stu-id="f1128-118">Method</span></span>                                                                     | <span data-ttu-id="f1128-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1128-119">Description</span></span>                                                                                                |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1128-120">**AddNode**</span><span class="sxs-lookup"><span data-stu-id="f1128-120">**AddNode**</span></span>](addnode-method-in-class-cim-clusteringservice.md)           | <span data-ttu-id="f1128-121">Klassenmethode, mit der ein neues Computersystem in einen Cluster integriert wird.</span><span class="sxs-lookup"><span data-stu-id="f1128-121">Class method that brings a new computer system into a cluster.</span></span> <span data-ttu-id="f1128-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1128-122">Not implemented by WMI.</span></span><br/>          |
| [<span data-ttu-id="f1128-123">**Evictnode**</span><span class="sxs-lookup"><span data-stu-id="f1128-123">**EvictNode**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)       | <span data-ttu-id="f1128-124">Klassenmethode, mit der ein Computersystem aus einem Cluster entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f1128-124">Class method that removes a computer system from a cluster.</span></span> <span data-ttu-id="f1128-125">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1128-125">Not implemented by WMI.</span></span><br/>             |
| [<span data-ttu-id="f1128-126">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="f1128-126">**StartService**</span></span>](startservice-method-in-class-cim-clusteringservice.md) | <span data-ttu-id="f1128-127">Klassenmethode, die versucht, den Dienst in seinen Startzustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="f1128-127">Class method that attempts to place the service into its startup state.</span></span> <span data-ttu-id="f1128-128">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1128-128">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="f1128-129">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="f1128-129">**StopService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)   | <span data-ttu-id="f1128-130">Klassenmethode, die den Dienst in den Zustand "beendet" versetzt.</span><span class="sxs-lookup"><span data-stu-id="f1128-130">Class method that places the service in the stopped state.</span></span> <span data-ttu-id="f1128-131">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1128-131">Not implemented by WMI.</span></span><br/>              |



 

### <a name="properties"></a><span data-ttu-id="f1128-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1128-132">Properties</span></span>

<span data-ttu-id="f1128-133">Die **CIM \_ clusteringservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1128-133">The **CIM\_ClusteringService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1128-134">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f1128-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1128-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-137">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f1128-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f1128-138">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1128-138">A short textual description of the object.</span></span>

<span data-ttu-id="f1128-139">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1128-140">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f1128-140">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1128-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-143">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="f1128-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f1128-144">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1128-144">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f1128-145">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f1128-145">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f1128-146">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-146">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1128-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1128-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1128-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-150">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f1128-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f1128-151">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1128-151">A textual description of the object.</span></span>

<span data-ttu-id="f1128-152">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1128-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f1128-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-154">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1128-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-156">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="f1128-156">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f1128-157">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1128-157">Indicates when the object was installed.</span></span> <span data-ttu-id="f1128-158">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f1128-158">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f1128-159">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1128-160">**Name**</span><span class="sxs-lookup"><span data-stu-id="f1128-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1128-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-163">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1128-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f1128-164">Die Name-Eigenschaft identifiziert den Dienst eindeutig und gibt Aufschluss über die verwaltete Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="f1128-164">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="f1128-165">Diese Funktionalität wird in der Description-Eigenschaft des Objekts ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f1128-165">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="f1128-166">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-166">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1128-167">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="f1128-167">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-168">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f1128-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-170">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="f1128-170">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="f1128-171">**True** gibt an, dass der Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="f1128-171">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="f1128-172">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-172">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1128-173">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="f1128-173">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1128-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-176">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Modus")</span><span class="sxs-lookup"><span data-stu-id="f1128-176">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="f1128-177">Gibt an, ob der Dienst automatisch gestartet wird (z. b. durch ein Betriebssystem) oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f1128-177">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="f1128-178">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-178">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="f1128-179">**Automatisch** ("automatisch")</span><span class="sxs-lookup"><span data-stu-id="f1128-179">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="f1128-180">**Manuell** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="f1128-180">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1128-181">**Status**</span><span class="sxs-lookup"><span data-stu-id="f1128-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1128-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-184">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f1128-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f1128-185">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="f1128-185">String that indicates the current status of the object.</span></span> <span data-ttu-id="f1128-186">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1128-186">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f1128-187">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f1128-187">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f1128-188">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="f1128-188">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f1128-189">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f1128-189">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f1128-190">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f1128-190">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f1128-191">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f1128-191">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f1128-192">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f1128-193">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="f1128-193">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f1128-194">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f1128-194">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f1128-195">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f1128-195">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f1128-196">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f1128-196">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1128-197">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f1128-197">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f1128-198">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f1128-198">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f1128-199">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f1128-199">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f1128-200">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="f1128-200">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f1128-201">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f1128-201">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f1128-202">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="f1128-202">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f1128-203">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="f1128-203">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f1128-204">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="f1128-204">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f1128-205">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="f1128-205">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1128-206">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f1128-206">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1128-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-209">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Klassenname")</span><span class="sxs-lookup"><span data-stu-id="f1128-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f1128-210">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f1128-210">Scoping system's creation class name.</span></span>

<span data-ttu-id="f1128-211">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-211">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1128-212">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="f1128-212">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1128-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1128-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1128-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1128-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1128-215">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="f1128-215">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="f1128-216">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="f1128-216">Name of the system that hosts the service.</span></span>

<span data-ttu-id="f1128-217">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1128-217">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1128-218">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1128-218">Remarks</span></span>

<span data-ttu-id="f1128-219">Die **CIM \_ clusteringservice** -Klasse wird vom [**CIM- \_ Dienst**](cim-service.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f1128-219">The **CIM\_ClusteringService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="f1128-220">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1128-220">WMI does not implement this class.</span></span>

<span data-ttu-id="f1128-221">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f1128-221">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f1128-222">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f1128-222">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1128-223">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1128-223">Requirements</span></span>



| <span data-ttu-id="f1128-224">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1128-224">Requirement</span></span> | <span data-ttu-id="f1128-225">Wert</span><span class="sxs-lookup"><span data-stu-id="f1128-225">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1128-226">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1128-226">Minimum supported client</span></span><br/> | <span data-ttu-id="f1128-227">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1128-227">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1128-228">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1128-228">Minimum supported server</span></span><br/> | <span data-ttu-id="f1128-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1128-229">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1128-230">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1128-230">Namespace</span></span><br/>                | <span data-ttu-id="f1128-231">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f1128-231">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1128-232">MOF</span><span class="sxs-lookup"><span data-stu-id="f1128-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1128-233"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f1128-233"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1128-234">DLL</span><span class="sxs-lookup"><span data-stu-id="f1128-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1128-235"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1128-235"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1128-236">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1128-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1128-237">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="f1128-237">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

