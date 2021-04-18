---
description: Der Win32- \_ Thread&\# 8194; Die WMI-Klasse stellt einen Ausführungs Thread dar.
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Win32_Thread-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6e9f6a8c821aa327e8b810b634c85bb06459910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340130"
---
# <a name="win32_thread-class"></a><span data-ttu-id="18c4f-103">Win32- \_ Thread Klasse</span><span class="sxs-lookup"><span data-stu-id="18c4f-103">Win32\_Thread class</span></span>

<span data-ttu-id="18c4f-104">Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32- \_ Thread** stellt einen Ausführungs Thread dar.</span><span class="sxs-lookup"><span data-stu-id="18c4f-104">The **Win32\_Thread** [WMI class](../wmisdk/retrieving-a-class.md) represents a thread of execution.</span></span> <span data-ttu-id="18c4f-105">Während ein Prozess einen Ausführungs Thread aufweisen muss, kann der Prozess andere Threads erstellen, um Aufgaben parallel auszuführen.</span><span class="sxs-lookup"><span data-stu-id="18c4f-105">While a process must have one thread of execution, the process can create other threads to execute tasks in parallel.</span></span> <span data-ttu-id="18c4f-106">Threads nutzen die Prozessumgebung gemeinsam, sodass mehrere Threads im selben Prozess weniger Arbeitsspeicher verwenden als die gleiche Anzahl von Prozessen.</span><span class="sxs-lookup"><span data-stu-id="18c4f-106">Threads share the process environment, thus multiple threads under the same process use less memory than the same number of processes.</span></span>

<span data-ttu-id="18c4f-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18c4f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="18c4f-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="18c4f-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18c4f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="18c4f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="18c4f-110">Member</span><span class="sxs-lookup"><span data-stu-id="18c4f-110">Members</span></span>

<span data-ttu-id="18c4f-111">Die **Win32- \_ Thread** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="18c4f-111">The **Win32\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="18c4f-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18c4f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18c4f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18c4f-113">Properties</span></span>

<span data-ttu-id="18c4f-114">Die **Win32- \_ Thread** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18c4f-114">The **Win32\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18c4f-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="18c4f-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-118">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="18c4f-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-119">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="18c4f-119">Short description of the object.</span></span>

<span data-ttu-id="18c4f-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-121">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="18c4f-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-124">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="18c4f-124">Qualifiers: [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-125">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="18c4f-125">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="18c4f-126">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="18c4f-126">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="18c4f-127">Diese Eigenschaft wird vom [**CIM- \_ Thread**](cim-thread.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-127">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-128">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18c4f-128">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-131">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM- \_ Prozess**](cim-process.md).**CSCreationClassName**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="18c4f-131">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-132">Der Name der Erstellungs Klasse des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="18c4f-132">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="18c4f-133">Diese Eigenschaft wird vom [**CIM- \_ Thread**](cim-thread.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-133">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="18c4f-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-137">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM- \_ Prozess**](cim-process.md).**Csname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="18c4f-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-138">Name des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="18c4f-138">Name of the scoping computer system.</span></span>

<span data-ttu-id="18c4f-139">Diese Eigenschaft wird vom [**CIM- \_ Thread**](cim-thread.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-139">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18c4f-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-143">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="18c4f-143">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-144">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="18c4f-144">Description of the object.</span></span>

<span data-ttu-id="18c4f-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-146">**Verweilzeit**</span><span class="sxs-lookup"><span data-stu-id="18c4f-146">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-147">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18c4f-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-149">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Performance Data Structures \| [**perf \_ Object \_ Type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="18c4f-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-150">Gesamt Ausführungszeit in Millisekunden, die diesem Thread seit seiner Erstellung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="18c4f-150">Total execution time, in milliseconds, given to this thread since its creation.</span></span>

<span data-ttu-id="18c4f-151">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="18c4f-151">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-152">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="18c4f-152">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-153">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18c4f-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-155">Der aktuelle Betriebszustand des Threads.</span><span class="sxs-lookup"><span data-stu-id="18c4f-155">Current operating condition of the thread.</span></span>

<span data-ttu-id="18c4f-156">Diese Eigenschaft wird vom [**CIM- \_ Thread**](cim-thread.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-156">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18c4f-157">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="18c4f-157">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18c4f-158">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="18c4f-158">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="18c4f-159">**Bereit** (2)</span><span class="sxs-lookup"><span data-stu-id="18c4f-159">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="18c4f-160">Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="18c4f-160">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="18c4f-161">**Blockiert** (4)</span><span class="sxs-lookup"><span data-stu-id="18c4f-161">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="18c4f-162">**Gesperrt** (5)</span><span class="sxs-lookup"><span data-stu-id="18c4f-162">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="18c4f-163">Angeh **alten (6** )</span><span class="sxs-lookup"><span data-stu-id="18c4f-163">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18c4f-164">**Handle**</span><span class="sxs-lookup"><span data-stu-id="18c4f-164">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-167">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("handle"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID")</span><span class="sxs-lookup"><span data-stu-id="18c4f-167">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32ThreadID")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-168">Handle für einen Thread.</span><span class="sxs-lookup"><span data-stu-id="18c4f-168">Handle to a thread.</span></span> <span data-ttu-id="18c4f-169">Standardmäßig verfügt das Handle über vollständige Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="18c4f-169">The handle has full access rights by default.</span></span> <span data-ttu-id="18c4f-170">Mit dem korrekten Sicherheits Zugriff kann das Handle in jeder Funktion verwendet werden, die ein Thread handle akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="18c4f-170">With the correct security access, the handle can be used in any function that accepts a thread handle.</span></span> <span data-ttu-id="18c4f-171">Abhängig von dem Vererbungs Flag, das bei der Erstellung angegeben wird, kann dieses Handle von untergeordneten Prozessen geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="18c4f-171">Depending on the inheritance flag specified when it is created, this handle can be inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18c4f-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-173">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="18c4f-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-175">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="18c4f-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-176">Das Objekt wurde installiert.</span><span class="sxs-lookup"><span data-stu-id="18c4f-176">Object was installed.</span></span> <span data-ttu-id="18c4f-177">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="18c4f-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="18c4f-178">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-179">**Kernelmodetime**</span><span class="sxs-lookup"><span data-stu-id="18c4f-179">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-180">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18c4f-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-182">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("kernelmodetime"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Performance Data Structures \| [**perf \_ Object \_ Type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| privilegedtime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span><span class="sxs-lookup"><span data-stu-id="18c4f-182">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-183">Zeit im Kernel Modus in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="18c4f-183">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="18c4f-184">Wenn diese Informationen nicht verfügbar sind, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18c4f-184">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="18c4f-185">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="18c4f-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-186">**Name**</span><span class="sxs-lookup"><span data-stu-id="18c4f-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-189">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="18c4f-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-190">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="18c4f-190">Label by which the object is known.</span></span> <span data-ttu-id="18c4f-191">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="18c4f-191">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="18c4f-192">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-193">**Oscreationclassname**</span><span class="sxs-lookup"><span data-stu-id="18c4f-193">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-196">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM- \_ Prozess**](cim-process.md).**Oscreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="18c4f-196">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-197">Der Name der Erstellungs Klasse des Bereichs bezogenen Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="18c4f-197">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="18c4f-198">Diese Eigenschaft wird vom [**CIM- \_ Thread**](cim-thread.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-198">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-199">**OSName**</span><span class="sxs-lookup"><span data-stu-id="18c4f-199">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-202">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM- \_ Prozess**](cim-process.md).**Osname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="18c4f-202">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-203">Der Name des Bereichs bezogenen Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="18c4f-203">Name of the scoping operating system.</span></span>

<span data-ttu-id="18c4f-204">Diese Eigenschaft wird vom [**CIM- \_ Thread**](cim-thread.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-204">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-205">**Priority**</span><span class="sxs-lookup"><span data-stu-id="18c4f-205">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-206">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18c4f-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-208">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Priorität"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpdelta-pri")</span><span class="sxs-lookup"><span data-stu-id="18c4f-208">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|tpDeltaPri")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-209">Dynamische Priorität des Threads.</span><span class="sxs-lookup"><span data-stu-id="18c4f-209">Dynamic priority of the thread.</span></span> <span data-ttu-id="18c4f-210">Jeder Thread verfügt über eine dynamische Priorität, die der Scheduler verwendet, um zu bestimmen, welcher Thread ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="18c4f-210">Each thread has a dynamic priority that the scheduler uses to determine which thread to execute.</span></span> <span data-ttu-id="18c4f-211">Anfänglich ist die dynamische Priorität eines Threads mit der Basis Priorität identisch.</span><span class="sxs-lookup"><span data-stu-id="18c4f-211">Initially, a thread's dynamic priority is the same as its base priority.</span></span> <span data-ttu-id="18c4f-212">Das System kann die dynamische Priorität erhöhen und verringern, um sicherzustellen, dass Sie reaktionsfähig ist (es wird sichergestellt, dass keine Threads zur Prozessorzeit verhungert werden).</span><span class="sxs-lookup"><span data-stu-id="18c4f-212">The system can raise and lower the dynamic priority, to ensure that it is responsive (guaranteeing that no threads are starved for processor time).</span></span> <span data-ttu-id="18c4f-213">Das System erhöht die Priorität von Threads mit einer Basis Prioritätsstufe zwischen 16 und 31 nicht.</span><span class="sxs-lookup"><span data-stu-id="18c4f-213">The system does not boost the priority of threads with a base priority level between 16 and 31.</span></span> <span data-ttu-id="18c4f-214">Nur Threads mit einer Basis Priorität zwischen 0 und 15 empfangen dynamische Prioritäts Steigerungen.</span><span class="sxs-lookup"><span data-stu-id="18c4f-214">Only threads with a base priority between 0 and 15 receive dynamic priority boosts.</span></span> <span data-ttu-id="18c4f-215">Höhere Zahlen weisen auf höhere Prioritäten hin.</span><span class="sxs-lookup"><span data-stu-id="18c4f-215">Higher numbers indicate higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-216">**PriorityBase**</span><span class="sxs-lookup"><span data-stu-id="18c4f-216">**PriorityBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-217">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18c4f-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-219">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Performance Data Structures \| [**perf \_ Object \_ Type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| perfprioritybase")</span><span class="sxs-lookup"><span data-stu-id="18c4f-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfPriorityBase")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-220">Aktuelle Basis Priorität eines Threads.</span><span class="sxs-lookup"><span data-stu-id="18c4f-220">Current base priority of a thread.</span></span> <span data-ttu-id="18c4f-221">Das Betriebssystem kann die dynamische Priorität des Threads oberhalb der Basis Priorität erhöhen, wenn der Thread Benutzereingaben behandelt, oder Sie wird auf die Basis Priorität herabgestuft, wenn der Thread in die Compute-Bindung wechselt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-221">The operating system may raise the thread's dynamic priority above the base priority if the thread is handling user input, or lower it toward the base priority if the thread becomes compute-bound.</span></span> <span data-ttu-id="18c4f-222">Die **PriorityBase** -Eigenschaft kann einen Wert zwischen 0 und 31 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="18c4f-222">The **PriorityBase** property can have a value between 0 and 31.</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-223">**Processcreationclassname**</span><span class="sxs-lookup"><span data-stu-id="18c4f-223">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-226">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM- \_ Prozess**](cim-process.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="18c4f-226">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-227">Der Wert der Eigenschaft " **upationclassname** " des Bereichs Prozesses.</span><span class="sxs-lookup"><span data-stu-id="18c4f-227">Value of the scoping process **CreationClassName** property.</span></span>

<span data-ttu-id="18c4f-228">Diese Eigenschaft wird vom [**CIM- \_ Thread**](cim-thread.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-228">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-229">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="18c4f-229">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-232">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**propagierter**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Prozess**](cim-process.md).**Handle**"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) (" Win32API \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ")</span><span class="sxs-lookup"><span data-stu-id="18c4f-232">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32OwnerProcessID")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-233">Prozess, mit dem der Thread erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="18c4f-233">Process that created the thread.</span></span> <span data-ttu-id="18c4f-234">Der Inhalt dieser Eigenschaft kann von API-Elementen (Windows Application Programming Interface) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18c4f-234">The contents of this property can be used by Windows application programming interface (API) elements.</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-235">**STARTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="18c4f-235">**StartAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-236">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18c4f-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-238">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WIn32API \| Thread Objekt \| lpthread \_ Start \_ Routine \| lpstartaddress")</span><span class="sxs-lookup"><span data-stu-id="18c4f-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIn32API\|Thread Object\|LPTHREAD\_START\_ROUTINE\|lpStartAddress")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-239">Die Startadresse des Threads.</span><span class="sxs-lookup"><span data-stu-id="18c4f-239">Starting address of the thread.</span></span> <span data-ttu-id="18c4f-240">Da jede Anwendung mit geeignetem Zugriff auf den Thread den Kontext des Threads ändern kann, ist dieser Wert möglicherweise nur ein Näherungswert für die Anfangsadresse des Threads.</span><span class="sxs-lookup"><span data-stu-id="18c4f-240">Because any application with appropriate access to the thread can change the thread's context, this value may only be an approximation of the thread's starting address.</span></span>

</dd> <dt>

<span data-ttu-id="18c4f-241">**Status**</span><span class="sxs-lookup"><span data-stu-id="18c4f-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18c4f-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-244">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="18c4f-244">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-245">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="18c4f-245">Current status of the object.</span></span> <span data-ttu-id="18c4f-246">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="18c4f-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="18c4f-247">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="18c4f-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="18c4f-248">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="18c4f-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="18c4f-249">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="18c4f-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="18c4f-250">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="18c4f-250">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="18c4f-251">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="18c4f-252">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="18c4f-252">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18c4f-253">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="18c4f-253">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="18c4f-254">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="18c4f-254">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18c4f-255">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="18c4f-255">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18c4f-256">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="18c4f-256">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="18c4f-257">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="18c4f-257">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="18c4f-258">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="18c4f-258">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="18c4f-259">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="18c4f-259">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="18c4f-260">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="18c4f-260">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="18c4f-261">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="18c4f-261">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="18c4f-262">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="18c4f-262">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="18c4f-263">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="18c4f-263">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="18c4f-264">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="18c4f-264">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18c4f-265">**ThreadState**</span><span class="sxs-lookup"><span data-stu-id="18c4f-265">**ThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-266">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18c4f-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-268">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Thread State")</span><span class="sxs-lookup"><span data-stu-id="18c4f-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread State")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-269">Aktueller Ausführungs Status für den Thread.</span><span class="sxs-lookup"><span data-stu-id="18c4f-269">Current execution state for the thread.</span></span>

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span data-ttu-id="18c4f-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Initialisiert** (0)</span><span class="sxs-lookup"><span data-stu-id="18c4f-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Initialized** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18c4f-271">Initialisiert – wird vom Mikrokernel erkannt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-271">Initialized — It is recognized by the microkernel.</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="18c4f-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Bereit** (1)</span><span class="sxs-lookup"><span data-stu-id="18c4f-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18c4f-273">Bereit – Sie ist für die Durchführung auf dem nächsten verfügbaren Prozessor vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="18c4f-273">Ready — It is prepared to run on the next available processor.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="18c4f-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (2)</span><span class="sxs-lookup"><span data-stu-id="18c4f-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18c4f-275">Wird ausgeführt – wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-275">Running — It is executing.</span></span>

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span data-ttu-id="18c4f-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)</span><span class="sxs-lookup"><span data-stu-id="18c4f-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18c4f-277">Standby – es wird gerade ausgeführt, es kann jeweils nur ein Thread in diesem Zustand sein.</span><span class="sxs-lookup"><span data-stu-id="18c4f-277">Standby — It is about to run, only one thread may be in this state at a time.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="18c4f-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Beendet** (4)</span><span class="sxs-lookup"><span data-stu-id="18c4f-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18c4f-279">Beendet – die Ausführung ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="18c4f-279">Terminated — It is finished executing.</span></span>

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span data-ttu-id="18c4f-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Warten** (5)</span><span class="sxs-lookup"><span data-stu-id="18c4f-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Waiting** (5)</span></span>


</dt> <dd>

<span data-ttu-id="18c4f-281">Warten – es ist nicht bereit für den Prozessor, wenn er bereit ist, wird er neu geplant.</span><span class="sxs-lookup"><span data-stu-id="18c4f-281">Waiting — It is not ready for the processor, when ready, it will be rescheduled.</span></span>

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span data-ttu-id="18c4f-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Übergang** (6)</span><span class="sxs-lookup"><span data-stu-id="18c4f-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transition** (6)</span></span>


</dt> <dd>

<span data-ttu-id="18c4f-283">Übergang – der Thread wartet auf andere Ressourcen als der Prozessor.</span><span class="sxs-lookup"><span data-stu-id="18c4f-283">Transition — The thread is waiting for resources other than the processor,</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18c4f-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (7)</span><span class="sxs-lookup"><span data-stu-id="18c4f-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (7)</span></span>


</dt> <dd>

<span data-ttu-id="18c4f-285">Unbekannt – der Thread Zustand ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-285">Unknown — The thread state is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18c4f-286">**ThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="18c4f-286">**ThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-287">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18c4f-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-289">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Thread Wait Reason")</span><span class="sxs-lookup"><span data-stu-id="18c4f-289">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread Wait Reason")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-290">Grund, warum der Thread wartet.</span><span class="sxs-lookup"><span data-stu-id="18c4f-290">Reason why the thread is waiting.</span></span> <span data-ttu-id="18c4f-291">Dieser Wert ist nur gültig, wenn der **Thread State** -Member auf "Transition (6)" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="18c4f-291">This value is only valid if the **ThreadState** member is set to Transition (6).</span></span> <span data-ttu-id="18c4f-292">Ereignis Paare ermöglichen die Kommunikation mit geschützten Subsystemen.</span><span class="sxs-lookup"><span data-stu-id="18c4f-292">Event pairs allow communication with protected subsystems.</span></span>

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="18c4f-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Führungs** Kraft (0)</span><span class="sxs-lookup"><span data-stu-id="18c4f-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="18c4f-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**Freepage** (1)</span><span class="sxs-lookup"><span data-stu-id="18c4f-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18c4f-295">Freepage</span><span class="sxs-lookup"><span data-stu-id="18c4f-295">FreePage</span></span>

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="18c4f-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pagein** (2)</span><span class="sxs-lookup"><span data-stu-id="18c4f-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="18c4f-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**Poolallocation** (3)</span><span class="sxs-lookup"><span data-stu-id="18c4f-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="18c4f-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**Executiondelay** (4)</span><span class="sxs-lookup"><span data-stu-id="18c4f-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="18c4f-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**Freepage** (5)</span><span class="sxs-lookup"><span data-stu-id="18c4f-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="18c4f-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pagein** (6)</span><span class="sxs-lookup"><span data-stu-id="18c4f-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="18c4f-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span><span class="sxs-lookup"><span data-stu-id="18c4f-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="18c4f-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**Freepage** (8)</span><span class="sxs-lookup"><span data-stu-id="18c4f-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="18c4f-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pagein** (9)</span><span class="sxs-lookup"><span data-stu-id="18c4f-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="18c4f-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**Poolallocation** (10)</span><span class="sxs-lookup"><span data-stu-id="18c4f-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="18c4f-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**Executiondelay** (11)</span><span class="sxs-lookup"><span data-stu-id="18c4f-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="18c4f-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**Freepage** (12)</span><span class="sxs-lookup"><span data-stu-id="18c4f-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="18c4f-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pagein** (13)</span><span class="sxs-lookup"><span data-stu-id="18c4f-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span data-ttu-id="18c4f-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**Eventpaarhigh** (14)</span><span class="sxs-lookup"><span data-stu-id="18c4f-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span data-ttu-id="18c4f-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**Eventpaarlow** (15)</span><span class="sxs-lookup"><span data-stu-id="18c4f-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span data-ttu-id="18c4f-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**Lpcreceive** (16)</span><span class="sxs-lookup"><span data-stu-id="18c4f-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span data-ttu-id="18c4f-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**Lpkreply** (17)</span><span class="sxs-lookup"><span data-stu-id="18c4f-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span data-ttu-id="18c4f-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**Virtualmemory** (18)</span><span class="sxs-lookup"><span data-stu-id="18c4f-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span data-ttu-id="18c4f-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)</span><span class="sxs-lookup"><span data-stu-id="18c4f-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18c4f-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (20)</span><span class="sxs-lookup"><span data-stu-id="18c4f-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (20)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18c4f-315">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="18c4f-315">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18c4f-316">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18c4f-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18c4f-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18c4f-318">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("UserModeTime"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Performance Data Structures \| [**perf \_ Object \_ Type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| usertime"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span><span class="sxs-lookup"><span data-stu-id="18c4f-318">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="18c4f-319">Zeit im Benutzermodus in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="18c4f-319">Time in user mode, in 100 nanoseconds units.</span></span> <span data-ttu-id="18c4f-320">Wenn diese Informationen nicht verfügbar sind, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18c4f-320">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="18c4f-321">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="18c4f-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18c4f-322">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18c4f-322">Remarks</span></span>

<span data-ttu-id="18c4f-323">Die **Win32- \_ Thread** Klasse wird vom [**CIM- \_ Thread**](cim-thread.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="18c4f-323">The **Win32\_Thread** class is derived from [**CIM\_Thread**](cim-thread.md).</span></span>

<span data-ttu-id="18c4f-324">**Übersicht**</span><span class="sxs-lookup"><span data-stu-id="18c4f-324">**Overview**</span></span>

<span data-ttu-id="18c4f-325">Für eine routinemäßige tägliche Überwachung gibt es in der Regel kaum einen Grund, eine detaillierte Liste der Threads und der zugehörigen Eigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="18c4f-325">For routine day-to-day monitoring, there is usually little reason to have a detailed list of threads and their associated properties.</span></span> <span data-ttu-id="18c4f-326">Auf Computern werden Tausende von Threads im Laufe eines Tages erstellt und gelöscht. einige dieser Erstellungs-oder Löschvorgänge sind für alle Benutzer, aber für den Entwickler, der die Software geschrieben hat, aussagekräftig.</span><span class="sxs-lookup"><span data-stu-id="18c4f-326">Computers create and delete thousands of threads during the course of a day, and few of these creations or deletions are meaningful to anyone but the developer who wrote the software.</span></span>

<span data-ttu-id="18c4f-327">Wenn Sie jedoch Probleme mit einer Anwendung beheben, können Sie bei der Nachverfolgung der einzelnen Threads für einen Prozess ermitteln, wann Threads erstellt werden und wann (oder ob) Sie zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="18c4f-327">However, when you are troubleshooting problems with an application, tracking the individual threads for a process allows you to identify when threads are created and when (or if) they are destroyed.</span></span> <span data-ttu-id="18c4f-328">Da Threads, die erstellt, aber nicht zerstört werden, zu Speicher Verlusten führen, kann das Nachverfolgen einzelner Threads nützliche Informationen für Support Techniker sein.</span><span class="sxs-lookup"><span data-stu-id="18c4f-328">Because threads that are created but not destroyed cause memory leaks, tracking individual threads can be useful information for support technicians.</span></span> <span data-ttu-id="18c4f-329">Analog dazu können Thread Prioritäten identifiziert werden, die die CPU-Zyklen, die von anderen Threads und anderen Prozessen benötigt werden, durch die Ausführung mit einer ungewöhnlich hohen Priorität als präemptiv halten.</span><span class="sxs-lookup"><span data-stu-id="18c4f-329">Likewise, identifying thread priorities can help pinpoint threads that, by running at an abnormally high priority, are preempting CPU cycles needed by other threads and other processes.</span></span>

<span data-ttu-id="18c4f-330">**Verwenden des Win32- \_ Threads**</span><span class="sxs-lookup"><span data-stu-id="18c4f-330">**Using Win32\_Thread**</span></span>

<span data-ttu-id="18c4f-331">Wie im vorangehenden Syntax Block impliziert, meldet die **Win32- \_ Thread** Klasse nicht den Namen des Prozesses, in dem jeder Thread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18c4f-331">As implied in the preceding syntax block, the **Win32\_Thread** class does not report the name of the process under which each thread runs.</span></span> <span data-ttu-id="18c4f-332">Stattdessen meldet er die ID des Prozesses, unter dem der Thread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18c4f-332">Instead, it reports the ID of the process under which the thread runs.</span></span> <span data-ttu-id="18c4f-333">Um den Namen eines Prozesses und eine Liste aller zugehörigen Threads zurückzugeben, muss Ihr Skript Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="18c4f-333">To return the name of a process and a list of all its threads, your script must:</span></span>

1.  <span data-ttu-id="18c4f-334">Stellen Sie eine Verbindung mit der [**Win32- \_ Prozess**](win32-process.md) Klasse her, und geben Sie die Liste der Prozesse und deren Prozess-IDs</span><span class="sxs-lookup"><span data-stu-id="18c4f-334">Connect to the [**Win32\_Process**](win32-process.md) class and return the list of processes and their process IDs.</span></span>
2.  <span data-ttu-id="18c4f-335">Temporäres Speichern dieser Informationen in einem Array-oder Wörterbuch Objekt.</span><span class="sxs-lookup"><span data-stu-id="18c4f-335">Temporarily store this information in an array or Dictionary object.</span></span>
3.  <span data-ttu-id="18c4f-336">Geben Sie für jede Prozess-ID die Liste der Threads für diesen Prozess zurück, und zeigen Sie dann den Prozessnamen und die Liste der Threads an.</span><span class="sxs-lookup"><span data-stu-id="18c4f-336">For each process ID, return the list of threads for that process, and then display the process name and the list of threads.</span></span>

## <a name="examples"></a><span data-ttu-id="18c4f-337">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18c4f-337">Examples</span></span>

<span data-ttu-id="18c4f-338">Im folgenden VBScript-Beispiel werden die auf einem Computer laufenden Threads überwacht.</span><span class="sxs-lookup"><span data-stu-id="18c4f-338">The following VBScript sample monitors the threads running on a computer.</span></span>


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
```



## <a name="requirements"></a><span data-ttu-id="18c4f-339">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18c4f-339">Requirements</span></span>



| <span data-ttu-id="18c4f-340">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18c4f-340">Requirement</span></span> | <span data-ttu-id="18c4f-341">Wert</span><span class="sxs-lookup"><span data-stu-id="18c4f-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18c4f-342">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18c4f-342">Minimum supported client</span></span><br/> | <span data-ttu-id="18c4f-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18c4f-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18c4f-344">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18c4f-344">Minimum supported server</span></span><br/> | <span data-ttu-id="18c4f-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18c4f-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18c4f-346">Namespace</span><span class="sxs-lookup"><span data-stu-id="18c4f-346">Namespace</span></span><br/>                | <span data-ttu-id="18c4f-347">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="18c4f-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18c4f-348">MOF</span><span class="sxs-lookup"><span data-stu-id="18c4f-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18c4f-349"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="18c4f-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18c4f-350">DLL</span><span class="sxs-lookup"><span data-stu-id="18c4f-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18c4f-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18c4f-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18c4f-352">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18c4f-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c4f-353">**CIM- \_ Thread**</span><span class="sxs-lookup"><span data-stu-id="18c4f-353">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dt>

[<span data-ttu-id="18c4f-354">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="18c4f-354">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
