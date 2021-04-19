---
description: Die CIM- \_ Thread Klasse stellt die Möglichkeit dar, gleichzeitig Einheiten eines Prozesses oder einer Aufgabe auszuführen. Ein Prozess kann über viele Threads verfügen, von denen jede für den Prozess schwach ist.
ms.assetid: 57222d57-61bd-4641-a77c-805263be04b7
ms.tgt_platform: multiple
title: CIM_Thread-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Thread
- CIM_Thread.Caption
- CIM_Thread.CreationClassName
- CIM_Thread.CSCreationClassName
- CIM_Thread.CSName
- CIM_Thread.Description
- CIM_Thread.ExecutionState
- CIM_Thread.Handle
- CIM_Thread.InstallDate
- CIM_Thread.KernelModeTime
- CIM_Thread.Name
- CIM_Thread.OSCreationClassName
- CIM_Thread.OSName
- CIM_Thread.Priority
- CIM_Thread.ProcessCreationClassName
- CIM_Thread.ProcessHandle
- CIM_Thread.Status
- CIM_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0a69554ef50a82695d2904b11f4189c3aab11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342782"
---
# <a name="cim_thread-class"></a><span data-ttu-id="b4b8f-104">CIM- \_ Thread Klasse</span><span class="sxs-lookup"><span data-stu-id="b4b8f-104">CIM\_Thread class</span></span>

<span data-ttu-id="b4b8f-105">Die **CIM- \_ Thread** Klasse stellt die Möglichkeit dar, gleichzeitig Einheiten eines Prozesses oder einer Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-105">The **CIM\_Thread** class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="b4b8f-106">Ein Prozess kann über viele Threads verfügen, von denen jede für den Prozess schwach ist.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-106">A process can have many threads, each of which is weak to the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4b8f-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b4b8f-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b4b8f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b4b8f-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b4b8f-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b8f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4b8f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C571-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Thread : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
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
  string   ProcessCreationClassName;
  string   ProcessHandle;
  string   Status;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="b4b8f-112">Member</span><span class="sxs-lookup"><span data-stu-id="b4b8f-112">Members</span></span>

<span data-ttu-id="b4b8f-113">Die **CIM- \_ Thread** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b4b8f-113">The **CIM\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="b4b8f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4b8f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4b8f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4b8f-115">Properties</span></span>

<span data-ttu-id="b4b8f-116">Die **CIM- \_ Thread** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-116">The **CIM\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4b8f-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-121">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-121">Short textual description of the object.</span></span>

<span data-ttu-id="b4b8f-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-123">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-126">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-126">Qualifiers: [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-127">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b4b8f-128">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-128">When used with other key properties of the class, this property allow all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-132">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Prozess**](cim-process.md).**CSCreationClassName**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-133">Der Name der Erstellungs Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-133">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-137">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Prozess**](cim-process.md).**Csname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-138">Der Name des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-138">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-142">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-143">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-143">Textual description of the object.</span></span>

<span data-ttu-id="b4b8f-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-145">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-145">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-146">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-148">Gibt den aktuellen Betriebszustand des Threads an.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-148">Indicates the current operating condition of the thread.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4b8f-149">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4b8f-150">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="b4b8f-151">**Bereit** (2)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-151">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="b4b8f-152">Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-152">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="b4b8f-153">**Blockiert** (4)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-153">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="b4b8f-154">**Gesperrt** (5)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-154">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="b4b8f-155">Angeh **alten (6** )</span><span class="sxs-lookup"><span data-stu-id="b4b8f-155">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4b8f-156">**Handle**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-156">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-159">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-159">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-160">Der Bezeichner für den Thread.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-160">Identifier for the thread.</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-162">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-164">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-165">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-165">Date and time the object was installed.</span></span> <span data-ttu-id="b4b8f-166">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b4b8f-167">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-168">**Kernelmodetime**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-168">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-169">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-171">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-171">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-172">Zeit im Kernel Modus in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-172">Time, in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="b4b8f-173">Wenn diese Informationen nicht verfügbar sind, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-173">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="b4b8f-174">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4b8f-174">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-175">**Name**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-178">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-178">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-179">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-179">Label by which the object is known.</span></span> <span data-ttu-id="b4b8f-180">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-180">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b4b8f-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-182">**Oscreationclassname**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-182">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-185">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Prozess**](cim-process.md).**Oscreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-186">Der Name der Erstellungs Klasse des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-186">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-187">**OSName**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-187">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-190">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Prozess**](cim-process.md).**Osname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-190">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-191">Der Name des Betriebssystems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-191">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-192">**Priority**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-192">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-193">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-195">Dringlichkeit der Ausführung eines Threads.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-195">Urgency for execution of a thread.</span></span> <span data-ttu-id="b4b8f-196">Ein Thread kann eine andere Priorität haben als der besitzende Prozess.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-196">A thread can have a different priority than its owning process.</span></span> <span data-ttu-id="b4b8f-197">Wenn diese Informationen für einen Thread nicht verfügbar sind, sollte der Wert 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-197">If this information is not available for a thread, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-198">**Processcreationclassname**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-198">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-201">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Prozess**](cim-process.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-202">Erstellungs Klassenname des Bereichs Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-202">Scoping process's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-203">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-203">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-206">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Prozess**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-206">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-207">Handle des Bereichs Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-207">Scoping process's handle.</span></span>

</dd> <dt>

<span data-ttu-id="b4b8f-208">**Status**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-208">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-211">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-211">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-212">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-212">Current status of the object.</span></span> <span data-ttu-id="b4b8f-213">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b4b8f-214">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="b4b8f-214">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b4b8f-215">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-215">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b4b8f-216">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-216">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b4b8f-217">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-217">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4b8f-218">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-218">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b4b8f-219">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-219">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b4b8f-220">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-220">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b4b8f-221">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-221">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b4b8f-222">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-222">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b4b8f-223">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-223">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b4b8f-224">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-224">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b4b8f-225">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-225">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b4b8f-226">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-226">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4b8f-227">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-227">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b8f-228">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b8f-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b8f-230">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="b4b8f-230">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="b4b8f-231">Zeit im Benutzermodus in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-231">Time, in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="b4b8f-232">Wenn diese Informationen nicht verfügbar sind, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-232">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="b4b8f-233">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4b8f-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4b8f-234">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4b8f-234">Remarks</span></span>

<span data-ttu-id="b4b8f-235">Die **CIM- \_ Thread** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-235">The **CIM\_Thread** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="b4b8f-236">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-236">WMI does not implement this class.</span></span> <span data-ttu-id="b4b8f-237">Informationen zu WMI-Klassen, die vom **CIM- \_ Thread** abgeleitet werden, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-237">For WMI classes derived from **CIM\_Thread**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b4b8f-238">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-238">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b4b8f-239">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b4b8f-239">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b8f-240">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4b8f-240">Requirements</span></span>



| <span data-ttu-id="b4b8f-241">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4b8f-241">Requirement</span></span> | <span data-ttu-id="b4b8f-242">Wert</span><span class="sxs-lookup"><span data-stu-id="b4b8f-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b8f-243">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-243">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b8f-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4b8f-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4b8f-245">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4b8f-245">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b8f-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4b8f-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4b8f-247">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4b8f-247">Namespace</span></span><br/>                | <span data-ttu-id="b4b8f-248">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b4b8f-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b4b8f-249">MOF</span><span class="sxs-lookup"><span data-stu-id="b4b8f-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4b8f-250"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b4b8f-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4b8f-251">DLL</span><span class="sxs-lookup"><span data-stu-id="b4b8f-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4b8f-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4b8f-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b8f-253">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4b8f-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b8f-254">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="b4b8f-254">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

