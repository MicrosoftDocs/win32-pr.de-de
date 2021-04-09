---
description: Die CIM- \_ Prozess Klasse stellt eine einzelne Instanz eines laufenden Programms dar. Ein Benutzer sieht in der Regel einen Prozess als Anwendung oder Aufgabe.
ms.assetid: 8b00ef6e-5c7f-410c-9e48-1205ea6e5a4c
ms.tgt_platform: multiple
title: CIM_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Process
- CIM_Process.Caption
- CIM_Process.CreationClassName
- CIM_Process.CreationDate
- CIM_Process.CSCreationClassName
- CIM_Process.CSName
- CIM_Process.Description
- CIM_Process.ExecutionState
- CIM_Process.Handle
- CIM_Process.InstallDate
- CIM_Process.KernelModeTime
- CIM_Process.Name
- CIM_Process.OSCreationClassName
- CIM_Process.OSName
- CIM_Process.Priority
- CIM_Process.Status
- CIM_Process.TerminationDate
- CIM_Process.UserModeTime
- CIM_Process.WorkingSetSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 355e29929dc05a701a2beac0919a28aca573ca9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958583"
---
# <a name="cim_process-class"></a><span data-ttu-id="f04b4-104">CIM- \_ Prozess Klasse</span><span class="sxs-lookup"><span data-stu-id="f04b4-104">CIM\_Process class</span></span>

<span data-ttu-id="f04b4-105">Die **CIM- \_ Prozess** Klasse stellt eine einzelne Instanz eines laufenden Programms dar.</span><span class="sxs-lookup"><span data-stu-id="f04b4-105">The **CIM\_Process** class represents a single instance of a running program.</span></span> <span data-ttu-id="f04b4-106">Ein Benutzer sieht in der Regel einen Prozess als Anwendung oder Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="f04b4-106">A user typically sees a process as an application or task.</span></span> <span data-ttu-id="f04b4-107">Ein Prozess wird durch einen Arbeitsbereich mit Speicherressourcen und Umgebungseinstellungen definiert, die ihm zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f04b4-107">A process is defined by a workspace of memory resources and environmental settings that are allocated to it.</span></span> <span data-ttu-id="f04b4-108">In einem Multitasking-System verhindert der Arbeitsbereich den Eindring Versuch von Ressourcen durch andere Prozesse.</span><span class="sxs-lookup"><span data-stu-id="f04b4-108">On a multitasking system, the workspace prevents intrusion of resources by other processes.</span></span> <span data-ttu-id="f04b4-109">Außerdem kann ein Prozess als mehrere Threads ausgeführt werden, die alle innerhalb desselben Arbeitsbereichs ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f04b4-109">Additionally, a process can execute as multiple threads, all which run within the same workspace.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f04b4-110">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f04b4-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f04b4-111">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f04b4-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f04b4-112">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f04b4-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f04b4-113">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f04b4-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04b4-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="f04b4-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C566-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes (CIM)"), AMENDMENT]
class CIM_Process : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  string   Status;
  datetime TerminationDate;
  uint64   UserModeTime;
  uint64   WorkingSetSize;
};
```

## <a name="members"></a><span data-ttu-id="f04b4-115">Member</span><span class="sxs-lookup"><span data-stu-id="f04b4-115">Members</span></span>

<span data-ttu-id="f04b4-116">Die **CIM- \_ Prozess** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f04b4-116">The **CIM\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="f04b4-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f04b4-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f04b4-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f04b4-118">Properties</span></span>

<span data-ttu-id="f04b4-119">Die **CIM- \_ Prozess** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f04b4-119">The **CIM\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f04b4-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f04b4-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-123">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f04b4-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-124">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f04b4-124">Short textual description of the object.</span></span>

<span data-ttu-id="f04b4-125">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f04b4-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-126">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f04b4-126">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-129">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Klassen Name")</span><span class="sxs-lookup"><span data-stu-id="f04b4-129">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-130">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f04b4-130">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f04b4-131">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f04b4-131">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-132">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="f04b4-132">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-133">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f04b4-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-135">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("up date")</span><span class="sxs-lookup"><span data-stu-id="f04b4-135">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-136">Uhrzeit, zu der die Ausführung des Prozesses begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="f04b4-136">Time that the process began executing.</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-137">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f04b4-137">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-140">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Name der Computer System Klasse ")</span><span class="sxs-lookup"><span data-stu-id="f04b4-140">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-141">Der Name der Erstellungs Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="f04b4-141">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-142">**CSName**</span><span class="sxs-lookup"><span data-stu-id="f04b4-142">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-145">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Csname**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="f04b4-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-146">Der Name des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f04b4-146">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f04b4-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-150">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f04b4-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-151">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f04b4-151">Textual description of the object.</span></span>

<span data-ttu-id="f04b4-152">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f04b4-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-153">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="f04b4-153">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-154">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f04b4-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-156">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ausführungs Status")</span><span class="sxs-lookup"><span data-stu-id="f04b4-156">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-157">Aktueller Betriebszustand des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="f04b4-157">Current operating condition of the process.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f04b4-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f04b4-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f04b4-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f04b4-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="f04b4-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Bereit** (2)</span><span class="sxs-lookup"><span data-stu-id="f04b4-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="f04b4-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="f04b4-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="f04b4-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blockiert** (4)</span><span class="sxs-lookup"><span data-stu-id="f04b4-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="f04b4-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Gesperrt** (5)</span><span class="sxs-lookup"><span data-stu-id="f04b4-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f04b4-164">Blockiert gesperrt</span><span class="sxs-lookup"><span data-stu-id="f04b4-164">Suspended blocked</span></span>

</dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="f04b4-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>Angeh **alten (6** )</span><span class="sxs-lookup"><span data-stu-id="f04b4-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f04b4-166">Angehalten</span><span class="sxs-lookup"><span data-stu-id="f04b4-166">Suspended ready</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="f04b4-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Beendet** (7)</span><span class="sxs-lookup"><span data-stu-id="f04b4-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="f04b4-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (8)</span><span class="sxs-lookup"><span data-stu-id="f04b4-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="f04b4-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Wächst** (9)</span><span class="sxs-lookup"><span data-stu-id="f04b4-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f04b4-170">**Handle**</span><span class="sxs-lookup"><span data-stu-id="f04b4-170">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-173">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("handle")</span><span class="sxs-lookup"><span data-stu-id="f04b4-173">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-174">Gibt den Prozess an.</span><span class="sxs-lookup"><span data-stu-id="f04b4-174">Identifies the process.</span></span> <span data-ttu-id="f04b4-175">Ein Prozess Bezeichner ist eine Art Prozess handle.</span><span class="sxs-lookup"><span data-stu-id="f04b4-175">A process identifier is a kind of process handle.</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-176">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f04b4-176">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-177">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f04b4-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-179">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="f04b4-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-180">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f04b4-180">Date and time the object was installed.</span></span> <span data-ttu-id="f04b4-181">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f04b4-181">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f04b4-182">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f04b4-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-183">**Kernelmodetime**</span><span class="sxs-lookup"><span data-stu-id="f04b4-183">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-184">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f04b4-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-186">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kernel Model Time"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="f04b4-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kernel Model Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-187">Zeit im Kernel Modus in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="f04b4-187">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="f04b4-188">Wenn diese Informationen nicht verfügbar sind, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f04b4-188">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="f04b4-189">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f04b4-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-190">**Name**</span><span class="sxs-lookup"><span data-stu-id="f04b4-190">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-193">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f04b4-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-194">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f04b4-194">Label by which the object is known.</span></span> <span data-ttu-id="f04b4-195">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f04b4-195">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f04b4-196">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f04b4-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-197">**Oscreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f04b4-197">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-200">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Betriebs System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="f04b4-200">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-201">Der Name der Erstellungs Klasse des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="f04b4-201">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-202">**OSName**</span><span class="sxs-lookup"><span data-stu-id="f04b4-202">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-205">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Betriebs System Name ")</span><span class="sxs-lookup"><span data-stu-id="f04b4-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-206">Der Name des Betriebssystems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f04b4-206">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-207">**Priority**</span><span class="sxs-lookup"><span data-stu-id="f04b4-207">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-208">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f04b4-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-210">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priorität")</span><span class="sxs-lookup"><span data-stu-id="f04b4-210">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-211">Dringlichkeit oder Wichtigkeit für die Prozess Ausführung.</span><span class="sxs-lookup"><span data-stu-id="f04b4-211">Urgency or importance for process execution.</span></span> <span data-ttu-id="f04b4-212">Wenn für einen Prozess keine Priorität definiert ist, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f04b4-212">If a priority is not defined for a process, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-213">**Status**</span><span class="sxs-lookup"><span data-stu-id="f04b4-213">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f04b4-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-216">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f04b4-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-217">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f04b4-217">Current status of the object.</span></span>

<span data-ttu-id="f04b4-218">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f04b4-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f04b4-219">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="f04b4-219">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f04b4-220">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f04b4-220">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f04b4-221">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f04b4-221">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f04b4-222">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f04b4-222">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f04b4-223">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f04b4-223">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f04b4-224">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f04b4-224">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f04b4-225">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f04b4-225">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f04b4-226">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="f04b4-226">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f04b4-227">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f04b4-227">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f04b4-228">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="f04b4-228">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f04b4-229">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="f04b4-229">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f04b4-230">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="f04b4-230">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f04b4-231">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="f04b4-231">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f04b4-232">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="f04b4-232">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-233">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f04b4-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-235">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Beendigungs Datum")</span><span class="sxs-lookup"><span data-stu-id="f04b4-235">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-236">Uhrzeit, zu der der Prozess beendet oder beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f04b4-236">Time that the process was stopped or terminated.</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-237">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="f04b4-237">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-238">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f04b4-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-240">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Benutzermoduszeit"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="f04b4-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("User Mode Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-241">Zeit im Benutzermodus in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="f04b4-241">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="f04b4-242">Wenn diese Informationen nicht verfügbar sind, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f04b4-242">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="f04b4-243">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f04b4-243">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f04b4-244">**Workingsetsize**</span><span class="sxs-lookup"><span data-stu-id="f04b4-244">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f04b4-245">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f04b4-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f04b4-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f04b4-247">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Workingsetgröße"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="f04b4-247">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Working Set Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f04b4-248">Umfang des Arbeitsspeichers in Bytes, der von einem Prozess für ein Betriebssystem mit Seiten basierter Speicherverwaltung effizient ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f04b4-248">Amount of memory, in bytes, that a process needs to execute efficiently for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="f04b4-249">Wenn das System nicht über genügend Arbeitsspeicher verfügt (weniger als die Workingsetgröße), tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="f04b4-249">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="f04b4-250">Wenn die Größe des Workingsets nicht bekannt ist, verwenden Sie **null** oder 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f04b4-250">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="f04b4-251">Wenn Workingsetdaten bereitgestellt werden, können Sie die Informationen überwachen, um die veränderlichen Arbeitsspeicher Anforderungen eines Prozesses zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="f04b4-251">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="f04b4-252">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f04b4-252">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f04b4-253">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f04b4-253">Remarks</span></span>

<span data-ttu-id="f04b4-254">Die **CIM- \_ Prozess** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f04b4-254">The **CIM\_Process** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="f04b4-255">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f04b4-255">WMI does not implement this class.</span></span> <span data-ttu-id="f04b4-256">Informationen zu WMI-Klassen, die vom **CIM- \_ Prozess** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="f04b4-256">For WMI classes derived from **CIM\_Process**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f04b4-257">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f04b4-257">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f04b4-258">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f04b4-258">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f04b4-259">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f04b4-259">Requirements</span></span>



| <span data-ttu-id="f04b4-260">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f04b4-260">Requirement</span></span> | <span data-ttu-id="f04b4-261">Wert</span><span class="sxs-lookup"><span data-stu-id="f04b4-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f04b4-262">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f04b4-262">Minimum supported client</span></span><br/> | <span data-ttu-id="f04b4-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f04b4-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f04b4-264">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f04b4-264">Minimum supported server</span></span><br/> | <span data-ttu-id="f04b4-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f04b4-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f04b4-266">Namespace</span><span class="sxs-lookup"><span data-stu-id="f04b4-266">Namespace</span></span><br/>                | <span data-ttu-id="f04b4-267">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f04b4-267">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f04b4-268">MOF</span><span class="sxs-lookup"><span data-stu-id="f04b4-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f04b4-269"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f04b4-269"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f04b4-270">DLL</span><span class="sxs-lookup"><span data-stu-id="f04b4-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f04b4-271"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f04b4-271"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f04b4-272">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f04b4-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f04b4-273">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="f04b4-273">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

